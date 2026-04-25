# Mẫu Novelty Scoring Chuẩn

Date: 2026-04-24

## Cách Dùng

- điền `1 lần trước khi build`
- cập nhật lại `1 lần trước khi release`
- dùng đúng thang điểm trong `01-platform/Novelty Scoring Rule.md`

---

## 1. Thông Tin Chung

- `Tên trang:`
- `Dự án:`
- `Ngày chấm:`
- `Người chấm:`

## 2. Trang Dùng Để So

- `Trang so 1:`
- `Trang so 2:`
- `Trang so 3:`

## 3. Điểm Theo 8 Trục

- `Hero Family (0-2):`
- `Section Order (0-2):`
- `Dominant Geometry (0-2):`
- `CTA Pattern (0-2):`
- `Proof Pattern (0-2):`
- `Content Density (0-2):`
- `Image Treatment (0-2):`
- `Motion Profile (0-2):`

## 4. Trục Trọng Yếu

- `Hero Family có trùng mạnh không:`
- `Section Order có trùng mạnh không:`
- `Dominant Geometry có trùng mạnh không:`
- `CTA Pattern có trùng mạnh không:`

## 4A. Macro Sequence Fingerprint

- `Macro Sequence Fingerprint của trang này:`
- `Macro Sequence Fingerprint của trang gần nhất:`
- `Mức trùng sequence đầu trang:`
- `Mức trùng sequence cuối trang:`
- `Macro Sequence Risk:`
  - `Low`
  - `Medium`
  - `High`
  - `Blocked`
- `Điểm khác thật ở nhịp section là gì:`

## 5. Kết Luận

- `Novelty Score tổng (0-16):`
- `Similarity Risk:`
  - `Low`
  - `Medium`
  - `High`
  - `Blocked`
- `Kết luận cuối:`
  - `Blocked`
  - `Warn`
  - `Pass`
  - `Pass mạnh`

## 6. Ghi Chú

- `Safe pattern có xuất hiện không:`
- `Trang này khác trang gần nhất ở điểm nào:`
- `Nếu vẫn còn giống, phải sửa gì tiếp:`

## 7. Checklist

- [ ] Đã so với ít nhất 3 trang gần nhất
- [ ] Đã chấm đủ 8 trục
- [ ] Đã ghi `Macro Sequence Fingerprint`
- [ ] `Macro Sequence Risk` không bị bỏ trống
- [ ] Đã kết luận Similarity Risk
- [ ] Đã kết luận Novelty Score
- [ ] Nếu dưới ngưỡng pass, chưa được build hoặc release
