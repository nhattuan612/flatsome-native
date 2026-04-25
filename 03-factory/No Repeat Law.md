# No Repeat Law

Date: 2026-04-24

## Mục Đích

Luật này tồn tại để chống việc nhiều trang khác nhau nhưng lại rơi về cùng một bố cục an toàn.

Từ nay đây là `hard gate`, không còn là nhắc nhở mềm.

Mặc định của công ty là:

- nếu user không yêu cầu lặp lại
- thì trang mới `phải khác` trang gần nhất về bố cục

## Luật Cứng

1. Không được lặp nguyên `section order` của trang gần nhất.
2. Không được lặp nguyên `hero family` của trang gần nhất.
3. Không được lặp nguyên `CTA pattern` của trang gần nhất.
4. Không được chỉ đổi màu, đổi chữ, đổi ảnh rồi gọi đó là trang mới.
5. Nếu cùng brief, cùng brand, cùng tone mà user không dặn giữ layout, vẫn phải tạo biến thể bố cục mới.
6. Trước khi build phải so với `3` trang gần nhất trong `07-reports/Recent Page Memory.md`.
7. Nếu `Similarity Risk = Blocked` thì không được build.
8. Nếu `Novelty Score dự kiến < 10` thì không được build.
9. Không được chỉ đổi `skin` mà giữ nguyên `Macro Sequence Fingerprint`.

## Những Thứ Phải Khác Theo Mặc Định

Tối thiểu phải đổi `3` lớp sau:

- `hero family`
- `section order`
- `dominant geometry`
- `content density`
- `proof pattern`
- `CTA pattern`
- `image treatment`
- `motion profile`
- `macro sequence fingerprint`

## Những Thứ Có Thể Giữ

Có thể giữ khi cùng brand:

- font
- tone màu
- cảm giác thương hiệu
- mức độ sang trọng / trẻ trung / corporate / editorial

## Trường Hợp Được Phép Lặp

Chỉ được phép lặp mạnh nếu có một trong các lý do:

- user yêu cầu rõ `giữ layout cũ`
- đây là biến thể A/B rất gần nhau
- đây là template system có chủ đích đồng bộ
- block chuẩn công ty cần tái dùng đúng nguyên bản

Nếu lặp:

- phải ghi lý do trong `Page Plan`
- phải ghi vào `report` nếu mức lặp cao

## Dấu Hiệu Vi Phạm

Nếu trang mới lại rơi về mô hình quá quen thuộc như:

- `hero -> 3 card benefits -> split image/text -> testimonial -> CTA`
- `hero lớn -> feature grid -> gallery -> form close`
- `hero slider -> stats -> services -> blog -> CTA`

thì phải dừng lại và đổi `recipe`.

## Cách Tránh Lặp

1. đổi `Layout DNA`
2. đổi `Section Order Recipe`
3. đổi `proof pattern`
4. đổi `hero family`
5. đổi `dominant geometry`
6. đổi cách phân bố CTA
7. đổi `Layout Pool`

## Quy Tắc Kiểm Tra Trước Khi Build

Trước khi build phải tự hỏi:

- trang gần nhất dùng hero gì
- trang gần nhất dùng recipe gì
- trang gần nhất dùng CTA pattern gì
- trang gần nhất dùng `Layout Pool` gì
- trang gần nhất dùng `Macro Sequence Fingerprint` gì
- lần này đổi tối thiểu 3 lớp chưa
- `Novelty Score dự kiến` là bao nhiêu
- `Similarity Risk` có bị block không

Nếu chưa:

- chưa được triển khai

## Quy Tắc Kiểm Tra Sau Khi Build

Sau khi build phải tự audit:

- người xem có cảm thấy đây là trang khác thật không
- section order có khác không
- nhịp nội dung có khác không
- điểm nhấn thị giác có khác không
- `Novelty Score cuối` có đạt ngưỡng pass không
- có đang rơi lại vào `safe pattern` bị cấm không

## File Bắt Buộc Phải Mở Cùng

- `03-factory/Layout DNA.md`
- `03-factory/Layout Pool.md`
- `03-factory/Hero Family Matrix.md`
- `03-factory/Section Order Recipes.md`
- `01-platform/Novelty Scoring Rule.md`
- `07-reports/Recent Page Memory.md`

## Kết Luận

`No Repeat Law` không cấm tái dùng tri thức.

Nó chỉ cấm:

- tái dùng `bố cục` một cách lười biếng
- tái dùng `cảm giác trang` quá giống nhau
- tái dùng `safe pattern` khi đã có bằng chứng lặp
