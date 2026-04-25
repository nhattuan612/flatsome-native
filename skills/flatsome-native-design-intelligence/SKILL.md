---
name: flatsome-native-design-intelligence
description: Tăng sáng tạo, đổi design language, reinterpret thay vì clone, giảm lặp bố cục. Chỉ dùng khi cần sáng tạo mạnh hơn Flatsome Native Core mặc định.
---

# flatsome-native-design-intelligence — Sáng Tạo

## Mục Đích

Skill này là **cửa sáng tạo nâng cao** của hệ `flatsome-native`.

Dùng khi:
- cần sáng tạo mạnh hơn mặc định Flatsome
- cần đổi design language (Minimal, Bold Editorial, Luxury, v.v.)
- cần reinterpret thay vì clone
- cần tăng novelty, giảm lặp bố cục

Không dùng khi:
- task chỉ cần build chuẩn theo lõi Flatsome mặc định → dùng `flatsome-native-builder`
- task đang là harvest kỹ thuật → dùng `flatsome-native-harvest`

## Call Phrase

```
use flatsome-native-design-intelligence_(Sang_Tao)
```

## Quy Tắc Khi Mở Skill Này

- mặc định hệ vẫn bám `Flatsome Native Core`
- chỉ mở lớp sáng tạo khi user yêu cầu rõ hoặc `builder` cần hỗ trợ để tránh lặp
- design intelligence KHÔNG thay thế skill build — nó hỗ trợ và nâng chất lượng sáng tạo

## Thứ Tự Đọc Tối Thiểu

1. `08-design-intelligence/README.md`
2. `08-design-intelligence/Design Mode Router.md`
3. `08-design-intelligence/Reference Sources.md`
4. `08-design-intelligence/Style Taxonomy.md`
5. `08-design-intelligence/Pattern Decision Matrix.md`
6. `03-factory/Design Language Reference.md`
7. `03-factory/Typography System.md`
8. `03-factory/Spacing System.md`
9. `03-factory/Layout DNA.md`
10. `03-factory/No Repeat Law.md`

Nếu cần thêm:
- `08-design-intelligence/Typography Mood Matrix.md`
- `08-design-intelligence/Spacing Rhythm Matrix.md`
- `08-design-intelligence/Motion Profile Matrix.md`
- `08-design-intelligence/Anti-Pattern Library.md`

## Design Mode Router

Trước khi chọn design direction, đọc:

- `08-design-intelligence/Design Mode Router.md`

Nó sẽ route vào đúng style family dựa trên yêu cầu của user.

## Reference Sources — Luật Dùng Nguồn Ngoài

Khi hút inspiration từ repo/site ngoài, phải theo:

- `08-design-intelligence/Reference Sources.md`

Không được:
- bê nguyên token màu của brand khác
- copy wording/screenshot của hệ khác
- dùng assets ngoài làm default mặc định

## Quan Hệ Với Builder

Skill này chỉ nên mở khi `builder` đã xác định cần sáng tạo mạnh hơn.

Luồng kết hợp thường gặp:
```
Builder (intake + route) -> Design Intelligence (chọn direction) -> Builder (build + audit)
```

## Hub Reference

Repo: https://github.com/flatsome-native/flatsome-native
File chính: `08-design-intelligence/README.md`, `08-design-intelligence/Design Mode Router.md`
