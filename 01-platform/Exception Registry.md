# Sổ Đăng Ký Ngoại Lệ Cho Flatsome Native

Date: 2026-04-24

## Mục Đích

Tài liệu này tồn tại để kiểm soát `ngoại lệ hiếm`.

Nếu không có sổ này, ngoại lệ sẽ biến thành đường tắt mặc định và làm hệ thống xuống cấp theo thời gian.

## Nguyên Tắc

- ngoại lệ là `hiếm`
- ngoại lệ không phải là quyền tự do làm tắt
- ngoại lệ chỉ tồn tại khi hệ chuẩn không xử lý tốt hơn
- mọi ngoại lệ phải được ghi lại

## Khi Nào Được Mở Ngoại Lệ

Chỉ được mở ngoại lệ khi đồng thời đúng:

- `public page` hoàn hảo
- `native >= 90%`
- `Codex` chấp thuận
- có `report + file/log`

## Khi Nào Không Được Mở Ngoại Lệ

Không được mở ngoại lệ nếu:

- chỉ để làm nhanh hơn
- chỉ để né `Page Plan`
- chỉ để bỏ qua kiểm tra cuối
- chỉ vì không muốn sửa lại native structure

## Trường Bắt Buộc Của Một Ngoại Lệ

Mỗi ngoại lệ phải có đủ:

- `Mã ngoại lệ`
- `Ngày`
- `Bối cảnh`
- `Người đề xuất`
- `Người phê chuẩn`
- `Lý do`
- `Chuẩn mặc định bị lệch ở đâu`
- `Ảnh hưởng`
- `Cách quay về chuẩn sau này`
- `Trạng thái`

## Vị Trí Lưu Chuẩn

Mọi report hoặc log ngoại lệ phải lưu tại:

- `VPS/docs/superpowers/flatsome-native/07-reports/exceptions/`

Tên file bắt buộc theo mẫu:

- `EX-YYYY-MM-DD-XX` + phần mở rộng .md

Ví dụ:

- `EX-2026-04-24-01` + phần mở rộng .md

## Mẫu Một Dòng Đăng Ký

```md
- Mã ngoại lệ: EX-2026-04-24-01
  - Ngày: 2026-04-24
  - Bối cảnh: trang tuyển dụng / nhúng map
  - Người đề xuất: Codex
  - Người phê chuẩn: Codex
  - Lý do: Builder không tái hiện được hiệu ứng nhúng map theo đúng kỳ vọng chỉ bằng native settings
  - Chuẩn mặc định bị lệch ở đâu: dùng `ux_html` để chèn `map`
  - Ảnh hưởng: không ảnh hưởng layout chính, native vẫn > 90%
  - Cách quay về chuẩn sau này: khi có native pattern tốt hơn thì bỏ ngoại lệ này
  - Trạng thái: đang hiệu lực
```

## Quy Tắc CEO

Nếu cùng một loại ngoại lệ lặp lại từ `2-3 lần`, không được tiếp tục coi nó là ngoại lệ riêng lẻ.

Khi đó phải làm một trong hai việc:

1. cập nhật `Operating Law`
2. cập nhật `UI Build Script`

Nói cách khác:

- ngoại lệ lặp nhiều lần = luật đang thiếu

## Trạng Thái Ngoại Lệ

Mỗi ngoại lệ chỉ được ở một trong ba trạng thái:

- `đang hiệu lực`
- `đã thay thế bằng luật mới`
- `đã đóng`

## Checklist Trước Khi Duyệt Ngoại Lệ

- [ ] Public page có thật sự hoàn hảo không
- [ ] Native có đạt `>=90%` không
- [ ] Có report không
- [ ] Có file/log không
- [ ] Có giải pháp native tốt hơn không
- [ ] Ngoại lệ này có nguy cơ bị lạm dụng không

Nếu bất kỳ câu nào trả lời không rõ, chưa được duyệt ngoại lệ.
