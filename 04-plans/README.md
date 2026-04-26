# 04-plans

Date: 2026-04-25

## Mục Đích

Folder này chỉ lưu `kế hoạch nâng cấp hệ thống đã duyệt`.

Nó dùng để:

- bắt đầu lại bất cứ lúc nào ở các workstream cấp hệ
- hiểu đã nâng cấp gì
- tránh làm trùng
- giữ dấu vết quyết định kiến trúc

## Đọc Gì Trước

Không phải folder đọc đầu tiên.

Chỉ mở khi cần:

- xem một đợt nâng cấp đã định làm gì
- audit xem tài liệu nào sinh ra từ kế hoạch nào
- tiếp tục một workstream cũ

## File Nào Làm Gì

- mỗi file plan = một đợt nâng cấp hoặc một nhiệm vụ lớn đã chốt
- tên file theo ngày + chủ đề

## Legacy Convention Còn Được Giữ

Một số plan lịch sử trong folder này vẫn còn:

- tham chiếu kiểu filename-only như `README.md`, `START HERE.md`
- đường dẫn cũ kiểu `...`
- wording theo trạng thái của hệ ở thời điểm plan được viết

Điều này là `giữ nguyên lịch sử`, không phải lỗi route hiện hành.

Khi đọc:

- chỉ lấy `ý định nâng cấp`
- không lấy wording cũ làm luật đang chạy
- không sửa hàng loạt plan cũ chỉ để đồng bộ câu chữ, trừ khi làm một đợt archive cleanup riêng

## Không Còn Lưu Ở Đây

Folder này không còn chứa:

- page-specific implementation plan
- execution plan cho 1 landing page cụ thể
- delivery plan cho 1 task content/page riêng lẻ

Những file đó phải đi về:

- `specs/ (ngoài hub)`
- hoặc `specs/page-task-plans/ (ngoài hub)`

## Source Of Truth

Folder này `không` là source of truth cho luật hay syntax hiện hành.

Source of truth luôn nằm ở:

- `01-platform/`
- `03-factory/`
- `05-flows/`

## Khi Nào Cập Nhật

- khi bắt đầu một hướng nâng cấp mới
- khi chốt một plan mới cần lưu dấu vết

## Không Được Làm

- không sửa plan cũ để viết lại lịch sử
- không dùng plan thay cho luật hiện hành
- không nhét output thực thi cuối vào đây
- không đưa page-specific implementation plan trở lại folder này

## Kết Luận

Đây là lớp lịch sử quyết định, không phải lớp đọc vận hành hằng ngày.
