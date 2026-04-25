# Flatsome Harvest Verifiable Flow

Date: 2026-04-25

## Mục đích

Thay thế flow batch import cũ trên một page duy nhất vì flow đó tạo ra `false positive`:

- controller báo `DONE`
- state file tăng
- nhưng WordPress không persist nội dung tương ứng

## Kết luận từ flow cũ

- Không dùng `controller.progress === 100` làm tiêu chí hoàn tất.
- Không tiếp tục harvest bulk trên cùng một page duy nhất.
- Mọi lần import sau này phải có bước verify thật sau save.

## Flow mới được ưu tiên

### Option ưu tiên

`fresh-page-per-import` hoặc `small-batch-per-page`

Lý do:

- dễ nhìn bằng mắt
- dễ verify bằng REST/revision
- giảm lệch state trong UX Builder
- nếu hỏng chỉ mất 1 page nhỏ, không hỏng cả batch lớn

## Verify bắt buộc sau mỗi import

1. Save page.
2. Đọc lại page qua REST API.
3. Kiểm tra ít nhất một trong các tín hiệu thật:
   - `modified_gmt` đổi
   - revision count tăng
   - content length đổi đúng kỳ vọng
   - xuất hiện keyword đặc trưng của template vừa import
4. Chỉ khi verify pass mới được ghi `DONE`.

## Tracking cần lưu

- page id
- public url
- template id
- template title
- verify result
- content length sau save
- revision id mới nhất
- telegram message id cho các mốc vận hành chính

## Telegram reporting

- Dùng cấu hình bot/group đã được provisioned tại môi trường vận hành.
- Không hardcode token/chat trong script harvest.
- Báo cáo tại các mốc:
  - `RUN_START`
  - `VERIFIED_TEMPLATE`
  - `CATEGORY_DONE`
  - `RUN_STOP`
  - `RUN_COMPLETE`
  - `FAIL`

## Rule hiện tại của verify

- Điều kiện pass:
  - `contentHash` của page thật sự đổi sau save
- Tín hiệu bổ sung:
  - `signatureMatched`
  - `modified_gmt`
  - `revisionCount`
  - `contentLength`

Lý do:

- `contentHash changed` là hàng rào chặn false positive cũ.
- `signatureMatched` hữu ích nhưng không thể bắt buộc với các template generic dùng nhiều text mẫu hoặc lorem.

## Kết quả mong muốn

- mỗi template import có bằng chứng tồn tại thật trên WordPress
- có thể mở link page để kiểm tra trực quan
- dữ liệu harvest đủ tin cậy để đưa vào `01-platform/Native Builder Language Map.md`

## File Liên Quan

- `05-flows/Imported Template Extraction Flow.md`
- `01-platform/native-builder-language/06-Patterns and Workflow.md`
- `07-reports/Direct Harvest Report.md`
