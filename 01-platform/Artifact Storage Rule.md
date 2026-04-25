# Artifact Storage Rule

Date: 2026-04-25

## Mục Đích

Chuẩn hóa nơi lưu và cách đặt tên cho toàn bộ artifact của task UI.

## Luật Cốt Lõi

1. Mọi task UI phải lưu artifact theo rule này.
2. Không được tự chọn nơi lưu theo cảm tính.
3. Tài liệu nền tảng và tài liệu page-specific phải tách riêng.

## Phân Loại Artifact

### 1. Nền tảng

Là tri thức dùng chung cho nhiều task.

Lưu tại:

- `01-platform/`
- `03-factory/`
- `05-flows/`
- `06-templates/`
- `08-design-intelligence/`

### 2. Kế hoạch hệ thống

Là plan nâng cấp kiến trúc hoặc tri thức tổng.

Lưu tại:

- `04-plans/`

### 2b. Kế hoạch theo task / page

Là execution plan cho một page hoặc một task giao hàng cụ thể.

Lưu tại:

- `VPS/docs/superpowers/specs/`
- hoặc `VPS/docs/superpowers/specs/page-task-plans/`

### 3. Báo cáo hệ thống

Là report audit, harvest, refactor hoặc nâng cấp hệ.

Lưu tại:

- `07-reports/`

### 4. Spec theo task / page

Là mô tả bài toán cụ thể của một page.

Lưu tại:

- `VPS/docs/superpowers/specs/`

### 5. Report theo task / page

Là báo cáo kết quả của một page cụ thể.

Lưu tại:

- `VPS/docs/superpowers/reports/`

### 5b. Report ngoại lệ hiếm

Là report hoặc log cho trường hợp được phê chuẩn lệch chuẩn mặc định.

Lưu tại:

- `VPS/docs/superpowers/flatsome-native/07-reports/exceptions/`

### 6. Shortcode và file thao tác tạm

Lưu tại:

- `VPS/tmp/`

## Tên File Chuẩn

### Plan hệ thống

- `YYYY-MM-DD-<topic>-plan.md`

### Report hệ thống

- `YYYY-MM-DD-<topic>-report.md`
  - hoặc nếu đã có convention cũ thì giữ nhưng ưu tiên hậu tố `report`

### Spec theo task

- `YYYY-MM-DD-<page-or-task>.md`

### Plan theo task / page

- `YYYY-MM-DD-<page-or-task>-plan.md`
- hoặc giữ convention cũ nếu file là archived plan đã tạo trước refactor

### Report theo task

- `YYYY-MM-DD-<page-or-task>.md`
  - tên phải đủ rõ để truy ngược page

### Shortcode

- `<slug>-YYYY-MM-DD.shortcode.txt`

## Gói Artifact Bắt Buộc Cho Một Task UI

Tối thiểu phải có:

- `Spec`
- `Input Contract`
- `Page Plan`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

## Mapping Gợi Ý

- `Spec`
  - `VPS/docs/superpowers/specs/`
- `Input Contract`
  - có thể nằm trong spec file
  - hoặc là section mở đầu của file page plan theo task
- `Page Plan`
  - có thể nằm trong spec file hoặc file page plan riêng theo task
- `Native Build Output`
  - `VPS/docs/superpowers/reports/`
- `Audit Checklist`
  - `VPS/docs/superpowers/reports/`
- `Fix Pass`
  - `VPS/docs/superpowers/reports/`
- `Final Verification`
  - `VPS/docs/superpowers/reports/`
- `Shortcode`
  - `VPS/tmp/`

## Optional Artifact

Chỉ tạo khi cần:

- screenshot riêng nhiều bước
- benchmark note
- exception note
- page override design file

## Không Được Làm

- không trộn task-specific report vào `01-platform/` hoặc `03-factory/`
- không để file tạm trong thư mục luật
- không tạo nhiều file tên mơ hồ kiểu note-final-new.md
- không lưu `ngoại lệ hiếm` chung với report task thông thường
- không lưu page-specific implementation plan trong `04-plans/`

## Kết Luận

Muốn hệ dễ scale và ít rơi đồ, phải lưu artifact đúng chỗ ngay từ đầu.
