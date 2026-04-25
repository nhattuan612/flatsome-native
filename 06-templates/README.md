# Bộ Biểu Mẫu Chuẩn Flatsome Native

Date: 2026-04-24

## Mục Đích

Thư mục này chứa các biểu mẫu chuẩn để biến luật công ty thành thao tác có thể điền, kiểm và lưu lại.

Mục tiêu:

- mọi task dùng cùng một form
- giảm sai khác giữa người làm
- tăng khả năng review, audit và tái sử dụng

## Danh Sách Biểu Mẫu

- `06-templates/Page Plan Template.md`
- `06-templates/Native Scoring Template.md`
- `06-templates/Novelty Scoring Template.md`
- `06-templates/Native Build Output Template.md`
- `06-templates/Audit Checklist Template.md`
- `06-templates/Fix Pass Template.md`
- `06-templates/Final Verification Template.md`
- `06-templates/Exception Report Template.md`
- `06-templates/Block Entry Template.md`

## Quy Tắc Dùng

1. Không tự phát minh biểu mẫu mới nếu biểu mẫu chuẩn đã đủ.
2. Nếu cần thay đổi biểu mẫu, phải cập nhật file gốc trong thư mục này.
3. Mọi task UI nên bắt đầu từ `06-templates/Page Plan Template.md`.
4. Trước `Page Plan`, worker phải đi qua `05-flows/Input Contract.md` và `05-flows/Brief Intake Flow.md`.
5. Mọi task hoàn thành phải có `06-templates/Native Scoring Template.md`.
6. Mọi task hoàn thành phải có `06-templates/Novelty Scoring Template.md`.
7. Mọi task hoàn thành phải có artifact `Native Build Output`, được tạo theo `06-templates/Native Build Output Template.md`.
8. Mọi task hoàn thành phải có artifact `Audit Checklist`, được tạo theo `06-templates/Audit Checklist Template.md`.
9. Mọi task hoàn thành phải có artifact `Fix Pass`, được tạo theo `06-templates/Fix Pass Template.md`.
10. Mọi task hoàn thành phải có artifact `Final Verification`, được tạo theo `06-templates/Final Verification Template.md`.
11. Mọi ngoại lệ hiếm phải có `06-templates/Exception Report Template.md`.
12. Mọi block muốn đưa vào quản trị phải đi qua `06-templates/Block Entry Template.md`.
13. Vị trí lưu artifact phải theo `01-platform/Artifact Storage Rule.md`.
14. `Page Plan Template` hiện cũng là `Build Readiness Contract`, không chỉ là sơ đồ section.
15. `Fix Pass` không chỉ ghi "đã sửa", mà phải ghi đủ:
   - `nhóm lỗi`
   - `lỗi gốc`
   - `cách sửa`
   - `bề mặt kiểm lại`
   - `kết quả sau sửa`
16. `Final Verification` chỉ hợp lệ khi `Repair Gate` đã pass.
