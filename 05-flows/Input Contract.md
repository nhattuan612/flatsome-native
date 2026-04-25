# Input Contract

Date: 2026-04-25

## Mục Đích

Đây là `cửa vào duy nhất` cho mọi task Flatsome.

Mục tiêu:

- chặn tình trạng brief ngắn nhưng kỳ vọng cao
- buộc worker chốt đúng `loại input`
- buộc worker chốt đúng `mức độ giống`
- buộc worker chốt đúng `mức độ sáng tạo`
- tạo ra `Brief Chuẩn Hóa V2` trước khi sang `Brief Intake Flow`

## Luật Cứng

- không được build nếu chưa đi qua `Input Contract`
- không được đoán `đang clone hay sáng tạo`
- không được đoán `mức độ giống`
- không được đoán `style source`
- phần nào không rõ phải ghi `không xác định`
- chỉ được dùng `default an toàn` ở phần thật sự thiếu dữ liệu

## Phải Chốt Ở Lớp Này

- `Loại input:`
  - `text thường`
  - `ảnh`
  - `markdown spec`
  - `link tham chiếu`
  - `mixed`
- `Mục tiêu task:`
  - `clone`
  - `interpret`
  - `creative-default`
  - `creative-modern`
  - `optimization`
  - `rebuild`
- `Mức độ giống mẫu:`
  - `gần như tuyệt đối`
  - `bám tinh thần`
  - `tự do sáng tạo có kiểm soát`
- `Mức độ sáng tạo:`
  - `default Flatsome`
  - `guided creative`
  - `design-language-driven`
- `CTA chính`
- `Thiết bị ưu tiên`
- `Tone giao diện`
- `Anti-patterns cần tránh`
- `Brand constraints`
- `Unknowns`
- `Default an toàn`

## Default An Toàn

Nếu user không chốt rõ:

- `style source:`
  - `Flatsome Native Core`
- `mức độ sáng tạo:`
  - `default Flatsome`
- `mức độ giống:`
  - `bám tinh thần`
- `thiết bị ưu tiên:`
  - `mobile trước`
- `motion:`
  - `nhẹ`
- `tone:`
  - `sáng`
  - `sạch`
  - `hiện đại`

## Style Source

Worker bắt buộc chốt `1` trong các nguồn sau:

- `Flatsome Native Core`
- `Flatsome Native Core + Design Intelligence`
- `tham chiếu ngoài do user đưa`

Nếu user không đưa gì và cũng không yêu cầu sáng tạo mạnh:

- dùng `Flatsome Native Core`

## Reference Authority

Worker phải chốt mức tin cậy của reference:

- `primary`
  - user bảo phải bám sát
- `secondary`
  - chỉ dùng để lấy tinh thần
- `inspiration-only`
  - chỉ để gợi ý

## Output Expectation

Worker phải chốt rõ output thuộc loại nào:

- `clone`
- `reinterpret`
- `original`

Không được sang build nếu mục này chưa khóa.

## Brief Chuẩn Hóa V2

Sau `Input Contract`, worker phải tạo được gói brief này:

```txt
Tên task:
Loại input:
Input gốc:
Mục tiêu task:
Output expectation:
Mức độ giống:
Mức độ sáng tạo:
Style source:
Reference authority:
CTA chính:
Thiết bị ưu tiên:
Tone giao diện:
Anti-patterns cần tránh:
Brand constraints:
Unknowns:
Default an toàn:
```

## Dấu Hiệu Fail Sớm

Nếu gặp một trong các dấu hiệu sau thì chưa được route:

- user chỉ nói `làm đẹp hơn` nhưng không rõ `clone` hay `creative`
- có link/ảnh tham chiếu nhưng không rõ phải `bám sát` hay `lấy tinh thần`
- có yêu cầu hiện đại/sáng tạo nhưng không rõ có mở `design intelligence` không
- không có CTA chính
- không có thiết bị ưu tiên

## Đầu Ra Bắt Buộc

- `Brief Chuẩn Hóa V2`
- `Unknowns`
- `Default an toàn`
- `Output expectation`
- `Style source`
- `Reference authority`

## Kết Luận

`Input Contract` tồn tại để worker không còn phải tự suy đoán cách hiểu brief ngay từ đầu.
