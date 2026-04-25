# Quy Tắc Quản Trị CSS Cho Flatsome Native

Date: 2026-04-24

## Mục Đích

Tài liệu này tồn tại để ngăn `CSS` trở thành bãi rác trong hệ thống Flatsome.

Mục tiêu:

- CSS có trật tự
- dễ tìm
- dễ sửa
- không phá editability của Builder

## Luật Gốc

1. `CSS` phải được ưu tiên giải quyết bằng `setting native` trước.
2. Chỉ dùng `CSS` khi native settings không đủ.
3. `CSS` phải đặt tại `Theme Options` của Flatsome như đường mặc định.
4. Không dùng `CSS` cục bộ tại trang như đường mặc định.
5. Mọi đoạn `CSS` thêm mới phải có comment tiếng Việt.
6. Không dùng CSS để che lỗi cấu trúc builder.
7. Mọi cụm CSS phải có `namespace`, `scope`, và `owner` rõ ràng.

## Khi Nào Được Phép Dùng CSS

Chỉ được thêm CSS khi thuộc một trong các nhóm sau:

- tinh chỉnh spacing mà native settings không đạt đúng mục tiêu
- tinh chỉnh typography đặc biệt mà builder không đủ
- xử lý hover/focus/state cần thiết cho trải nghiệm
- sửa va chạm hiếm giữa components
- khóa tone brand nhất quán trên nhiều trang

## Khi Nào Không Được Dùng CSS

Không được dùng CSS để:

- dựng lại toàn bộ layout chính
- giả section / row / col bằng div và CSS
- che lỗi native structure
- vá tạm cho qua QA
- kéo một trang HTML-heavy thành nhìn giống native

## Namespace Bắt Buộc

Mọi CSS thêm mới phải có prefix theo mẫu:

`[dự án]-[trang]-[section]-[vai trò]`

Ví dụ:

- `.pl-home-hero-shell`
- `.pl-recruit-cta-button`
- `.brand-about-proof-grid`

Nếu không xác định được namespace rõ ràng thì chưa được thêm CSS.

## Mẫu Comment Bắt Buộc

Mọi cụm CSS thêm mới phải có comment tiếng Việt theo mẫu:

```css
/* 
Mục đích: Điều chỉnh khoảng cách cho CTA cuối trang tuyển dụng
Trang áp dụng: Tuyển dụng / About / Landing tuyển dụng
Section áp dụng: CTA cuối
Ngày thêm: 2026-04-24
Người thêm: Codex
Ghi chú: Native spacing không đủ để đạt khoảng thở theo chuẩn thương hiệu
Scope: project
Namespace: pl-recruit-cta
*/
```

## Quy Tắc Đặt Tên Class

Nếu phải thêm class phục vụ CSS:

- dùng tên có nghĩa
- tránh tên mơ hồ kiểu `custom-box-1`, `fix-row-new`, `tmp-style`
- ưu tiên prefix theo ngữ cảnh rõ ràng

Ví dụ:

- `.pl-recruit-cta`
- `.brand-home-hero`
- `.company-proof-grid`

## Cấp Độ CSS

### Cấp 1: CSS nền công ty

Dùng khi:

- áp dụng cho nhiều trang
- gắn với luật thương hiệu
- có khả năng tái sử dụng cao

### Cấp 2: CSS theo dự án

Dùng khi:

- chỉ áp dụng cho một dự án
- nhưng có thể tái dùng giữa nhiều trang trong cùng dự án

### Cấp 3: CSS ngoại lệ hiếm

Dùng khi:

- chỉ xử lý một trường hợp rất cụ thể
- không nên tái sử dụng rộng
- phải có `report + file/log`

## Điều Kiện Pass

CSS được xem là quản trị tốt khi:

- tất cả CSS mới có comment tiếng Việt
- CSS nằm trong `Theme Options`
- không có dấu hiệu dựng layout chính bằng CSS
- builder editability vẫn còn nguyên
- người sau nhìn vào hiểu được mục đích của đoạn CSS

## Điều Kiện Fail

Fail khi:

- CSS không có comment
- CSS không có namespace rõ ràng
- CSS cục bộ nằm rải rác khó quản lý
- CSS bị dùng để che lỗi structure
- CSS phá khả năng chỉnh sửa của Builder
- CSS tích tụ nhưng không có logic đặt tên

## Câu Hỏi Trước Khi Viết CSS

Trước khi thêm CSS, phải tự trả lời:

1. Có giải được bằng native setting không?
2. Nếu không, phần nào của native setting đang thiếu?
3. CSS này là nền công ty, theo dự án, hay ngoại lệ hiếm?
4. Người sau có hiểu được đoạn này không?
5. CSS này có làm Builder khó chỉnh lại không?

Nếu không trả lời rõ được 5 câu trên thì chưa được thêm CSS.
