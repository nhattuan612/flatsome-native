# Luật Vận Hành Flatsome Native Builder

Date: 2026-04-24

## Mục Tiêu Tối Cao

Mục tiêu tối cao của toàn công ty khi tạo UI bằng `Flatsome UX Builder` là:

- `đồng nhất`
- `khả năng kéo thả chỉnh sửa về sau`

Luật tối cao duy nhất là:

- mọi UI phải đi theo `section-first`

## Phạm Vi Áp Dụng

Bộ luật này áp dụng cho:

- `Codex`
- `OpenClaw`
- mọi `worker`
- mọi `sub-agent`
- mọi nhân sự hay tiến trình tự động tham gia build UI bằng `Flatsome UX Builder`

Bộ luật này áp dụng cho `100%` mọi trang trong mọi sản phẩm và dự án dùng `Flatsome UX Builder`.

## Cấu Trúc Chuẩn Bắt Buộc

Mọi thành phần phải nằm trong cấu trúc:

`section -> row -> col -> element`

Các biến thể sau được coi là hợp lệ trong luật chính:

- `row_inner`
- `col_inner`

Quy tắc bổ sung:

- một `section` không nên chứa trực tiếp `element`
- tốt nhất mọi thành phần đi qua `row` để giữ tính responsive và dễ bảo trì
- nếu layout cần chia nhỏ, ưu tiên `chia nhiều section rõ ràng` thay vì dồn quá nhiều logic vào một section lớn

## Luật Cứng

1. Không được build theo kiểu kéo thả ngẫu hứng.
2. Không được triển khai khi chưa có `Page Plan`.
3. Không được dùng `ux_html` hoặc HTML làm khung layout chính.
4. Mục tiêu native tối thiểu là `>=90%` theo tinh thần: miễn không dùng HTML làm khung chính và phần lớn cấu trúc thật sự nằm trong native builder.
5. `ux_html` chỉ được dùng cho:
   - `iframe`
   - `embed`
   - `link` đặc biệt
   - `map`
6. `CSS` phải chèn tại `Theme Options` của Flatsome để dễ quản lý tập trung.
7. Không dùng `CSS` cục bộ tại trang như đường mặc định.
8. Mọi đoạn `CSS` thêm mới phải có comment tiếng Việt giải thích rõ mục đích.
9. Nếu thiếu dữ liệu, phải ghi rõ `không xác định`, dùng default an toàn, không được tự bịa.
10. Nếu `UX Builder` không mở lại và chỉnh sửa kéo thả được thì mặc định trang chưa đạt.
11. Kiểm tra khả năng chỉnh sửa phải thực hiện ở cả:
    - `UX Code / edit surface / builder surface`
    - `giao diện public cho người xem`
12. Mọi trang phải đi qua đủ chuỗi:
    - `Plan -> Build -> Audit -> Repair -> Release`
13. Sau `Audit`, bắt buộc phải có vòng:
    - `Classify lỗi -> Fix -> Re-check -> Re-open Builder -> Public Re-check`
14. Không được publish hoặc công khai khi chưa qua hết vòng sửa lỗi sau audit.
15. Không được báo hoàn thành khi chưa qua kiểm tra cuối.
16. Mọi ngoại lệ hiếm phải có `report + file/log` rõ ràng.
17. Mọi trang phải có `Native Scoring`.
18. Mọi trang phải có `Novelty Scoring`.
19. Không được build nếu `Similarity Risk = Blocked`.
20. Không được build nếu `Novelty Score dự kiến < 10`.
21. Không được release nếu `Novelty Score cuối < 10`.
22. Mọi page mới phải so với `3` trang gần nhất trong `07-reports/Recent Page Memory.md`.
23. Mọi `Page Plan` phải chốt `Typography direction`.
24. Mọi `Page Plan` phải chốt `Spacing profile`.
25. Mọi `Page Plan` phải chốt `Hero title budget` và `Heading wrapper risk`.
26. Mọi `Page Plan` phải chốt `Macro Sequence Fingerprint`.
27. Không được build khi chưa xác định rõ `type roles` chính của trang.
28. Không được build khi spacing còn ở mức ngẫu hứng, không có scale hoặc rhythm rõ.
29. Mọi artifact của task UI phải được lưu theo `01-platform/Artifact Storage Rule.md`.
30. Mọi `Fix Pass` phải ghi:
   - `nhóm lỗi`
   - `lỗi gốc`
   - `cách sửa`
   - `bề mặt kiểm lại`
   - `kết quả sau sửa`
31. Mọi vòng sửa lỗi sau audit phải tham chiếu:
   - `05-flows/Common Error Repair Playbook.md`

## Ưu Tiên Thiết Kế Và Triển Khai

Khi buộc phải trade-off:

- `độ giống thiết kế` và `độ native` được coi là ngang nhau
- phải `hy sinh tốc độ trước`

Quy tắc vận hành:

- ưu tiên tuyệt đối `setting native`
- chỉ dùng `CSS` sau khi đã xác nhận native settings không đủ
- nếu một phần render kém, ưu tiên thay bằng `native pattern` khác tương đương thay vì vá bằng HTML

## Luật Về Typography Và Spacing

1. Typography phải được xem là `hierarchy system`.
2. Spacing phải được xem là `token + rhythm system`.
3. Mọi trang phải chốt tối thiểu:
   - `font chính`
   - `type roles`
   - `hero title strategy`
   - `section spacing profile`
   - `card spacing profile`
   - `mobile reduction`
4. Không được để hero title, section title, body và CTA cùng một cấp cảm nhận.
5. Không được để body text quá rộng hoặc quá đặc gây khó đọc.
6. Không được dùng quá nhiều `gap` hoặc margin âm để vá bố cục.
7. Mọi quyết định typography và spacing phải ưu tiên giải bằng native structure trước.
8. Trang phải chịu được logic `text spacing accessibility` ở mức hợp lý; nếu tăng spacing mà vỡ nặng thì coi như chưa bền.

## Luật Về Ngôn Ngữ Thiết Kế

1. `Flatsome Native Core` là gốc mặc định của công ty.
2. `111 Full Page` của `Flatsome Studio` là lớp tham chiếu native quan trọng nhất về bố cục và pattern.
3. Mọi repo hoặc design system bên ngoài chỉ là `tham khảo`.
4. Không được biến một repo ngoài thành luật mặc định của công ty.
5. Nếu user đưa một chuẩn thiết kế riêng, phải dịch nó về `section-first` và `native-first`.
6. Nếu user không đưa chuẩn riêng, được phép đề xuất nguồn tham khảo nhưng không được ép.
7. `Độ chuyên nghiệp` không được đánh đổi bằng việc phá vỡ khả năng mở lại của UX Builder.

## Luật Chống Lặp

1. Nếu user không yêu cầu lặp lại, mặc định trang mới phải khác trang gần nhất về bố cục.
2. Không được chỉ đổi màu, đổi ảnh, đổi chữ rồi giữ nguyên khung.
3. Trước khi build phải chốt:
   - `Layout DNA`
   - `Layout Pool`
   - `Hero Family`
   - `Section Order Recipe`
4. Nếu lặp mạnh bố cục cũ, phải ghi lý do vào `Page Plan`.
5. `No Repeat Law` là `hard gate`.
6. Các chuỗi `safe pattern` đã bị ghi nhận trong `07-reports/Recent Page Memory.md` không được phép lặp thêm.
7. Nếu trang mới lặp `3/4` trục trọng yếu sau đây với trang gần nhất thì mặc định fail:
   - `Hero Family`
   - `Section Order`
   - `Dominant Geometry`
   - `CTA Pattern`
8. Nếu `Macro Sequence Fingerprint` của trang mới gần như trùng page gần nhất, phải coi đây là lỗi novelty thật dù màu và content đã đổi.

## Native Elements Ưu Tiên

Danh sách native elements ưu tiên của công ty:

- `section`
- `row`
- `col`
- `row_inner`
- `col_inner`
- `Slider`
- `Block/Grid`
- `Page Header`
- `Stack`
- `Widget Area`
- `Button`
- `Lottie`
- `Menu`
- `Navigation`
- `Text`
- `Banner`
- `Accordion`
- `Blog Posts`
- `Countdown`
- `Divider`
- `Follow Icons`
- `Form (CF7)`
- `Gallery`
- `Gap`
- `Icon Box`
- `Image`
- `Image Box`
- `Instagram Feed`
- `Logo`
- `Map`
- `Message Box`
- `Pages`
- `Price Table`
- `Scroll To`
- `Search Box`
- `Share Icons`
- `Tabs`
- `Team Member`
- `Testimonial`
- `Title`
- `Video`
- `Video Button`
- `WP Gallery`

## Luật Về Block

1. Mọi section lặp lại từ `2 lần` trở lên phải tách thành `UX Block`, trừ khi đã được ghi rõ là ngoại lệ hiếm.
2. Hướng ưu tiên là `UX Blocks reusable`.
3. Khi hợp lý, block nên được nâng lên thành `block thư viện công ty`.
4. Reuse block phải được ghi rõ trong `Page Plan` bằng tiếng Việt.

## Luật Về Quyền Hạn

- `Codex` là người quyết định cuối.
- `OpenClaw` và các worker khác chỉ là lớp thực thi phụ trợ khi cần.
- Ngoại lệ hiếm chỉ được chấp nhận khi:
  - có lý do rõ ràng
  - có report
  - có file/log
  - và không phá vỡ mục tiêu tối cao của hệ thống

## Chính Sách Ngoại Lệ Hiếm

Ngoại lệ hiếm chỉ được cân nhắc khi đồng thời thỏa cả 3 điều kiện:

- `public page` hoàn hảo
- `native >= 90%`
- `Codex` chấp thuận

Nếu có ngoại lệ hiếm:

- phải ghi rõ lý do
- phải ghi rõ phần nào không đạt chuẩn mặc định
- phải có `report + file/log`
- không được dùng ngoại lệ như đường tắt mặc định

## Luật Về Giao Tiếp

Trước khi build, phải hỏi và chốt rõ với người giao việc ít nhất các điểm sau:

- muốn làm trang gì
- mục tiêu gì
- tone gì
- font gì
- style gì
- CTA chính là gì
- thiết bị ưu tiên là gì

Chỉ sau khi `Page Plan` đã rõ ràng mới được triển khai.

## Chuẩn Đầu Ra Bắt Buộc

Mỗi task UI phải có đủ:

- `Page Plan`
- `Section Map`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

Các artifact này phải lưu đúng chỗ theo:

- `01-platform/Artifact Storage Rule.md`

## Điều Kiện Hoàn Thành

Một trang chỉ được xem là hoàn thành khi:

- `public page` ổn
- `edit page` ổn
- `UX Builder` mở được
- `native structure` còn nguyên
- không còn lỗi lớn về `UI`, `UX`, `code`
- có `link public`
- có bằng chứng kiểm tra cuối

## Công Thức Vận Hành Chung

`Plan -> Build -> Audit -> Repair -> Release`
