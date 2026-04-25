# Official Demo Surface Ingestion Report

Date: 2026-04-24

## Trạng thái

`PASS: official demo surfaces reviewed and ingested selectively`

## Phạm vi đã quét

Đã quét từ entry:

- https://demos.flatsome.com/features/ux-page-builder/

Đã đi qua các nhóm menu chính để xác định phần nào thật sự bổ sung tri thức:

- `DEMOS`
- `FEATURES`
- `SHOP`
- `PAGES`
- `BLOG`
- `ELEMENTS`

## Nguồn chính đã dùng

### Feature-level sources

- https://demos.flatsome.com/features/ux-page-builder/
- https://demos.flatsome.com/features/elements-overview/
- https://demos.flatsome.com/features/blocks-element/
- https://demos.flatsome.com/features/header-designer/
- https://demos.flatsome.com/features/footer-features/
- https://demos.flatsome.com/features/blog-features/
- https://demos.flatsome.com/features/portfolio-features/
- https://demos.flatsome.com/features/whats-new/

### Element-level sources

- https://demos.flatsome.com/elements/sections/
- https://demos.flatsome.com/elements/rows-columns/
- https://demos.flatsome.com/elements/galleries/
- https://demos.flatsome.com/elements/lightbox/
- https://demos.flatsome.com/elements/message-box/
- https://demos.flatsome.com/elements/instagram-feed/
- https://demos.flatsome.com/elements/search-box/
- https://demos.flatsome.com/elements/forms/
- https://demos.flatsome.com/elements/price-table/
- https://demos.flatsome.com/elements/pages/
- https://demos.flatsome.com/elements/portfolio/
- https://demos.flatsome.com/elements/map/
- https://demos.flatsome.com/elements/product-categories/
- https://demos.flatsome.com/elements/products/
- https://demos.flatsome.com/elements/team-member/
- https://demos.flatsome.com/elements/tabs/
- https://demos.flatsome.com/elements/hotspot/
- https://demos.flatsome.com/elements/flip-book/

### Demo/page-family sources

- https://demos.flatsome.com/shop/
- https://demos.flatsome.com/demos/shop-demos/classic-shop/
- https://demos.flatsome.com/demos/shop-demos/big-sale/
- https://demos.flatsome.com/demos/shop-demos/sale-countdown/
- https://demos.flatsome.com/demos/business-demos/agency/
- https://demos.flatsome.com/demos/business-demos/simple-corporate/
- https://demos.flatsome.com/demos/business-demos/explore/

## Những gì thực sự đáng nạp

### 1. Official source layer mới

Đã xác nhận cần thêm `official Flatsome demo surfaces` như một lớp nguồn riêng, nằm giữa:

- `official docs`
- `verified local extraction`

Giá trị của lớp này:

- xác nhận một element/surface có tồn tại thật trong hệ Flatsome
- xác nhận một pattern là một phần của ngôn ngữ trình bày chính thức
- xác nhận một page family là native-friendly

Giới hạn của lớp này:

- không đồng nghĩa với full shortcode syntax map
- không đồng nghĩa với full parameter coverage

### 2. Officially confirmed native surfaces

Các surface được bổ sung vào knowledge hub theo dạng:

- `confirmed`
- `operating value`
- `syntax capture pending` nếu chưa có capture đủ chắc

Nhóm đáng giữ:

- `lightbox`
- `hotspot`
- `flip book`
- `video button`
- `message box`
- `forms`
- `search box`
- `tabs`
- `map`
- `price table`
- `team member`
- `portfolio`
- `logo`

Sau bước capture syntax tiếp theo, các surface đã lên mức `syntax-complete` trong hub:

- `lightbox`
- `video_button`
- `map`
- `tabgroup`
- `tab`
- `team_member`
- `ux_portfolio`
- `logo`

Các surface vẫn đang `syntax capture pending`:

- `hotspot`
- `flip book`
- `message box`

Một số tín hiệu vận hành đáng giữ thêm:

- `forms` trên official demo gắn với `Contact Form 7 presets`
- `blog_posts` được official demo cho thấy dùng được theo `slider / row / grid / masonry`
- `block` được official demo xác nhận dùng cho:
  - `custom blog header`
  - `custom shop header`
  - `shop category headers`
  - `footer widgets`
  - `footer replace`
- `price table` hiện được hiểu là `native composition pattern`, chưa có bằng chứng shortcode riêng trong harvested exports

### 3. Pattern-level knowledge

Các pattern có giá trị sản xuất rõ ràng:

- `lookbook / hotspot storytelling`
- `footer replacement via reusable block`
- `editorial posts slider / teaser rail`
- `shop hero + category discovery band`
- `utility section with message/search/form surface`

### 4. Effect/surface confirmations ngoài data harvest

Đã bổ sung nhóm xác nhận chính thức ngoài `337 export` harvest:

- `sticky section`
- `section masks`
- `lightbox behavior`
- `hotspot interaction`
- `flip book interaction`
- `video button surface`

## Những gì không nạp vào platform layer

Đã cố ý không nạp:

- brand copy của từng demo page
- toàn bộ catalogue demo page dưới dạng mô tả dài
- chi tiết trang cụ thể không có giá trị tái sử dụng
- syntax bịa cho element chưa capture chắc

## File đã cập nhật

- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/01-Overview and Source Rules.md`
- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`
- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/04-Commerce and Dynamic.md`
- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/05-Aliases and Broad Surface.md`
- `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/06-Patterns and Workflow.md`
- `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/Effects.md`
- `VPS/docs/superpowers/flatsome-native/03-factory/Section Archetypes.md`
- `VPS/docs/superpowers/flatsome-native/03-factory/Composition Rules.md`

## Kết luận vận hành

Sau đợt này, knowledge hub mạnh hơn ở 3 điểm:

- hiểu rõ hơn `Flatsome native surface` do demo chính thức xác nhận
- hiểu rõ hơn `pattern nào là hàng chính hãng của Flatsome`
- giảm nguy cơ đánh giá thấp Builder rồi rơi vào HTML quá sớm
