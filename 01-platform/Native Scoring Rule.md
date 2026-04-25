# Quy Tắc Chấm Điểm Native Cho Trang Flatsome

Date: 2026-04-24

## Mục Đích

Tài liệu này định nghĩa cách công ty chấm điểm một trang `Flatsome Native Builder` để tránh tình trạng nói chung chung kiểu `trông có vẻ native`.

Mục tiêu của luật này là:

- biến `>=90% native` thành tiêu chuẩn có thể đánh giá
- khóa điều kiện `pass / fail`
- buộc mọi worker dùng cùng một thước đo

## Nguyên Tắc Chấm Điểm

Không chấm native theo cảm tính.

Trang phải được chấm trên `3 trục`:

1. `Layout Native`
2. `Content Native`
3. `Editability Native`

Chỉ cần một trục quá thấp thì toàn trang bị xem là rủi ro, dù các trục khác cao.

## Trục 1: Layout Native

### Mục tiêu

Kiểm tra phần khung trang có thật sự sống trong `section -> row -> col -> element` hay không.

### Điểm pass

Pass khi:

- layout chính nằm trong `section`, `row`, `col`
- không dùng `ux_html` làm khung layout chính
- các chia tách lớn của trang có thể nhìn ra rõ bằng `Section Map`
- không có phần lớn nào “giả native nhưng thật ra là HTML shell”

### Điểm fail nặng

Fail nặng khi:

- hero chính dựng bằng HTML shell
- khối nội dung lớn dựng bằng HTML shell
- row / col chỉ tồn tại để bọc HTML nặng
- section-first bị phá vỡ ở các phần chính

## Trục 2: Content Native

### Mục tiêu

Kiểm tra nội dung hiển thị có dùng đúng các elements mà UX Builder cung cấp hay không.

### Nội dung nên sống trong native

- `Text`
- `Title`
- `Banner`
- `Image`
- `Slider`
- `Stack`
- `Button`
- `Divider`
- `Accordion`
- `Gallery`
- `Icon Box`
- `Image Box`
- `Blog Posts`
- `Team Member`
- `Testimonial`
- `Page Header`
- các module native khác cùng họ

### Điểm pass

Pass khi:

- phần lớn nội dung sống trong native modules
- HTML không bị dùng để dựng các nhóm nội dung có thể làm bằng native module
- CTA, tiêu đề, text, ảnh, banner, slider đều ưu tiên native

### Điểm fail nặng

Fail nặng khi:

- nội dung chính của nhiều section nằm trong HTML dài
- text hierarchy sống ngoài native `Text/Title`
- CTA sống ngoài native `Button`
- nhiều khối visual chính chỉ là HTML/CSS tự dựng

## Trục 3: Editability Native

### Mục tiêu

Kiểm tra sau khi save, trang còn thật sự chỉnh sửa lại được trong Builder hay không.

### Điểm pass

Pass khi:

- `edit page` ổn
- `UX Builder` mở lại được
- kéo thả/chỉnh sửa lại được các phần chính
- người làm sau nhìn vào Builder vẫn hiểu cấu trúc
- section / row / col / element còn rõ ràng

### Điểm fail nặng

Fail nặng khi:

- Builder mở nhưng khó chỉnh sửa lại phần chính
- native structure bị bẩn tới mức người sau không dám sửa
- public đẹp nhưng bên trong builder gần như không còn khả năng bảo trì

## Thang Điểm Chuẩn

Mỗi trục chấm theo thang:

- `5`
  - rất tốt
- `4`
  - tốt
- `3`
  - chấp nhận được nhưng có rủi ro
- `2`
  - yếu
- `1`
  - fail nặng

## Cách Đọc Điểm

### Pass mạnh

- cả `3 trục` đều từ `4` trở lên

### Pass có điều kiện

- không có trục nào dưới `3`
- tổng thể vẫn đạt tinh thần `>=90% native`
- không có fail nặng

### Fail

Fail nếu xảy ra một trong các điều sau:

- có bất kỳ trục nào ở mức `1`
- `Editability Native` dưới `3`
- `Layout Native` dưới `3`
- dùng HTML làm layout chính
- Builder không mở lại/chỉnh lại được theo chuẩn thông thường

## Kết Luận Chấm Điểm

Khi review một trang, phải ghi đủ:

- `Layout Native Score`
- `Content Native Score`
- `Editability Native Score`
- `Novelty Score`
- `Similarity Risk`
- `Kết luận`
- `Lý do`

## Mẫu Ghi Điểm

```md
Native Scoring

- Layout Native Score: 4/5
- Content Native Score: 5/5
- Editability Native Score: 4/5
- Kết luận: Pass mạnh
- Lý do:
  - layout section-first rõ
  - CTA và text sống trong native modules
  - builder mở lại và chỉnh sửa được
```

## Quy Tắc CEO

Nếu có tranh cãi giữa:

- `public nhìn đẹp`
- và `builder chỉnh lại khó`

thì `Codex` phải ưu tiên khả năng bảo trì lâu dài, trừ khi trang đủ điều kiện `Ngoại Lệ Hiếm` đã được định nghĩa trong `01-platform/Operating Law.md`.

Từ nay một trang chỉ được xem là `release-ready` khi:

- `Native Scoring` pass
- và `Novelty Scoring` pass
