# Quy Tắc Chấm Điểm Novelty

Date: 2026-04-24

## Mục Đích

Tài liệu này biến yêu cầu `đừng lặp layout` thành một luật có thể chấm điểm.

`Native Scoring` kiểm tra:

- trang có builder-native hay không

`Novelty Scoring` kiểm tra:

- trang có đủ mới so với các trang gần nhất hay không

Release chỉ được xem là mạnh khi:

- `Native pass`
- và `Novelty pass`

## Dữ Liệu So Sánh Bắt Buộc

Trước khi chấm, phải mở:

- `07-reports/Recent Page Memory.md`

Mỗi trang mới phải so với:

- `3` trang gần nhất cùng loại hoặc gần loại

## 8 Trục Chấm Novelty

Chấm trên `8 trục` sau:

1. `Hero Family`
2. `Section Order`
3. `Dominant Geometry`
4. `CTA Pattern`
5. `Proof Pattern`
6. `Content Density`
7. `Image Treatment`
8. `Motion Profile`

## Macro Sequence Fingerprint

Ngoài `8 trục` chấm điểm, mọi page phải ghi thêm `Macro Sequence Fingerprint`.

Đây là chữ ký cấp cao của page theo thứ tự section chức năng, ví dụ:

- `hero -> stats -> showcase -> split thesis -> tabs utility -> proof -> faq -> close cta`
- `hero -> editorial band -> gallery -> trust -> pricing -> close cta`

Fingerprint này dùng để chặn đúng kiểu lỗi:

- đổi màu
- đổi domain
- đổi copy
- nhưng nhịp section tổng thể vẫn là cùng một page

### Cách Ghi

Phải ghi chuỗi vai trò của `8-12` section theo logic chức năng, không ghi theo tên mỹ thuật.

Ưu tiên dùng các nhãn:

- `hero`
- `stats / signal`
- `showcase`
- `split thesis / story`
- `utility tabs / compare`
- `gallery / visual showcase`
- `proof / testimonial`
- `timeline / process`
- `pricing / access`
- `faq / objection handling`
- `close cta`

### Luật Đọc Fingerprint

Nếu page mới:

- trùng `4` vai trò đầu tiên với page gần nhất
- và trùng thêm close sequence

thì `Similarity Risk` tối thiểu phải là `High`.

Nếu page mới:

- trùng `6+` vai trò chính trong cùng thứ tự
- và `Hero Family` hoặc `CTA Pattern` cũng gần giống

thì mặc định `Blocked`.

## Thang Điểm

Mỗi trục được chấm:

- `0`
  - gần như lặp lại
- `1`
  - có đổi nhưng chưa rõ
- `2`
  - đổi rõ, có giá trị

Tổng điểm tối đa:

- `16`

## Trục Trọng Yếu

4 trục sau là `trục trọng yếu`:

1. `Hero Family`
2. `Section Order`
3. `Dominant Geometry`
4. `CTA Pattern`

Nếu trang mới lặp `3/4` trục trọng yếu với trang gần nhất:

- mặc định `Blocked`

## Cách Đọc Điểm

### `0-6`

- `Blocked`
- chưa được build hoặc chưa được release

### `7-9`

- `Warn`
- chỉ được đi tiếp nếu có lý do rõ và sửa thêm để tăng novelty

### `10-13`

- `Pass`
- đủ mới để đi tiếp

### `14-16`

- `Pass mạnh`
- khác rõ cả về cấu trúc và cảm giác

## Similarity Risk

Ngoài tổng điểm, phải ghi `Similarity Risk` theo 4 mức:

- `Low`
- `Medium`
- `High`
- `Blocked`

### Luật đọc risk

- `Low`
  - chỉ trùng tối đa `1` trục trọng yếu
- `Medium`
  - trùng `2` trục trọng yếu hoặc nhiều trục phụ
- `High`
  - trùng `2` trục trọng yếu và cảm giác trang gần giống
- `Blocked`
  - trùng `3` trục trọng yếu hoặc lặp safe pattern
  - hoặc `Macro Sequence Fingerprint` quá gần với page gần nhất

## Safe Pattern Block

Các mô hình sau nếu lặp lại gần nguyên trạng phải bị `Blocked`:

- `slider hero -> benefits grid -> split story -> process -> testimonial -> faq -> CTA`
- `statement hero -> 3 cards -> split section -> testimonial -> CTA`
- `hero -> grid -> split -> process -> FAQ -> CTA`

Ngoài các safe pattern cố định trên, nếu `Macro Sequence Fingerprint` cho thấy page mới chỉ là biến thể da bên ngoài của page cũ, cũng phải bị `Blocked`.

## Dữ Liệu Bắt Buộc Phải Ghi

Khi chấm novelty, phải ghi:

- `3 trang đã so`
- `Hero Family`
- `Section Order`
- `Dominant Geometry`
- `CTA Pattern`
- `Proof Pattern`
- `Macro Sequence Fingerprint`
- `Macro Sequence Risk`
- `Novelty Score`
- `Similarity Risk`
- `Kết luận`

## Điều Kiện Được Phép Build

Chỉ được phép build khi:

- `Similarity Risk` không phải `Blocked`
- `Novelty Score dự kiến >= 10`

Nếu chỉ đạt `7-9`:

- phải sửa plan trước khi build

## Điều Kiện Được Phép Release

Chỉ được phép release khi:

- `Similarity Risk cuối` không phải `Blocked`
- `Novelty Score cuối >= 10`
- `Native Scoring` không fail

## Quy Tắc CEO

Nếu trang:

- builder-native tốt
- nhưng novelty thấp

thì vẫn chưa đạt chuẩn công ty.

Từ nay `builder-native` và `novelty` là `hai cổng pass độc lập`.
