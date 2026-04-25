# Best Result Playbook

Date: 2026-04-25

## Mục Đích

Đây là file dành cho người giao task.

Nó trả lời:

- giao task thế nào để AI hiểu nhanh
- nói ngắn nhưng vẫn đủ rõ bằng cách nào
- cần tối thiểu thông tin gì để ra kết quả đẹp ngay từ vòng đầu

## Luật Giao Task Ngắn Mà Vẫn Rõ

Nếu muốn kết quả tốt nhất, brief nên có ít nhất:

- `loại input`
- `mục tiêu task`
- `output expectation`
- `CTA chính`
- `tone`
- `thiết bị ưu tiên`

Nếu có reference:

- nói rõ nó là `bám sát`, `bám tinh thần`, hay `chỉ để tham khảo`

## Mẫu Giao Task Tối Thiểu

```txt
Loại input:
Mục tiêu task:
Output expectation:
CTA chính:
Tone giao diện:
Thiết bị ưu tiên:
Reference authority:
Điểm cần bám:
Điểm được sáng tạo:
```

## Mẫu Tốt

### 1. Clone gần giống

```txt
Loại input: ảnh + link
Mục tiêu task: clone
Output expectation: clone
CTA chính: đăng ký tư vấn
Tone giao diện: sáng, premium
Thiết bị ưu tiên: mobile trước
Reference authority: primary
Điểm cần bám: hero layout, section order, hierarchy
Điểm được sáng tạo: ảnh và copy chi tiết
```

### 2. Build từ brief thường

```txt
Loại input: text thường
Mục tiêu task: creative-default
Output expectation: original
CTA chính: xem sản phẩm
Tone giao diện: sạch, hiện đại
Thiết bị ưu tiên: mobile trước
Reference authority: không có
Điểm cần bám: native, dễ edit
Điểm được sáng tạo: bố cục và visual language
```

### 3. Build từ ảnh

```txt
Loại input: ảnh
Mục tiêu task: interpret
Output expectation: reinterpret
CTA chính: liên hệ ngay
Tone giao diện: editorial, nhẹ
Thiết bị ưu tiên: mobile trước
Reference authority: secondary
Điểm cần bám: nhịp section và tinh thần tổng
Điểm được sáng tạo: typography, spacing, card style
```

### 4. Build từ markdown spec

```txt
Loại input: markdown spec
Mục tiêu task: rebuild
Output expectation: reinterpret
CTA chính: nhận báo giá
Tone giao diện: theo spec
Thiết bị ưu tiên: mobile trước
Reference authority: primary
Điểm cần bám: section map và CTA flow
Điểm được sáng tạo: visual refinement nếu spec không khóa
```

### 5. Sáng tạo theo Flatsome mặc định

```txt
Loại input: text thường
Mục tiêu task: creative-default
Output expectation: original
CTA chính: đặt lịch tư vấn
Tone giao diện: sáng, hiện đại
Thiết bị ưu tiên: mobile trước
Reference authority: không có
Điểm cần bám: Flatsome native core
Điểm được sáng tạo: layout, hero family, proof pattern
```

### 6. Sáng tạo theo design language hiện đại

```txt
Loại input: text + repo tham khảo
Mục tiêu task: creative-modern
Output expectation: original
CTA chính: dùng thử ngay
Tone giao diện: bold, hiện đại
Thiết bị ưu tiên: mobile trước
Reference authority: inspiration-only
Điểm cần bám: tinh thần design language
Điểm được sáng tạo: toàn bộ layout trong giới hạn native
```

## Mẫu Xấu

### Xấu 1

`làm cho đẹp hơn`

Vấn đề:

- không biết clone hay sáng tạo
- không có CTA
- không có tone
- không có reference authority

### Xấu 2

`làm giống web này`

Vấn đề:

- không rõ `gần như tuyệt đối` hay `bám tinh thần`
- không rõ phần nào được đổi
- không rõ thiết bị ưu tiên

### Xấu 3

`build cho tôi 1 homepage hiện đại`

Vấn đề:

- `hiện đại` là quá rộng
- không rõ dùng Flatsome mặc định hay design language ngoài

## Khi Nào Cần Viết Dài Hơn

Hãy viết thêm nếu:

- cần clone sát
- có nhiều reference xung đột
- có brand guideline riêng
- có nhiều CTA
- có mục tiêu chuyển đổi rất cụ thể

## Kết Luận

Người giao task không cần viết dài.

Nhưng phải chốt đúng:

- input gì
- muốn giống tới đâu
- cho phép sáng tạo tới đâu
- CTA là gì
- ưu tiên thiết bị nào
