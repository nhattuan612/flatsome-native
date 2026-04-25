# Kịch Bản Xây Dựng UI Bằng Flatsome Native Builder

Date: 2026-04-25

## Mục Đích

Đây là kịch bản vận hành tuần tự cho toàn công ty khi tạo bất kỳ UI trang web nào bằng `Flatsome UX Builder`.

Kịch bản này dùng tiếng Việt hoàn toàn và bám luật gốc:

- `section-first`
- `native-first`
- `Page Plan trước, triển khai sau`
- `public + edit + builder` đều phải kiểm

## Bộ Biểu Mẫu Chuẩn Phải Dùng

Các biểu mẫu chuẩn nằm tại:

- `VPS/docs/superpowers/flatsome-native/06-templates/`

Khi vận hành, phải ưu tiên dùng đúng các mẫu sau:

- `06-templates/Page Plan Template.md`
- `06-templates/Native Scoring Template.md`
- `06-templates/Novelty Scoring Template.md`
- `06-templates/Native Build Output Template.md`
- `06-templates/Audit Checklist Template.md`
- `06-templates/Fix Pass Template.md`
- `06-templates/Final Verification Template.md`
- `06-templates/Exception Report Template.md`
- `06-templates/Block Entry Template.md`

Toàn bộ quy tắc dùng biểu mẫu xem tại:

- `06-templates/README.md`

## Toàn Bộ Chuỗi Vận Hành

Chuỗi vận hành đầy đủ là:

`Quick Start -> Guided Intake -> Input Contract -> Chuẩn hóa brief -> Route -> Plan -> Build -> Audit -> Repair -> Release -> Lưu bài học`

Trong đó, chuỗi bắt buộc cốt lõi không được bỏ bước là:

`Plan -> Build -> Audit -> Repair -> Release`

Sau `Audit`, bắt buộc chạy thêm vòng kiểm-sửa-kiểm:

`Audit -> Classify -> Fix -> Re-check -> Re-open Builder -> Public Re-check -> Release`

Trước `Plan`, phải chạy:

- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`
- `05-flows/Brief Intake Flow.md`
- `08-design-intelligence/Design Mode Router.md`
- `03-factory/Task Route Matrix.md`
- `03-factory/Page Goal Routing.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`
- `03-factory/Layout DNA.md`
- `03-factory/Layout Pool.md`
- `03-factory/Hero Family Matrix.md`
- `03-factory/No Repeat Law.md`
- `03-factory/Section Order Recipes.md`
- `01-platform/Novelty Scoring Rule.md`
- `07-reports/Recent Page Memory.md`
- `03-factory/Section Starter Snippets.md`

## Bước 0: Chuẩn Hóa Brief

### Mục tiêu

Hiểu đúng yêu cầu trước khi lập kế hoạch.

### Việc phải làm

1. Hỏi rõ người giao việc:
   - đang đưa loại input gì
   - muốn làm trang gì
   - mục tiêu kinh doanh là gì
   - output expectation là gì
   - tone giao diện là gì
   - font mong muốn là gì
   - style mong muốn là gì
   - CTA chính là gì
   - thiết bị ưu tiên là gì
2. Ghi rõ mọi chỗ còn thiếu là `không xác định`.
3. Không được tự bịa brand, tone hay content.
4. Nếu user có đưa repo, brand guideline, website mẫu hoặc design system riêng, ghi rõ đó là `nguồn tham khảo`.
5. Nếu user không đưa chuẩn tham chiếu, được phép đề xuất hướng nhưng vẫn phải bám `Flatsome Native Core`.

### Đầu ra bắt buộc

- brief đã chuẩn hóa
- `loại input`
- `output expectation`
- `style source`
- `reference authority`
- danh sách `không xác định`
- điều kiện mặc định an toàn sẽ dùng nếu thiếu dữ liệu
- `Skeleton` đã chọn
- `Archetype` đã chọn
- `Nguồn design language tham khảo`
- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`
- `Typography direction`
- `Spacing profile`
- `Layout DNA` sơ bộ
- `Recipe` sơ bộ
- `Layout Pool` sơ bộ
- `Hero Family` sơ bộ
- `3 trang gần nhất để so`

## Bước 1: Lập Kế Hoạch

### Mục tiêu

Khóa cấu trúc trang trước khi build.

### Luật bắt buộc

- mọi trang đều phải có `Section Map`
- mọi phần đều phải nằm trong `section` và `row`
- phải chốt số lượng chính xác trước khi kéo thả

### Nội dung bắt buộc của Page Plan

- `Page Goal`
- `Page Type`
- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`
- `Section Count`
- `Layout DNA`
- `Typography direction`
- `Spacing profile`
- `Layout Pool`
- `Hero Family`
- `Recipe đã chọn`
- `Section 1`
- `Section 2`
- `Section 3`
- `Unknowns`
- `Native Elements Priority`
- `Risk Notes`
- `Tái sử dụng từ block sẵn có`

### Với mỗi section phải ghi rõ

- mục tiêu
- số `row`
- số `col` chính
- nhóm `element`

### Phải chốt thêm

- tone giao diện
- màu
- font
- motion
- design mode
- style family
- pattern family
- typography mood
- spacing rhythm
- motion profile
- anti-patterns cần tránh
- typography direction
- spacing profile
- hero title budget
- heading wrapper risk
- CTA chính
- thiết bị ưu tiên
- nguồn design language tham khảo
- lý do vì sao trang này khác trang gần nhất
- `Macro Sequence Fingerprint`
- `Similarity Risk dự kiến`
- `Novelty Score dự kiến`

### Điều cấm

- không được build khi chưa có `Page Plan`
- không được đổi cấu trúc lớn một cách tùy hứng trong lúc làm
- không được lặp nguyên recipe của trang gần nhất nếu không có lý do
- không được build nếu chưa đi qua novelty gate

### Novelty Gate Bắt Buộc

Trước khi build, phải chốt và ghi đủ:

- `Layout Pool`
- `Hero Family`
- `Dominant Geometry`
- `CTA Pattern`
- `Macro Sequence Fingerprint`
- `3 trang gần nhất đã so`
- `Similarity Risk dự kiến`
- `Novelty Score dự kiến`

Điều kiện pass novelty gate:

- `Similarity Risk` không phải `Blocked`
- `Novelty Score dự kiến >= 10`

Nếu không đạt:

- phải quay lại đổi `Layout Pool`
- hoặc đổi `Hero Family`
- hoặc đổi `Section Order Recipe`

### Đầu ra bắt buộc

- `Page Plan`
- `Section Map`
- `Novelty Scoring` bản dự kiến

## Bước 2: Triển Khai

### Mục tiêu

Build đúng plan bằng native modules của UX Builder.

### Quy tắc triển khai

1. Build đúng theo `Page Plan`.
2. Dùng tối thiểu `>=90%` native elements.
3. Tạo `section`, `row`, `col`, `row_inner`, `col_inner`, block và element theo logic của UX Builder.
4. Ưu tiên tuyệt đối `setting native`.
5. Chỉ tinh chỉnh bằng `CSS` khi native settings không đủ.
6. `CSS` phải đặt tại `Theme Options` của Flatsome.
7. `CSS` phải có comment tiếng Việt.
8. Không dùng `ux_html` làm khung layout chính.
9. `ux_html` chỉ được dùng cho:
   - `iframe`
   - `embed`
   - `link` đặc biệt
   - `map`
10. Trong lúc build phải giữ đúng `Layout DNA` và `Section Order Recipe` đã chốt, trừ khi có lý do rõ ràng.
11. Phải giữ đúng `Typography direction` và `Spacing profile` đã chốt, trừ khi có lý do rõ ràng.
12. Nếu dùng semantic heading như `h1/h2/h3` bên trong `ux_text`, không được đẩy `font_size` wrapper lên mức quá lớn.
13. Trước khi chốt page, phải kiểm public page để phát hiện `compound scaling` giữa `ux_text` và heading theme.
14. Nếu hero title vượt `Hero title budget`, phải sửa headline hoặc structure trước khi đi tiếp.
15. Không được để page pass novelty nếu `Macro Sequence Fingerprint` vẫn gần như trùng page gần nhất.

### Danh sách native elements ưu tiên

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

### Đầu ra bắt buộc

- `Native Build Output`
- `Native Scoring` bản đầu
- `Novelty Scoring` bản đầu

Các artifact phải lưu đúng chỗ theo:

- `01-platform/Artifact Storage Rule.md`

## Bước 3: Kiểm Tra

### Mục tiêu

Soát lại toàn trang ở cả mặt cấu trúc và mặt trải nghiệm người dùng.

### Hai mặt bắt buộc phải kiểm

- cấu trúc `Builder`
- giao diện `public` cho người dùng

### Checklist bắt buộc

- có thiếu `section` hay `row` không
- có thiếu `element` không
- có sai thứ bậc nội dung không
- `Layout DNA` thực tế có còn đúng với plan không
- `Layout Pool` có còn đúng với plan không
- `Hero Family` có còn đúng với plan không
- recipe có bị rơi về mô hình lặp an toàn không
- `Similarity Risk cuối` là gì
- `Novelty Score cuối` là bao nhiêu
- hierarchy chữ có còn đúng như plan không
- text width có đang quá dài không
- heading semantic có bị wrapper scale quá mức không
- spacing có gãy không
- typography có lệch không
- CTA spacing có còn rõ không
- mobile có vỡ không
- tablet có ổn không
- desktop có ổn không
- ảnh có lỗi, trống, sai tỷ lệ không
- CTA có rõ không
- shortcode/native code có lỗi không
- `UX Builder` có mở lại được không
- `UX Builder` có chỉnh sửa kéo thả lại được không
- trang `public` sau khi save có đúng không

### Đầu ra bắt buộc

- `Native Scoring` bản cuối
- `Novelty Scoring` bản cuối
- `Audit Checklist`
- danh sách lỗi đã phân loại theo nhóm

## Bước 4: Bổ Sung Và Sửa Lỗi

### Mục tiêu

Sửa toàn bộ lỗi đã phát hiện ở bước kiểm tra.

### Playbook bắt buộc

Mọi vòng sửa lỗi phải tham chiếu:

- `05-flows/Common Error Repair Playbook.md`

### Chuỗi bắt buộc trong bước này

1. `Classify lỗi`
2. `Fix lỗi gốc`
3. `Re-check đúng bề mặt đã lỗi`
4. `Re-open Builder`
5. `Public Re-check`
6. nếu còn lỗi: lặp lại bước `1 -> 5`

### Quy tắc sửa lỗi

1. Sửa tất cả lỗi đã phát hiện.
2. Mỗi lỗi phải được gán vào một `nhóm lỗi chuẩn`.
3. Ưu tiên sửa bằng `native module`.
4. Nếu một phần render kém, thay bằng `native pattern` tương đương.
5. Không được dùng HTML để che lỗi cấu trúc.
6. Nếu sau khi sửa mà bố cục lại giống trang gần nhất quá nhiều, phải đổi section hoặc recipe trước khi chốt.
7. Không được publish ngay sau khi vừa sửa xong mà chưa re-check.
8. Nếu cần ngoại lệ hiếm, phải:
   - có lý do
   - có report
   - có file/log

### Nhóm lỗi tối thiểu phải nhận diện

- `Lỗi cú pháp shortcode`
- `Lỗi module native không ổn định`
- `Lỗi typography`
- `Lỗi spacing và bố cục`
- `Lỗi responsive`
- `Lỗi CTA / link / hành vi`

### Evidence tối thiểu sau mỗi vòng fix

- lỗi cũ còn hay không
- `public` còn lỗi hay không
- `edit` còn lỗi hay không
- `builder` còn mở được không
- có phát sinh lỗi mới không

### Đầu ra bắt buộc

- `Fix Pass`

## Bước 5: Hoàn Thành

### Mục tiêu

Chỉ chốt task khi toàn bộ bề mặt đã pass.

### Điều kiện hoàn thành bắt buộc

- `public page` ổn
- `edit page` ổn
- `UX Builder` mở được
- `native structure` còn nguyên
- `Fix Pass` đã đóng mọi lỗi blocking
- `Novelty Score cuối >= 10`
- không còn lỗi lớn về `UI`, `UX`, `code`
- có `link public`
- có bằng chứng kiểm tra cuối

### Ngoại lệ hiếm ở bước hoàn thành

Chỉ được phép chốt ngoại lệ hiếm nếu:

- `public page` hoàn hảo
- `native >= 90%`
- `Codex` phê chuẩn
- có `report + file/log`

### Đầu ra bắt buộc

- `Final Verification`

### Runtime khuyến nghị

Khi task dùng shortcode file và cần gate tự động, ưu tiên chạy:

`VPS/tmp/run_flatsome_repair_gate.py`

Mục tiêu:

- lint shortcode trước khi chạm WordPress
- tạo page ở trạng thái `draft`
- preflight `edit + builder`
- chỉ publish khi preflight pass
- nếu public verify fail thì kéo page về `draft`
- tự ghi `Fix Pass` và `Final Verification`

Lưu ý:

- `Fix Pass` và `Final Verification` do runtime gate ghi ra chỉ xác nhận `surface gate`
- không được hiểu nhầm đây là `full QA pass`
- các mục như `native score`, `novelty score`, `typography`, `spacing`, `responsive` vẫn phải đi qua audit thật của task nếu cần chốt release hoàn chỉnh

## Bước 6: Lưu Bài Học

### Mục tiêu

Giữ lại tri thức tái sử dụng mà không kéo output trang cụ thể vào lớp tri thức nền tảng.

### Việc phải làm

1. Nếu phát hiện pattern native tốt, đưa vào kho tri thức phù hợp.
2. Nếu phát hiện ngoại lệ hiếm, ghi vào report hoặc log.
3. Report hoặc log của ngoại lệ phải lưu đúng vị trí chuẩn:
   - `VPS/docs/superpowers/flatsome-native/07-reports/exceptions/`
4. Tên file ngoại lệ phải theo mẫu:
   - `EX-YYYY-MM-DD-XX` + phần mở rộng .md
5. Không đưa output trang sản phẩm vào lớp tri thức nền tảng.
6. Chỉ giữ lại tri thức thật sự tái sử dụng được.

### Đầu ra gợi ý

- ghi chú nội bộ
- pattern reusable
- exception note nếu có

## Công Thức Cốt Lõi

`Plan -> Build -> Audit -> Repair -> Release`
