# Quick Start Menu

Date: 2026-04-25

## Mục Đích

Đây là menu khởi động nhanh cho người dùng chưa biết nên mô tả task thế nào.

Chỉ cần chọn đúng `1` nhánh là worker đã có thể route tiếp.

## Menu 6 Nhánh

### 1. Tôi muốn clone gần giống một giao diện có sẵn

Hãy đưa:

- `ảnh` hoặc `link`
- CTA chính
- mức độ giống mong muốn

Worker sẽ route:

- `clone`

### 2. Tôi có ảnh, hãy dựng lại bằng UX Builder editable

Hãy đưa:

- `ảnh`
- phần nào phải bám sát
- phần nào được đổi
- CTA chính

Worker sẽ route:

- `clone` hoặc `reinterpret`

### 3. Tôi chỉ có brief ngắn, hãy tự sáng tạo theo Flatsome mặc định

Hãy đưa:

- mục tiêu trang
- CTA chính
- tone
- thiết bị ưu tiên

Worker sẽ route:

- `creative-default`

### 4. Tôi muốn sáng tạo mạnh hơn, hiện đại hơn

Hãy đưa:

- mục tiêu trang
- CTA chính
- tone
- mức độ sáng tạo mong muốn
- nếu có thì thêm style tham khảo

Worker sẽ route:

- `creative-modern`

### 5. Tôi có markdown/spec, hãy build từ đó

Hãy đưa:

- file spec hoặc nội dung spec
- phần nào là khóa cứng
- phần nào được tinh chỉnh

Worker sẽ route:

- `rebuild`

### 6. Tôi có nhiều nguồn: text + ảnh + link + repo style

Hãy đưa:

- tất cả nguồn
- nguồn nào là chính
- output cuối muốn clone, reinterpret hay original

Worker sẽ route:

- `mixed` theo `output expectation`

## Mẫu Chọn Nhanh

```txt
Chọn 1 nhánh:
1. Clone gần giống
2. Dựng lại từ ảnh
3. Brief ngắn + Flatsome mặc định
4. Brief ngắn + sáng tạo mạnh
5. Build từ markdown/spec
6. Mixed input
```

## Sau Khi Chọn Menu

Worker phải mở tiếp:

- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`

## Kết Luận

Menu này tồn tại để người mới bắt đầu thật nhanh mà không cần hiểu nội bộ hệ thống.
