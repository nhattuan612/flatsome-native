# Typography System

Date: 2026-04-24

## Mục Đích

Tài liệu này chuẩn hóa cách `học`, `chọn`, `dịch`, và `kiểm` typography cho mọi trang build bằng `Flatsome Native Builder`.

Mục tiêu:

- hierarchy chữ rõ
- đọc nhanh
- hợp tone
- mở lại chỉnh sửa được bằng `UX Builder`
- không phải vá layout bằng HTML

## Nguồn Học Gốc

- Atlassian Typography:
  - `https://atlassian.design/foundations/typography/`
- IBM Carbon Typography:
  - `https://carbondesignsystem.com/elements/typography/overview/`
- W3C Text Spacing:
  - `https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html`

## Luật Cốt Lõi

1. Typography là `hệ phân cấp`, không phải chỉ là chọn font.
2. Mỗi trang phải chốt `type roles` trước khi build.
3. Không tăng giảm cỡ chữ theo cảm tính từng section.
4. Ưu tiên `setting native` của Flatsome trước.
5. Nếu không thể mô tả hierarchy chữ bằng `section -> row -> col -> element`, chứng tỏ plan chưa rõ.

## Type Roles Bắt Buộc Phải Nghĩ

Khi lập `Page Plan`, phải chốt tối thiểu các vai trò sau:

- `Display / Hero Title`
- `Hero Lead / Subheadline`
- `Section Title`
- `Section Lead`
- `Body`
- `Meta / Caption / Label`
- `Button Text`

Nếu trang giàu nội dung hơn, có thể thêm:

- `Card Title`
- `Card Body`
- `Statistic Number`
- `Eyebrow`
- `Testimonial Quote`

## Quy Tắc Phân Cấp

### 1. Một màn hình đầu không nên có quá nhiều cấp chữ

Mặc định an toàn:

- tối đa `3` cấp rõ ràng trong cùng một viewport đầu
- `1` tiêu đề chính
- `1` mô tả hỗ trợ
- `1` CTA rõ

### 2. Hero title phải lớn hơn section title một bậc rõ ràng

Nếu người xem không quét mắt ra được đâu là tiêu đề mạnh nhất, hierarchy đang fail.

### 3. Body copy không được dài và đặc quá mức

Mặc định:

- đoạn ngắn: `1-3` câu
- đoạn mô tả chuẩn: `2-4` dòng
- đoạn dài chỉ dùng khi trang cần giải thích sâu

### 4. Button text phải là cấp hành động, không được chìm

Nút bấm có thể nhỏ hơn title, nhưng không được yếu hơn text nền xung quanh.

## Guardrails Khả Dụng

### Chiều dài dòng

- body lý tưởng:
  - khoảng `45-75` ký tự mỗi dòng
- text quá dài ngang full viewport thường phải giảm width hoặc chia lại layout

### Line-height

- heading:
  - khoảng `1.1 - 1.3`
- body:
  - khoảng `1.5 - 1.8`

### Text spacing accessibility

Trang phải chịu được logic override gần với WCAG:

- `line-height >= 1.5`
- `paragraph spacing >= 2x`
- `letter spacing >= 0.12x`
- `word spacing >= 0.16x`

Nếu tăng spacing hợp lý mà layout vỡ mạnh, typography chưa bền.

## Chọn Font Theo Vai Trò, Không Theo Cảm Tính

Khi chốt font, phải trả lời:

- font này cho cảm giác gì
- hợp với `tone` nào
- heading và body có khác nhau rõ không
- mobile có còn đọc dễ không
- tiếng Việt có hiển thị sạch không

## Hướng Font Theo Tone

- `hiện đại / sáng / startup`
  - ưu tiên sans sạch, ít trang trí
- `premium / editorial / sang`
  - có thể dùng serif cho heading, sans cho body
- `enterprise / kỹ thuật / rõ việc`
  - ưu tiên hierarchy ổn định, body đọc bền
- `thân thiện / lifestyle / consumer`
  - ưu tiên rounded hoặc humanist sans nhưng vẫn giữ độ rõ

## Dịch Sang Flatsome Native

Typography phải được map vào các surface native sau:

- `title`
- `text`
- `ux_text`
- `banner` + `text_box`
- `button`
- `message_box`
- `icon_box`
- `featured_box`
- `tabs`
- `accordion`

## Thứ Tự Chỉnh Typography Trong Flatsome

1. chọn `role` của đoạn chữ
2. đặt đúng `element` native
3. chỉnh `font size`
4. chỉnh `line height`
5. chỉnh `text align`
6. chỉnh `max width` bằng layout native
7. chỉ sau cùng mới cân nhắc `CSS`

## Luật Không Được Làm

- không dùng `ux_html` để dựng typography shell
- không dùng quá nhiều cỡ chữ lẻ
- không để hero title, section title, card title gần như cùng một cấp
- không nhét quá nhiều text vào một banner chỉ vì còn chỗ
- không dùng in hoa dài cho cả đoạn nội dung
- không bọc `h1/h2/h3` trong `ux_text font_size` quá lớn rồi mong Flatsome tự cân lại
- không dùng `ux_text` cỡ lớn như `3.x - 4.x` để ôm heading semantic, vì wrapper sẽ nhân thêm scale của heading và rất dễ vỡ khung

## Cảnh Báo Compound Scaling

Khi một heading semantic như `h1`, `h2`, `h3` nằm bên trong `[ux_text font_size=\"...\"]`, cỡ chữ thực tế có thể bị `nhân tầng`:

- `font_size` của wrapper
- scale mặc định của heading trong theme
- line-height của heading

Kết quả là nhìn trong shortcode có vẻ hợp lý nhưng khi render public lại phình quá lớn.

Quy tắc an toàn:

- nếu dùng `h1/h2/h3` bên trong `ux_text`, giữ wrapper ở mức vừa phải, thường quanh `1.3 - 1.8`
- nếu muốn display cực lớn, ưu tiên test trực tiếp ở public page trước khi chốt
- nếu chỉ cần chữ lớn mang tính trang trí, cân nhắc `title` hoặc text không semantic thay vì đẩy semantic heading lên quá mức

## Hero Title Budget Guardrail

Mọi `Page Plan` phải chốt thêm:

- `Hero title budget`
- `Hero title expected line count`
- `Heading wrapper risk`
- `Hero title fallback`

### Budget an toàn mặc định

#### Hero cột hẹp hoặc split hero (`5/12` tới `6/12`)

- soft budget:
  - `40-55` ký tự
- hard budget:
  - `70` ký tự
- desktop:
  - mục tiêu `2` dòng
- mobile:
  - mục tiêu `3` dòng

#### Hero cột rộng hoặc full-width statement

- soft budget:
  - `55-75` ký tự
- hard budget:
  - `95` ký tự
- desktop:
  - mục tiêu `2-3` dòng
- mobile:
  - mục tiêu `3-4` dòng

### Heading wrapper risk

Nếu dùng `h1/h2/h3` bên trong `ux_text`, phải tự chấm:

- `Low`
  - wrapper `<= 1.6`
- `Medium`
  - wrapper `1.7 - 1.8`
- `High`
  - wrapper `1.9 - 2.1`
- `Blocked`
  - wrapper `> 2.1`

Nếu `Heading wrapper risk = High`:

- phải có lý do rõ
- phải kiểm public sớm
- phải có fallback trước khi build tiếp

Nếu `Heading wrapper risk = Blocked`:

- không được build nguyên trạng

### Fallback bắt buộc khi vượt budget

Nếu hero title vượt budget hoặc có đồng thời:

- cột hero hẹp
- text dài
- wrapper scale cao

thì phải chọn ít nhất `1` hướng:

- rút ngắn headline
- tách thành `eyebrow + title + lead`
- giảm wrapper scale
- tăng chiều rộng cột hero
- đổi sang `title` hoặc native surface khác hợp vai hơn

## Checklist Nhanh Trước Khi Build

- đã chốt `font chính`
- đã chốt `tone chữ`
- đã chốt `type roles`
- đã biết `hero title` khác `section title` ở đâu
- đã chốt `Hero title budget`
- đã chốt `Heading wrapper risk`
- đã biết body sẽ ngắn hay dài
- đã biết CTA text sẽ mạnh đến mức nào

## Checklist Audit Typography

- hierarchy có nhìn ra trong `3 giây` không
- title chính có thật sự là mạnh nhất không
- hero title có nằm trong budget đã chốt không
- hero title có vượt số dòng mobile đã chốt không
- body có đọc thoáng không
- mobile có bị nhỏ và dày quá không
- CTA có bị chìm giữa nhiều text không
- card title và body có cùng cấp vô thức không
- text có bị kéo quá rộng không

## Kết Luận

Typography trong hệ này là:

- `role-first`
- `hierarchy-first`
- `readability-first`
- `native-first`

Không được xem typography chỉ là chuyện `đổi font`.
