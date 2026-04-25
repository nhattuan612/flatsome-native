# Section Starter Snippets

Date: 2026-04-24

## Mục Đích

Đây là file khởi động nhanh từ `Archetype` sang `shortcode-native`.

Nó không thay `Page Plan`.
Nó không thay `Section Map`.
Nó chỉ giúp bắt đầu nhanh hơn sau khi route đã chốt.

## Luật Dùng

- chỉ dùng sau `Brief Intake Flow`
- chỉ dùng sau khi đã chọn `Skeleton` và `Archetype`
- được phép đổi copy, ảnh, spacing, màu, CTA
- không được đổi cấu trúc lớn một cách ngẫu hứng
- không được thêm HTML để làm khung layout

## 1. Hero: Slider + Side CTA

### Dùng khi nào

- landing
- campaign
- recruitment
- sales push

### Khung native

```txt
[section label="Hero" padding="0px"]

[row style="collapse" width="full-width"]

[col span="12" span__sm="12"]

[row_inner style="collapse" width="full-width" v_align="middle"]

[col_inner span="8" span__sm="12"]
[ux_slider]
[ux_banner height="680px" height__sm="420px" bg="IMAGE_ID_1"]
[text_box position_x="50" position_y="50"]
<h2>Hero title</h2>
Hero description
[button text="CTA chính" color="secondary"]
[/text_box]
[/ux_banner]
[ux_banner height="680px" height__sm="420px" bg="IMAGE_ID_2"]
[text_box position_x="50" position_y="50"]
<h2>Slide title</h2>
Slide description
[/text_box]
[/ux_banner]
[/ux_slider]
[/col_inner]

[col_inner span="4" span__sm="12" padding="32px 32px 32px 32px" bg_color="rgb(255,255,255)"]
[ux_text font_size="1.6"]
<h3>CTA phụ trợ</h3>
Nội dung hỗ trợ chuyển đổi.
[/ux_text]
[divider width="80px" height="3px"]
[button text="Hành động" color="secondary" radius="6"]
[/col_inner]

[/row_inner]

[/col]

[/row]

[/section]
```

### Biến chính

- `bg`
- `height`
- copy hero
- CTA chính
- CTA phụ trợ

## 2. Hero: Offset Image + Text Card

### Dùng khi nào

- about
- recruitment
- service intro

### Khung native

```txt
[section label="Hero Intro" padding="70px" padding__sm="30px"]

[row h_align="right"]
[col span="10" span__sm="12"]
[ux_banner height="560px" height__sm="320px" bg="IMAGE_ID"]
[text_box style="display:none;" visibility="hidden"]
[/text_box]
[/ux_banner]
[/col]
[/row]

[row]
[col span="5" span__sm="12" padding="8% 6% 6% 6%" margin="-320px 0px 0px 0px" margin__sm="20px 0px 0px 0px" bg_color="rgba(255,255,255,0.92)"]
[ux_text font_size="2.4" line_height="1.1"]
<h2>Khối nội dung chính</h2>
[/ux_text]
Mô tả mở đầu của section.
[button text="CTA chính" color="secondary" style="underline"]
[/col]
[/row]

[/section]
```

### Biến chính

- ảnh nền
- mức offset
- tỷ lệ card
- heading scale

## 3. Feature Grid

### Dùng khi nào

- benefits
- services
- differentiators

### Khung native

```txt
[section label="Feature Grid" padding="70px" padding__sm="40px"]

[row h_align="center"]
[col span="8" span__sm="12" align="center"]
[title style="center" text="Điểm nổi bật"]
[gap height="12px"]
[ux_text font_size="1.1"]
Mô tả ngắn cho section.
[/ux_text]
[/col]
[/row]

[row]
[col span="12"]
[row_inner]

[col_inner span="4" span__sm="12" padding="30px 30px 30px 30px" bg_color="rgb(255,255,255)" depth="2"]
[featured_box img="ICON_ID_1" img_width="48" pos="center"]
<h3>Feature 1</h3>
Mô tả feature.
[/featured_box]
[/col_inner]

[col_inner span="4" span__sm="12" padding="30px 30px 30px 30px" bg_color="rgb(255,255,255)" depth="2"]
[featured_box img="ICON_ID_2" img_width="48" pos="center"]
<h3>Feature 2</h3>
Mô tả feature.
[/featured_box]
[/col_inner]

[col_inner span="4" span__sm="12" padding="30px 30px 30px 30px" bg_color="rgb(255,255,255)" depth="2"]
[featured_box img="ICON_ID_3" img_width="48" pos="center"]
<h3>Feature 3</h3>
Mô tả feature.
[/featured_box]
[/col_inner]

[/row_inner]
[/col]
[/row]

[/section]
```

### Biến chính

- số cột
- icon/image
- độ nổi khối
- màu nhấn

## 4. CTA Block

### Dùng khi nào

- close section
- lead capture
- cuối trang

### Khung native

```txt
[section label="CTA" padding="0px"]

[row]
[col span="12"]
[ux_banner height="420px" height__sm="300px" bg="IMAGE_ID"]
[text_box position_x="50" position_y="50"]
<h2>CTA headline</h2>
Nội dung chốt hành động.
[button text="CTA chính" color="secondary" radius="6"]
[/text_box]
[/ux_banner]
[/col]
[/row]

[/section]
```

### Biến chính

- background
- overlay/tone
- CTA copy

## 5. Contact Split With Map

### Dùng khi nào

- contact
- service
- location presence

### Khung native

```txt
[section label="Contact Split" padding="70px" padding__sm="35px"]

[row v_align="middle"]

[col span="5" span__sm="12" padding="20px 20px 20px 20px"]
[ux_text font_size="2"]
<h2>Liên hệ</h2>
[/ux_text]
[ux_text font_size="1.05"]
Thông tin hỗ trợ và định hướng chuyển đổi.
[/ux_text]
[contact-form-7 id="FORM_ID"]
[/col]

[col span="7" span__sm="12"]
[map height="540px" height__sm="340px" content_enable="0" color="#455e61" saturation="-81"]
<h3>Địa chỉ / vùng phục vụ</h3>
<p>Mô tả ngắn.</p>
[/map]
[/col]

[/row]

[/section]
```

### Biến chính

- `FORM_ID`
- nội dung liên hệ
- map height
- tone màu map

## 6. Team Roster Grid

### Dùng khi nào

- about
- leadership
- recruitment

### Khung native

```txt
[section label="Team" padding="70px" padding__sm="40px"]

[row h_align="center"]
[col span="8" span__sm="12" align="center"]
[title style="center" text="Đội ngũ"]
[ux_text font_size="1.05"]
Mô tả ngắn về đội ngũ.
[/ux_text]
[/col]
[/row]

[row]
[col span="12"]
[row_inner]

[col_inner span="4" span__sm="12"]
[team_member img="IMAGE_ID_1" name="Tên 1" title="Chức danh" icon_style="small" facebook="#" phone="#" linkedin="#" image_height="100%" image_width="80" image_radius="100"]
[/team_member]
[/col_inner]

[col_inner span="4" span__sm="12"]
[team_member img="IMAGE_ID_2" name="Tên 2" title="Chức danh" icon_style="small" facebook="#" phone="#" linkedin="#" image_height="100%" image_width="80" image_radius="100"]
[/team_member]
[/col_inner]

[col_inner span="4" span__sm="12"]
[team_member img="IMAGE_ID_3" name="Tên 3" title="Chức danh" icon_style="small" facebook="#" phone="#" linkedin="#" image_height="100%" image_width="80" image_radius="100"]
[/team_member]
[/col_inner]

[/row_inner]
[/col]
[/row]

[/section]
```

### Biến chính

- số thành viên
- ảnh
- social fields
- density card

## 7. Tabbed FAQ / Pricing Panel

### Dùng khi nào

- FAQ
- pricing
- service explainer

### Khung native

```txt
[section label="Tabs Panel" padding="70px" padding__sm="40px"]

[row]
[col span="12"]
[tabgroup style="line-bottom" align="center"]
[tab title="Nhóm 1"]
[accordion]
[accordion-item title="Câu hỏi 1"]
<p>Trả lời 1</p>
[/accordion-item]
[accordion-item title="Câu hỏi 2"]
<p>Trả lời 2</p>
[/accordion-item]
[/accordion]
[/tab]
[tab title="Nhóm 2"]
[ux_text font_size="1.05"]
Nội dung nhóm thứ hai.
[/ux_text]
[button text="CTA chính" color="secondary" style="underline"]
[/tab]
[/tabgroup]
[/col]
[/row]

[/section]
```

### Biến chính

- số tab
- style tab
- có accordion hay không
- CTA close

## 8. Video Trigger Banner

### Dùng khi nào

- story
- process
- explainer

### Khung native

```txt
[section label="Video Banner" padding="0px"]

[row]
[col span="12"]
[ux_banner height="520px" height__sm="320px" bg="IMAGE_ID"]
[text_box position_x="50" position_y="50"]
<h2>Watch the story</h2>
[video_button video="https://www.youtube.com/watch?v=example"]
[/text_box]
[/ux_banner]
[/col]
[/row]

[/section]
```

### Biến chính

- ảnh nền
- vị trí text
- link video

## 9. Editorial Posts Rail

### Dùng khi nào

- blog home
- insights
- authority section

### Khung native

```txt
[section label="Posts Rail" padding="70px" padding__sm="40px"]

[row h_align="center"]
[col span="8" span__sm="12" align="center"]
[title style="center" text="Bài viết nổi bật"]
[/col]
[/row]

[row]
[col span="12"]
[blog_posts style="normal" columns="3" posts="6" show_date="text" image_height="56.25%"]
[/col]
[/row]

[/section]
```

### Biến chính

- style bài viết
- số lượng bài
- image ratio

## Ghi Chú Trung Thực

- các snippet này là `starter shell`, không phải block cuối
- nơi nào syntax còn chưa đủ chứng cứ thì không được tự thêm tham số
- nếu cần surface như `hotspot`, `flip book`, `message box`, phải quay lại lớp `platform` để kiểm tra trạng thái xác minh
