# AI HANDOFF GUIDE

Date: 2026-04-25

## Mục Đích

Đây là file handoff cho `Codex / GPT / OpenClaw / AI worker khác`.

Mục tiêu là để AI mới vào đọc ít nhưng route đúng nhanh.

## Luật Cứng Phải Nạp Trước

Phải giữ nguyên:

- `section-first`
- `section -> row -> col -> element`
- `native >= 90%`
- không dùng `ux_html` làm layout shell chính
- `ux_html` chỉ dùng cho `iframe / embed / link / map` hoặc ngoại lệ hiếm
- output phải mở lại được bằng `Flatsome UX Builder`
- không dùng `report` thay cho `law`

## Đường Đọc Tối Thiểu

Nếu chỉ được đọc ít file trước khi làm:

1. `MASTER OPERATING MEMORY.md`
2. `START HERE.md`
3. `05-flows/Task Type Router.md`
4. `05-flows/Input Contract.md`
5. `05-flows/Master System Flow Map.md`
6. `01-platform/Operating Law.md`
7. `06-templates/Page Plan Template.md`
8. `05-flows/UI Build Script.md`
9. `05-flows/Final QA Checklist.md`

## Route Theo Loại Task

### Nếu là `page-task`

Đọc:

1. `05-flows/Quick Start Menu.md`
2. `05-flows/Guided Intake Questions.md`
3. `05-flows/Input Contract.md`
4. `05-flows/Brief Intake Flow.md`
5. `03-factory/Task Route Matrix.md`
6. `03-factory/Page Goal Routing.md`
7. `06-templates/Page Plan Template.md`
8. `05-flows/UI Build Script.md`
9. `05-flows/Final QA Checklist.md`

### Nếu là `harvest-task`

Đọc:

1. `05-flows/Verifiable Harvest Flow.md`
2. `05-flows/Direct Harvest Flow.md`
3. `01-platform/Artifact Storage Rule.md`

### Nếu là `extract-task`

Đọc:

1. `05-flows/Imported Template Extraction Flow.md`
2. `01-platform/Native Builder Language Map.md`
3. `01-platform/Artifact Storage Rule.md`

### Nếu là `system-doc-task`

Đọc:

1. `README.md`
2. `MASTER OPERATING MEMORY.md`
3. `01-platform/Artifact Storage Rule.md`
4. `05-flows/Master System Flow Map.md`

## Khi Nào Mở Lớp Sáng Tạo

Chỉ mở `08-design-intelligence/` khi:

- user yêu cầu sáng tạo mạnh
- user muốn theo một design language cụ thể
- input tham chiếu yêu cầu reinterpret thay vì clone

Nếu không có chỉ định rõ:

- mặc định dùng `Flatsome Native Core`

## Build Không Được Bắt Đầu Khi Chưa Khóa

Trước `Page Plan`, phải khóa:

- `loại input`
- `output expectation`
- `style source`
- `reference authority`
- `CTA chính`
- `thiết bị ưu tiên`

Nếu thiếu:

- ghi `không xác định`
- dùng `default an toàn`
- không tự bịa

## Artifact Bắt Buộc

Mọi `page-task` phải có:

- `Spec`
- `Input Contract`
- `Page Plan`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

Nơi lưu:

- xem `01-platform/Artifact Storage Rule.md`

## Cách Không Làm Hỏng Hub

Khi sửa luật:

- chỉ sửa `01-platform/`

Khi sửa flow:

- chỉ sửa `05-flows/`

Khi sửa template:

- chỉ sửa `06-templates/`

Khi thêm report:

- để vào `07-reports/`

Khi thêm page-specific spec/report:

- để ngoài hub tại `VPS/docs/superpowers/specs/` hoặc `VPS/docs/superpowers/reports/`

## AI Mới Vào Thường Sai Ở Đâu

Sai phổ biến:

- đọc report cũ rồi tưởng là luật
- bỏ qua `Input Contract`
- build luôn khi chưa khóa `output expectation`
- thay đổi skin nhưng giữ nguyên macro sequence
- dùng `ux_html` để vá layout thay vì sửa native structure

## Check Trước Khi Kết Thúc

Trước khi báo xong, phải chắc:

- builder mở lại được
- public page ổn
- edit page ổn
- không còn lỗi blocking
- artifact lưu đúng nơi
- nếu là page mới, đã xét `Recent Page Memory`

## Kết Luận

Muốn AI làm đúng, phải route theo task type trước, rồi mới build.
Đừng cho AI nhảy thẳng từ brief sang shortcode.
