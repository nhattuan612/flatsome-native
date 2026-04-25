# Playbook Sửa Lỗi Thường Gặp Flatsome Native

Date: 2026-04-25

## Mục Đích

Đây là playbook bắt buộc dùng sau `Audit` và trước `Release`.

Mục tiêu:

- không publish khi mới chỉ "thấy lỗi"
- buộc đi qua vòng `phân loại lỗi -> sửa đúng gốc -> kiểm lại`
- tái sử dụng tri thức từ các lỗi đã gặp thật

## Chuỗi Bắt Buộc

`Audit -> Classify -> Fix -> Re-check -> Re-open Builder -> Public Re-check -> Release`

Không được bỏ bước.

## Cách Dùng

1. Ghi từng lỗi vào `Fix Pass`.
2. Gán mỗi lỗi vào một nhóm lỗi chuẩn bên dưới.
3. Sửa theo hướng ưu tiên được chỉ định.
4. Kiểm lại đúng bề mặt đã lỗi:
   - `public`
   - `edit`
   - `builder`
   - `mobile`
5. Nếu còn lỗi, lặp lại vòng fix.
6. Chỉ khi không còn lỗi `blocking` mới được qua `Final Verification`.

## Nhóm Lỗi Chuẩn

### Nhóm A: Lỗi cú pháp shortcode

Ví dụ:

- shortcode mở bằng `>` thay vì `]`
- đóng sai tag
- thiếu tag đóng
- lồng `row_inner/col_inner` sai
- lộ raw shortcode như `[/text_box]`, `[/tab]`, `[/ux_text]`

Cách sửa ưu tiên:

1. Soát file shortcode nguồn.
2. Sửa cú pháp tại nguồn, không vá ở public.
3. Publish lại.
4. Kiểm public xem còn raw shortcode hay không.
5. Mở lại `edit` và `builder`.

Evidence bắt buộc:

- raw shortcode public = `0`
- `builder` mở lại được

### Nhóm B: Lỗi module native không ổn định

Ví dụ:

- `tabgroup` render lỗi
- `slider` vỡ nhịp
- `banner/text_box` hiển thị sai
- `col_inner` hoạt động không ổn trong pattern hiện tại

Cách sửa ưu tiên:

1. Đổi về syntax đã xác minh ở page khác.
2. Nếu syntax vẫn rủi ro, thay bằng `native pattern` đơn giản hơn nhưng cùng mục tiêu.
3. Không dùng HTML để che.

Ví dụ thay thế an toàn:

- `tabgroup phức tạp` -> `tabgroup đơn giản hơn` hoặc `accordion`
- `card lồng quá sâu` -> `col` hoặc `col_inner` phẳng hơn

### Nhóm C: Lỗi typography

Ví dụ:

- heading quá to
- `ux_text` + `h1/h2/h3` compound scaling
- text width quá dài
- line-height quá dày hoặc quá đặc

Cách sửa ưu tiên:

1. Giảm scale ở `ux_text` wrapper trước.
2. Giảm độ nặng semantic heading nếu cần.
3. Kiểm lại mobile trước desktop.
4. Không vá bằng CSS nếu native settings xử lý được.

### Nhóm D: Lỗi spacing và bố cục

Ví dụ:

- section quá bí hoặc quá rỗng
- card padding lệch
- mobile vỡ nhịp
- lạm dụng `gap`
- lạm dụng margin âm

Cách sửa ưu tiên:

1. Sửa `section padding`, `row`, `col padding` trước.
2. Sửa nhịp spacing hệ thống trước từng điểm lẻ.
3. Giảm số lượng `gap` dùng để vá.
4. Nếu lệch lớn, đổi structure native thay vì vá spacing.

### Nhóm E: Lỗi responsive

Ví dụ:

- vỡ ngang
- chữ rớt khung
- cột chồng bất thường
- tap target quá nhỏ

Cách sửa ưu tiên:

1. Kiểm `span__sm`, `padding__sm`, `height__sm`, `font_size__sm`.
2. Bỏ bớt phần phụ trên mobile nếu cần.
3. Ưu tiên readability hơn wow trên mobile.

### Nhóm F: Lỗi CTA / link / hành vi

Ví dụ:

- CTA không rõ
- CTA phụ lấn CTA chính
- link neo làm vỡ parser hoặc gây lỗi render

Cách sửa ưu tiên:

1. Chuyển về link an toàn đã xác minh nếu nghi parser lỗi.
2. Giữ CTA chính nổi hơn CTA phụ.
3. Kiểm lại click path sau khi save.

## Luật Ưu Tiên Khi Sửa

1. Sửa lỗi gốc trước.
2. Sửa ở file nguồn trước.
3. Ưu tiên `native setting`.
4. Ưu tiên pattern đơn giản hơn nếu pattern hiện tại không bền.
5. Không dùng HTML để che symptom.
6. Không publish khi chưa re-check xong.

## Re-check Tối Thiểu Sau Mỗi Vòng Fix

- `public` không còn lỗi cũ
- `edit` không vỡ
- `builder` mở lại được
- `mobile` không phát sinh lỗi mới
- không làm tụt `Novelty Score`
- không làm gãy `Layout DNA`

## Điều Kiện Qua Cửa Repair

Chỉ được rời bước `Repair` khi:

- mọi lỗi `blocking` đã đóng
- `Fix Pass` đã ghi rõ từng lỗi
- đã có ít nhất `1` vòng re-check sau sửa
- public không còn raw shortcode
- builder còn chỉnh sửa được
