# Repair Gate Runtime Report

Date: 2026-04-25

## Mục Tiêu

Nối `Repair Gate` từ lớp tài liệu xuống lớp runtime thực thi để task page mới không còn publish trực tiếp kiểu cũ.

## Đã Làm

- tạo helper runtime dùng chung:
  - `tmp/flatsome_runtime_gate.py`
- tạo wrapper orchestrator:
  - `tmp/run_flatsome_repair_gate.py`
- nối helper vào:
  - `tmp/publish_wp_page_from_shortcode.py`
  - `tmp/verify_wp_page_surfaces.py`
- chuyển các launcher `create_*` sang dùng `run_repair_gate(...)`:
  - `tmp/create_real_estate_homepage_test_page.py`
  - `tmp/create_orange_juice_homepage_test_page.py`
  - `tmp/create_orange_juice_purple_homepage_test_page.py`
  - `tmp/create_orange_juice_apple_style_homepage_test_page.py`
  - `tmp/create_sales_test_page.py`
  - `tmp/create_seox_clone_page.py`
- cập nhật flow doc để runtime khuyến nghị dùng wrapper mới.
- thêm `preflight syntax lint` trước WordPress cho các lỗi nguy hiểm:
  - opener dùng `>` thay vì `]`
  - cặp `tabgroup/tab` mất cân bằng
- bỏ hard-code credentials khỏi source runtime:
  - runtime đọc từ `env` hoặc file local ngoài snapshot
- mở rộng phát hiện `raw shortcode leak` theo token tổng quát hơn
- sửa artifact runtime để không tự nhận `full QA pass`

## Runtime Mới Hoạt Động Thế Nào

Chuỗi thực thi:

- tạo page ở `draft`
- preflight `edit + builder`
- chỉ publish nếu preflight pass
- verify `public`
- nếu fail thì kéo page về `draft`
- ghi `Fix Pass`
- ghi `Final Verification`

Lưu ý:

- `Final Verification` do runtime gate sinh ra là `surface verification artifact`
- nó không thay thế `full QA` của task build hoàn chỉnh

## Evidence

### Unit Test

Command:

```bash
python3 -m unittest tmp/tests/test_flatsome_runtime_gate.py
```

Result:

- `Ran 10 tests`
- `OK`

### Syntax Check

Command:

```bash
python3 -m py_compile \
  tmp/run_flatsome_repair_gate.py \
  tmp/create_real_estate_homepage_test_page.py \
  tmp/create_orange_juice_homepage_test_page.py \
  tmp/create_orange_juice_purple_homepage_test_page.py \
  tmp/create_orange_juice_apple_style_homepage_test_page.py \
  tmp/create_sales_test_page.py \
  tmp/create_seox_clone_page.py \
  tmp/publish_wp_page_from_shortcode.py \
  tmp/verify_wp_page_surfaces.py \
  tmp/flatsome_runtime_gate.py
```

Result:

- exit `0`

### Smoke Test Pass

- Post ID: `[redacted]`
- Public URL:
  - `https://your-wp-site.com/repair-gate-smoke-test-orange-2026-04-25/`
- Artifact:
  - `docs/superpowers/reports/2026-04-25-repair-gate-smoke-test-fix-pass.md`
  - `docs/superpowers/reports/2026-04-25-repair-gate-smoke-test-final-verification.md`

### Smoke Test Fail

- Post ID: `1166`
- Failure:
  - `raw shortcode leaked to public page: [/text_box]`
- Runtime action:
  - kéo page về `draft`
- Evidence:
  - `hidden_post_status = draft`
- Artifact:
  - `reports/ (ngoài hub)2026-04-25-repair-gate-broken-probe-fix-pass.md`
  - `reports/ (ngoài hub)2026-04-25-repair-gate-broken-probe-final-verification.md`

### Lint Preflight Fail

- runtime bị chặn trước khi chạm WordPress
- failure:
  - `Shortcode opener dùng '>' thay vì ']' cho [ux_banner]`
- runtime action:
  - `POST_STATUS skipped-before-wordpress`
- artifact:
  - `reports/ (ngoài hub)2026-04-25-repair-gate-lint-probe-fix-pass.md`
  - `reports/ (ngoài hub)2026-04-25-repair-gate-lint-probe-final-verification.md`

## Kết Luận

`Repair Gate` đã không còn là luật trên giấy.

Nó đã:

- chạy thật
- pass ở nhánh tốt
- fail đúng ở nhánh lỗi
- tự kéo page lỗi về `draft`
- tự ghi artifact kiểm tra

## Điểm Chưa Làm

- chưa tự động hóa `Screenshot cuối`
- chưa nối wrapper mới vào toàn bộ mọi pipeline page ngoài nhóm `create_*`
