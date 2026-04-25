# Guided Intake Questions

Date: 2026-04-25

## Mục Đích

Đây là script hỏi đáp ngắn cho người dùng chưa hiểu rõ hệ thống.

Mục tiêu:

- giúp 2 bên hiểu nhau nhanh
- không hỏi lan man
- không hỏi quá sâu quá sớm
- chốt đúng route trước khi build

## Nguyên Tắc Hỏi

- hỏi theo `2 tầng`
- tầng 1 chỉ để khóa route
- tầng 2 chỉ mở khi route đã rõ
- ưu tiên câu hỏi ngắn, dễ chọn
- ưu tiên `2-3 lựa chọn rõ ràng`
- không hỏi những gì đã biết từ brief

## Tầng 1: Hỏi Cực Ngắn Để Khóa Route

Phải chốt tối thiểu 5 điểm này:

1. `Anh đang đưa gì cho em?`
   - `mô tả bằng chữ`
   - `ảnh`
   - `link`
   - `markdown/spec`
   - `trộn nhiều loại`

2. `Anh muốn kết quả theo kiểu nào?`
   - `làm gần giống`
   - `bám tinh thần`
   - `tự sáng tạo mới`

3. `Anh muốn em đi theo hướng nào?`
   - `Flatsome mặc định`
   - `hiện đại hơn`
   - `theo mẫu hoặc style anh đưa`

4. `CTA chính là gì?`
   - ví dụ:
     - `liên hệ`
     - `đăng ký`
     - `xem sản phẩm`
     - `đặt lịch`

5. `Ưu tiên thiết bị nào?`
   - `mobile trước`
   - `desktop trước`
   - `cân bằng cả hai`

Nếu chưa chốt được 5 điểm này:

- chưa được route

## Tầng 2: Chỉ Hỏi Sâu Khi Cần

### Nếu route là `clone`

Hỏi thêm:

1. `Anh muốn giống gần như tuyệt đối hay chỉ cần rất gần?`
2. `Phần nào phải bám sát nhất?`
   - `hero`
   - `section order`
   - `typography`
   - `màu sắc`
3. `Phần nào được phép đổi?`

### Nếu route là `reinterpret`

Hỏi thêm:

1. `Anh muốn giữ tinh thần ở phần nào?`
2. `Phần nào em được phép làm mới mạnh hơn?`
3. `Có cần giữ đúng nhịp nội dung không?`

### Nếu route là `original`

Hỏi thêm:

1. `Anh muốn tone nào rõ nhất?`
   - `sáng`
   - `premium`
   - `tối giản`
   - `bold`
   - `neon`
2. `Anh muốn mặc định Flatsome hay hiện đại hơn?`
3. `Có thương hiệu hoặc style nào cần tránh không?`

## Bộ Câu Hỏi Theo Từng Loại Input

### A. Người dùng chỉ có brief text ngắn

Hỏi lần lượt:

1. `Anh muốn em làm gần giống một kiểu mẫu có sẵn hay tự sáng tạo mới?`
2. `Anh muốn giao diện theo Flatsome mặc định hay hiện đại hơn?`
3. `CTA chính là gì?`
4. `Ưu tiên mobile hay desktop?`

### B. Người dùng đưa ảnh

Hỏi lần lượt:

1. `Anh muốn clone gần giống hay chỉ lấy tinh thần từ ảnh này?`
2. `Phần nào trong ảnh phải bám sát nhất?`
3. `Có phần nào được phép sáng tạo lại không?`
4. `CTA chính của trang mới là gì?`

### C. Người dùng đưa link

Hỏi lần lượt:

1. `Link này là để clone hay chỉ để tham khảo tinh thần?`
2. `Em cần bám sát phần nào nhất?`
3. `Có phần nào không cần giữ?`
4. `CTA chính là gì?`

### D. Người dùng đưa markdown/spec

Hỏi lần lượt:

1. `Spec này là khóa cứng hay em được tinh chỉnh visual?`
2. `Section map có phải giữ nguyên không?`
3. `CTA chính đã là CTA cuối cùng chưa?`
4. `Có style source nào ngoài spec cần bám không?`

### E. Người dùng đưa mixed input

Hỏi lần lượt:

1. `Trong các nguồn này, cái nào là nguồn chính?`
2. `Anh muốn kết quả cuối là clone, reinterpret, hay original?`
3. `Nếu các nguồn xung đột thì ưu tiên nguồn nào?`
4. `CTA chính là gì?`

## Cách Tóm Tắt Hiểu Nhau Trước Khi Build

Sau khi hỏi xong, worker phải chốt lại bằng đoạn ngắn:

```txt
Em hiểu task này là:
- Loại input:
- Output expectation:
- Style source:
- Reference authority:
- CTA chính:
- Thiết bị ưu tiên:
- Phần phải bám:
- Phần được sáng tạo:
```

Nếu đoạn chốt này còn mơ hồ:

- quay lại hỏi tiếp

## Mẫu Hỏi Nhanh 1 Lượt

```txt
Để em hiểu đúng trước khi build, anh chốt giúp em 5 điểm:
1. Anh đang đưa cho em loại input nào: text, ảnh, link, spec hay mixed?
2. Anh muốn kết quả gần giống, bám tinh thần, hay sáng tạo mới?
3. Anh muốn đi theo Flatsome mặc định, hiện đại hơn, hay theo style tham chiếu?
4. CTA chính là gì?
5. Ưu tiên mobile hay desktop?
```

## Không Được Làm

- không hỏi sâu ngay từ câu đầu
- không hỏi 10 câu liền nhau với người mới
- không nhảy sang build khi chưa khóa route
- không dùng câu hỏi mở quá rộng nếu có thể hỏi bằng lựa chọn ngắn

## Kết Luận

File này giúp worker hỏi đúng mức, đủ rõ, và không làm người dùng mới bị mệt.
