# SKILL SURFACE MAP

Date: 2026-04-25

## Mục Đích

File này định nghĩa lớp `skill surface` khi đóng gói `flatsome-native` thành skill cho Codex hoặc AI worker khác.

Mục tiêu:

- chỉ dùng `3 skill`
- tên hiển thị rõ cho người dùng Việt
- AI đọc vào hiểu ngay skill nào dùng để làm gì
- giữ tên kỹ thuật đủ sạch để dễ map nội bộ

## Nguyên Tắc Chung

Chỉ có `3 skill` vận hành:

- `flatsome-native-builder`
- `flatsome-native-harvest`
- `flatsome-native-design-intelligence`

Bên ngoài có thể hiển thị bằng label dài hơn để người dùng dễ hiểu.

## Skill 1

### Canonical ID

- `flatsome-native-builder`

### Display Label

- `flatsome-native-builder_(Build_Trang)`

### Call Phrase

- `use flatsome-native-builder_(Build_Trang)`

### Dùng Khi Nào

- build page mới bằng `Flatsome UX Builder`
- clone hoặc rebuild UI từ brief, ảnh, link, markdown spec
- tạo `Page Plan`, build native, audit, repair, release

### Không Dùng Khi Nào

- mục tiêu chính là hút thêm thư viện UI
- mục tiêu chính là nghiên cứu sáng tạo hoặc mở design language ngoài

### Route Nội Bộ

Skill này đi qua các lớp:

- `05-flows/Task Type Router.md`
- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`
- `05-flows/Brief Intake Flow.md`
- `03-factory/Task Route Matrix.md`
- `06-templates/Page Plan Template.md`
- `05-flows/UI Build Script.md`
- `05-flows/Final QA Checklist.md`

### Vai Trò

Đây là `cửa chính`.

Nếu user không nói gì đặc biệt, mặc định vào skill này trước.

## Skill 2

### Canonical ID

- `flatsome-native-harvest`

### Display Label

- `flatsome-native-harvest_(Hoc_Them_UI)`

### Call Phrase

- `use flatsome-native-harvest_(Hoc_Them_UI)`

### Dùng Khi Nào

- harvest từ `Flatsome Studio`
- import / kiểm coverage / check catalog
- extract template evidence
- cập nhật native map, slot map, library knowledge

### Không Dùng Khi Nào

- mục tiêu chính là giao 1 page hoàn chỉnh cho người xem
- mục tiêu chính là đề xuất design language sáng tạo

### Route Nội Bộ

Skill này đi qua:

- `05-flows/Task Type Router.md`
- `05-flows/Verifiable Harvest Flow.md`
- `05-flows/Direct Harvest Flow.md`
- `05-flows/Imported Template Extraction Flow.md`
- `01-platform/Artifact Storage Rule.md`

### Vai Trò

Đây là `cửa học thêm tri thức`.

Nó mở rộng năng lực hệ nhưng không thay thế skill build.

## Skill 3

### Canonical ID

- `flatsome-native-design-intelligence`

### Display Label

- `flatsome-native-design-intelligence_(Sang_Tao)`

### Call Phrase

- `use flatsome-native-design-intelligence_(Sang_Tao)`

### Dùng Khi Nào

- cần sáng tạo mạnh hơn mặc định Flatsome
- cần đổi design language
- cần reinterpret thay vì clone
- cần tăng novelty, giảm lặp bố cục

### Không Dùng Khi Nào

- task chỉ cần build chuẩn theo lõi Flatsome mặc định
- task đang là harvest kỹ thuật

### Route Nội Bộ

Skill này đi qua:

- `08-design-intelligence/README.md`
- `08-design-intelligence/Design Mode Router.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`
- `03-factory/Layout DNA.md`
- `03-factory/No Repeat Law.md`

### Vai Trò

Đây là `cửa sáng tạo nâng cao`.

Nó chỉ nên mở khi có yêu cầu sáng tạo rõ hoặc khi `builder` cần hỗ trợ để tránh lặp.

## Quan Hệ Giữa 3 Skill

- `builder`
  - skill mặc định
- `harvest`
  - skill học thêm tri thức
- `design-intelligence`
  - skill nâng chất lượng sáng tạo

Quan hệ vận hành:

- đa số task đi vào `builder`
- khi cần học thêm hoặc cập nhật thư viện, dùng `harvest`
- khi cần sáng tạo mạnh hoặc đổi ngôn ngữ thiết kế, mở `design-intelligence`

## Quy Tắc Gọi An Toàn

Nếu chưa chắc:

- dùng `use flatsome-native-builder_(Build_Trang)`

Nếu nhiệm vụ là hút thêm giao diện:

- dùng `use flatsome-native-harvest_(Hoc_Them_UI)`

Nếu nhiệm vụ là sáng tạo mạnh:

- dùng `use flatsome-native-design-intelligence_(Sang_Tao)`

## Ghi Chú Cho AI

AI không nên coi `Display Label` là `ID nội bộ`.

Nên hiểu như sau:

- `Canonical ID`
  - tên kỹ thuật để map hệ thống
- `Display Label`
  - tên hiển thị cho người dùng
- `Call Phrase`
  - câu gọi dễ dùng trong prompt

## Kết Luận

Lớp skill surface của `flatsome-native` được chốt gọn ở `3 skill`.
Đây là mức đủ mạnh để vận hành mà vẫn dễ nhớ, dễ gọi, dễ scale.
