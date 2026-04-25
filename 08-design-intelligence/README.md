# 08-design-intelligence

Date: 2026-04-24

## Mục Đích

Đây là lớp `UI Intelligence` của công ty.

Nó không thay thế `Flatsome Core`.

Nó chỉ bổ sung:

- tư duy thẩm mỹ
- tư duy route thiết kế
- tư duy pattern
- tư duy typography / spacing / motion
- tư duy anti-pattern

để khi cần sáng tạo, hệ vẫn tạo được biến thể mạnh mà không phá native.

## Vai Trò Trong Hệ

- `Flatsome Core`
  - trả lời cái gì build được bằng native builder
- `Design Intelligence`
  - trả lời nên build với gu nào, nhịp nào, level chuyên nghiệp nào

Kết luận:

- `Flatsome` là lớp thực thi
- `Design Intelligence` là lớp định hướng sáng tạo

## Khi Nào Phải Đọc Folder Này

- khi user nói:
  - sáng tạo hơn
  - chuyên nghiệp hơn
  - theo phong cách Apple / Fluent / Carbon / editorial / luxury / startup / premium
- khi cần tạo biến thể khác hẳn các trang gần nhất
- khi muốn đề xuất 2-3 hướng thiết kế để user chọn
- khi user đưa design repo, brand guideline, website mẫu

## Khi Nào Không Cần Dùng

- khi task chỉ là build nhanh theo logic Flatsome mặc định
- khi brief rất rõ và không cần biến thể sáng tạo
- khi trang chỉ cần follow trực tiếp một page-local block đã ổn

## Đọc Gì Trước

1. `Design Intelligence Operating Model.md`
2. `08-design-intelligence/Design Mode Router.md`
3. `08-design-intelligence/Reference Sources.md`
4. `Style Taxonomy.md`
5. `Pattern Decision Matrix.md`
6. `Typography Mood Matrix.md`
7. `Spacing Rhythm Matrix.md`
8. `Motion Profile Matrix.md`
9. `Anti-Pattern Library.md`
10. `templates/MASTER Design System Template.md`
11. `templates/Page Override Template.md`

## Source Of Truth Trong Folder Này

- mode rule:
  - `08-design-intelligence/Design Mode Router.md`
- operating model:
  - `Design Intelligence Operating Model.md`
- source usage rule:
  - `08-design-intelligence/Reference Sources.md`
- style taxonomy:
  - `Style Taxonomy.md`
- design decision layer:
  - `Pattern Decision Matrix.md`
  - `Typography Mood Matrix.md`
  - `Spacing Rhythm Matrix.md`
  - `Motion Profile Matrix.md`
- safety layer:
  - `Anti-Pattern Library.md`

## Luật Quan Trọng

1. Không copy nguyên xi design system ngoài.
2. Không dùng repo ngoài như `source of truth` mặc định.
3. Chỉ hấp thụ `cấu trúc tư duy`.
4. Mọi kết quả cuối phải dịch về `Flatsome Native`.
5. Nếu user không yêu cầu sáng tạo, mặc định ưu tiên `Flatsome Core`.
6. `08-design-intelligence/Reference Sources.md` là source of truth duy nhất cho source usage rule của lớp này.

## Kết Luận

Folder này là:

- lớp sáng tạo
- lớp đề xuất
- lớp mở rộng vốn thiết kế

nhưng không phải lớp phá luật native.
