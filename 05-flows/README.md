# 05-flows

Date: 2026-04-25

## Mục Đích

Đây là lớp `cách làm`.

Nếu `01-platform` là luật và `03-factory` là khả năng build, thì `05-flows` là trình tự thao tác.

## Đọc Gì Trước

Khi build UI:

1. `05-flows/Task Type Router.md`
2. `05-flows/Quick Start Menu.md`
3. `05-flows/Guided Intake Questions.md`
4. `05-flows/Input Contract.md`
5. `05-flows/Master System Flow Map.md`
6. `05-flows/Brief Intake Flow.md`
7. `05-flows/UI Build Script.md`
8. `05-flows/Final QA Checklist.md`

Nếu task cần sáng tạo mạnh hoặc route theo design language ngoài:

1. `08-design-intelligence/README.md`
2. `08-design-intelligence/Design Mode Router.md`

Nếu task đã build xong và cần lưu đúng artifact:

1. `01-platform/Artifact Storage Rule.md`

Nếu task là hút hoặc extract template:

1. `05-flows/Verifiable Harvest Flow.md`
2. `05-flows/Imported Template Extraction Flow.md`

Nếu cần hiểu vai trò worker:

1. `05-flows/Execution Role Boundaries.md`

Khi harvest Flatsome Studio:

1. `05-flows/Verifiable Harvest Flow.md`
2. `05-flows/Direct Harvest Flow.md`

## File Nào Làm Gì

- `05-flows/Brief Intake Flow.md`
  - chuẩn hóa brief trước page plan
- `05-flows/Task Type Router.md`
  - khóa loại task trước khi mở flow chi tiết
- `05-flows/Input Contract.md`
  - khóa đầu vào trước brief intake
- `05-flows/Guided Intake Questions.md`
  - script hỏi đáp ngắn cho người mới hoàn toàn
- `05-flows/Quick Start Menu.md`
  - menu chọn nhánh nhanh trước khi hỏi sâu
- `05-flows/Best Result Playbook.md`
  - hướng dẫn người giao task để ra kết quả tốt nhất
- `05-flows/Master System Flow Map.md`
  - lưu đồ tổng từ intake đến release
- `05-flows/UI Build Script.md`
  - kịch bản build trang chuẩn
- `05-flows/Final QA Checklist.md`
  - checklist kiểm cuối
- `05-flows/Verifiable Harvest Flow.md`
  - flow harvest có verify thật
- `05-flows/Direct Harvest Flow.md`
  - flow import/hút trực tiếp
- `05-flows/Imported Template Extraction Flow.md`
  - flow đọc và trích shortcode từ page/imported surface
- `05-flows/Execution Role Boundaries.md`
  - vai trò và boundary của Codex / OpenClaw / worker

## Source Of Truth Trong Folder Này

- build UI: `05-flows/UI Build Script.md`
- task type router: `05-flows/Task Type Router.md`
- audit cuối: `05-flows/Final QA Checklist.md`
- quick start: `05-flows/Quick Start Menu.md`
- intake questions: `05-flows/Guided Intake Questions.md`
- intake contract: `05-flows/Input Contract.md`
- master flow map: `05-flows/Master System Flow Map.md`
- brief route: `05-flows/Brief Intake Flow.md`
- harvest: `05-flows/Verifiable Harvest Flow.md`
- nơi lưu artifact: `01-platform/Artifact Storage Rule.md`

## Khi Nào Cập Nhật

- khi phát hiện flow hiện tại thiếu bước
- khi có lỗi vận hành lặp lại
- khi cần rút ngắn flow mà vẫn giữ an toàn

## Không Được Làm

- không viết flow mơ hồ
- không bỏ bước verify
- không coi progress giả là hoàn thành thật

## Kết Luận

AI muốn làm đúng quy trình mà không phải đoán thì đọc folder này.
