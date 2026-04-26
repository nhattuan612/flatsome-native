# 07-reports

Date: 2026-04-25

## Mục Đích

Folder này lưu `bằng chứng đã làm`.

Nó trả lời:

- đã làm gì
- học được gì
- còn thiếu gì
- kết quả của từng đợt nâng cấp ra sao

## Đọc Gì Trước

Không phải folder đọc đầu tiên.

Chỉ mở khi cần:

- xem evidence
- audit một claim
- tra nguồn gốc của một quyết định

## File Nào Làm Gì

- mỗi report = kết quả của một plan hoặc một đợt triển khai
- `07-reports/Recent Page Memory.md`
  - bộ nhớ vận hành ngắn hạn để novelty gate so layout gần nhất
- `exceptions/`
  - nơi chứa report ngoại lệ nếu có

## Legacy Convention Còn Được Giữ

Một số report lịch sử trong folder này vẫn còn:

- tham chiếu kiểu filename-only như `README.md`, `START HERE.md`
- đường dẫn cũ kiểu `...`
- mô tả lại trạng thái hệ tại thời điểm report được ghi

Điều này là `evidence lịch sử`, không phải chỉ dẫn vận hành mới nhất.

Khi đọc:

- dùng để audit claim hoặc truy quyết định
- không copy wording cũ sang lớp core
- nếu report lệch với lớp core hiện tại thì tin `01-platform/`, `03-factory/`, `05-flows/`, `06-templates/`

## Không Phải Luật Đang Chạy

Trừ `07-reports/Recent Page Memory.md`, mọi file trong folder này chỉ là:

- evidence
- historical audit
- record của điều đã làm

Nếu report nói khác với:

- `01-platform/`
- `03-factory/`
- `05-flows/`

thì luôn tin lớp core trước.

## Source Of Truth

Folder này `không` là source of truth vận hành.

Nó chỉ là:

- bằng chứng
- báo cáo
- kết quả học được

Source of truth vận hành vẫn là:

- `01-platform/`
- `03-factory/`
- `05-flows/`

Riêng `07-reports/Recent Page Memory.md` là ngoại lệ hẹp:

- không phải luật
- nhưng là dữ liệu bắt buộc để novelty gate so trang gần nhất

## Khi Nào Cập Nhật

- sau khi hoàn tất một đợt nâng cấp
- sau khi hoàn tất một đợt săn syntax
- sau khi hoàn tất một đợt refactor lớn

## Không Được Làm

- không dùng report thay luật
- không để report chứa brand/project-specific nếu report thuộc lớp tri thức tổng
- không đọc report trước khi đọc luật và flow
- không dùng report cũ làm shortcut để bỏ qua flow hiện hành

## Kết Luận

Đây là lớp bằng chứng, không phải lớp onboarding đầu tiên.
