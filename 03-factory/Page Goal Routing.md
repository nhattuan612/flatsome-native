# Page Goal Routing

Date: 2026-04-24

## Mục Đích

Tài liệu này tồn tại để route một brief mới theo tuyến ngắn và ổn định:

`Loại trang -> Mục tiêu chính -> Skeleton -> Archetype ưu tiên -> Ứng viên block -> Native build`

Không được nhảy thẳng vào kéo thả khi chưa đi qua route này.

## Luật Route

1. chốt `Loại trang`
2. chốt `Mục tiêu chính`
3. chọn `Skeleton`
4. chọn `Archetype ưu tiên`
5. kiểm tra `Ứng viên block` trong `03-factory/Block Library Candidates.md`
6. chốt `reuse decision` với `03-factory/Block Registry.md`
7. mới lập `Section Map`

## Gói Bàn Giao Factory Bắt Buộc

Trước khi rời file này để sang `Page Plan`, worker phải chốt được:

- `Skeleton đã chọn`
- `Archetype ưu tiên`
- `Ứng viên block nên tái dùng`
- `Ứng viên block nên tạo mới`
- `Reuse decision`
- `Section starter direction`

Nếu task đang ở `Design Mode` khác `Flatsome Default`, phải chốt thêm:

- `Design Mode`
- `Style family`
- `Pattern family`

Nguồn đối chiếu:

- `03-factory/Design Language Reference.md`
- `03-factory/Section Starter Snippets.md`
- `03-factory/Block Library Candidates.md`
- `03-factory/Block Registry.md`

## Routing Table

### 1. Landing page chuyển đổi

- `Loại trang:`
  - landing
- `Mục tiêu chính:`
  - chuyển đổi
  - lead capture
  - sales push
- `Skeleton nên dùng:`
  - `Landing page`
- `Archetype ưu tiên:`
  - `Hero: slider + side CTA`
  - `Feature grid`
  - `Testimonial + logo proof rail`
  - `CTA block`
  - `Contact / signup section`
- `Ứng viên block:`
  - hero
  - proof rail
  - CTA close
- `Risk note:`
  - dễ nhồi quá nhiều section; phải giữ CTA chính thật rõ

### 2. About / thương hiệu

- `Loại trang:`
  - about
  - brand story
- `Mục tiêu chính:`
  - giới thiệu
  - tăng tin cậy
- `Skeleton nên dùng:`
  - `About page`
- `Archetype ưu tiên:`
  - `Hero: offset image + text card`
  - `Gallery: staggered image strip`
  - `Team roster grid`
  - `Testimonial + logo proof rail`
- `Ứng viên block:`
  - story split
  - team grid
  - proof band
- `Risk note:`
  - dễ bị kể chuyện lan man; phải giữ hierarchy nội dung rõ

### 3. Recruitment / hiring

- `Loại trang:`
  - tuyển dụng
  - careers
- `Mục tiêu chính:`
  - thu hút ứng viên
  - thể hiện văn hóa
- `Skeleton nên dùng:`
  - `Recruitment page`
- `Archetype ưu tiên:`
  - `Hero: offset image + text card`
  - `Feature grid`
  - `Team roster grid`
  - `Testimonial + logo proof rail`
  - `Contact / signup section`
- `Ứng viên block:`
  - culture/value grid
  - team row
  - apply CTA
- `Risk note:`
  - đừng biến thành about page; phải giữ CTA ứng tuyển rõ

### 4. Ecommerce landing

- `Loại trang:`
  - ecommerce
  - shop landing
- `Mục tiêu chính:`
  - đẩy danh mục
  - đẩy sản phẩm
- `Skeleton nên dùng:`
  - `Ecommerce landing`
- `Archetype ưu tiên:`
  - `Content commerce / product block`
  - `Shop hero + category discovery band`
  - `Instagram / social proof strip`
  - `Video trigger banner`
- `Ứng viên block:`
  - category rail
  - product rail
  - newsletter strip
- `Risk note:`
  - dễ lẫn giữa page builder và archive logic; phải kiểm sản phẩm lấy từ đâu

### 5. Editorial / blog home

- `Loại trang:`
  - blog
  - insights
  - newsroom
- `Mục tiêu chính:`
  - tăng authority
  - dẫn traffic đọc tiếp
- `Skeleton nên dùng:`
  - `Editorial / blog homepage`
- `Archetype ưu tiên:`
  - `Editorial posts / insights rail`
  - `Testimonial + logo proof rail`
  - `CTA block`
- `Ứng viên block:`
  - featured posts rail
  - newsletter band
  - proof strip
- `Risk note:`
  - đừng chỉ dùng default post grid; phải chọn style phù hợp mục tiêu

### 6. Contact page

- `Loại trang:`
  - contact
  - locations
- `Mục tiêu chính:`
  - nhận liên hệ
  - thể hiện hiện diện địa phương
- `Skeleton nên dùng:`
  - `Contact page`
- `Archetype ưu tiên:`
  - `Contact split with map`
  - `Tabbed FAQ / pricing panel`
  - `CTA block`
- `Ứng viên block:`
  - contact split
  - office info row
  - faq strip
- `Risk note:`
  - phải kiểm mobile stacking giữa form và map

### 7. Portfolio / case-study landing

- `Loại trang:`
  - portfolio
  - case-study
  - showcase
- `Mục tiêu chính:`
  - chứng minh năng lực
  - dẫn sang project detail
- `Skeleton nên dùng:`
  - `Portfolio / case-study landing`
- `Archetype ưu tiên:`
  - `Portfolio showcase rail`
  - `Testimonial + logo proof rail`
  - `CTA block`
- `Ứng viên block:`
  - portfolio rail
  - case-study teaser
  - proof band
- `Risk note:`
  - phải giữ tỷ lệ ảnh và nhịp CTA ổn định

### 8. Service / agency page

- `Loại trang:`
  - service
  - agency
- `Mục tiêu chính:`
  - giải thích dịch vụ
  - tăng trust
  - tạo lead
- `Skeleton nên dùng:`
  - `Service / agency page`
- `Archetype ưu tiên:`
  - `Feature grid`
  - `Portfolio showcase rail`
  - `Testimonial + logo proof rail`
  - `Contact split with map`
- `Ứng viên block:`
  - services grid
  - proof rail
  - contact split
- `Risk note:`
  - dễ trùng với landing; cần giữ phần giải thích rõ hơn

### 9. Pricing / FAQ page

- `Loại trang:`
  - pricing
  - faq
  - membership
- `Mục tiêu chính:`
  - giải thích gói
  - xử lý phản đối
- `Skeleton nên dùng:`
  - `Pricing / FAQ page`
- `Archetype ưu tiên:`
  - `Tabbed FAQ / pricing panel`
  - `Testimonial + logo proof rail`
  - `CTA block`
- `Ứng viên block:`
  - tabs panel
  - faq accordion cluster
  - pricing close CTA
- `Risk note:`
  - đừng bịa shortcode riêng cho price table khi chưa có chứng cứ

## Quy Tắc CEO

- nếu brief mới không route được vào một skeleton rõ ràng, phải tách lại brief trước khi build
- nếu một page cần nhiều hơn `2` skeleton chính, khả năng brief đang quá loãng
- nếu đã có archetype phù hợp mà vẫn dựng từ đầu, đó là dấu hiệu vận hành kém
- nếu archetype đã có ứng viên `P1` trong `03-factory/Block Library Candidates.md`, phải cân nhắc tái dùng trước khi tạo block mới
