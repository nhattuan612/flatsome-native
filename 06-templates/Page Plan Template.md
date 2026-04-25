# Mẫu Page Plan Chuẩn

Date: 2026-04-24

## Cách Dùng

- điền đầy đủ trước khi build
- không được bỏ trống các mục bắt buộc
- mọi giá trị chưa rõ phải ghi `không xác định`

---

## 1. Thông Tin Chung

- `Loại input:`
- `Input gốc:`
- `Tên trang:`
- `Dự án:`
- `Loại trang:`
- `Mục tiêu trang:`
- `Mục tiêu task:`
- `Output expectation:`
- `Reference authority:`
- `Style source:`
- `Mức độ tự do sáng tạo:`
- `CTA chính:`
- `Thiết bị ưu tiên:`

## 2. Định Hướng Giao Diện

- `Tone giao diện:`
- `Design Mode:`
- `Style family:`
- `Pattern family:`
- `Typography mood:`
- `Spacing rhythm:`
- `Motion profile:`
- `Anti-patterns cần tránh:`
- `Màu chủ đạo:`
- `Màu phụ:`
- `Font chính:`
- `Hướng typography:`
- `Type roles chính:`
- `Chiến lược hero title:`
- `Hero title budget:`
- `Hero title expected line count desktop/mobile:`
- `Heading wrapper risk:`
- `Hero title fallback nếu vượt budget:`
- `Chiến lược body copy:`
- `Spacing profile:`
- `Mật độ section:`
- `Mật độ card:`
- `Chiến lược giảm spacing mobile:`
- `Phong cách chuyển động (motion):`
- `Mức độ giống mẫu tham chiếu cần đạt:`
- `Nguồn design language tham khảo:`
- `Điểm phải bám sát:`
- `Điểm được sáng tạo:`
- `Layout DNA đã chọn:`
- `Lý do chọn DNA:`
- `Layout Pool đã chọn:`
- `Hero Family đã chọn:`
- `Dominant Geometry đã chọn:`
- `CTA Pattern đã chọn:`
- `Proof Pattern đã chọn:`
- `Recipe section order đã chọn:`
- `Macro Sequence Fingerprint dự kiến:`
- `Điểm khác macro sequence so với trang gần nhất:`
- `Trang gần nhất để so chống lặp:`
- `3 trang gần nhất đã so:`
- `Điểm phải khác trang gần nhất:`
- `Similarity Risk dự kiến:`
- `Novelty Score dự kiến (0-16):`
- `Kết luận novelty gate:`

## 3. Giá Trị Chưa Rõ

- `Unknowns:`
- `Default an toàn sẽ dùng:`
- `Có cần suy diễn không:`
- `Nếu có thì suy diễn phần nào:`
- `Mức độ rõ của input:`
- `Độ tin cậy của reference:`

## 4. Reuse Từ Tài Sản Sẵn Có

- `Route label:`
- `Skeleton đã chọn:`
- `Archetype ưu tiên:`
- `Tái sử dụng từ block sẵn có:`
- `Ứng viên block nên tái dùng:`
- `Ứng viên block nên tạo mới:`
- `Block nào là page-local:`
- `Block nào có thể nâng lên thư viện công ty:`
- `Route lý do chọn:`
- `Ngoại lệ được phép nếu có:`

## 5. Cấu Trúc Tổng Thể

- `Section Count:`
- `Tổng số row dự kiến:`
- `Tổng số col chính dự kiến:`

## 6. Section Map

### Section 1

- `Tên section:`
- `Mục tiêu:`
- `Số row:`
- `Số col chính:`
- `Nhóm element:`
- `CTA trong section này:`
- `Ghi chú responsive:`

### Section 2

- `Tên section:`
- `Mục tiêu:`
- `Số row:`
- `Số col chính:`
- `Nhóm element:`
- `CTA trong section này:`
- `Ghi chú responsive:`

### Section 3

- `Tên section:`
- `Mục tiêu:`
- `Số row:`
- `Số col chính:`
- `Nhóm element:`
- `CTA trong section này:`
- `Ghi chú responsive:`

### Section N

- `Tên section:`
- `Mục tiêu:`
- `Số row:`
- `Số col chính:`
- `Nhóm element:`
- `CTA trong section này:`
- `Ghi chú responsive:`

## 7. Native Elements Priority

- `Các native elements chính sẽ dùng:`
- `Điểm nào có nguy cơ phải dùng ngoại lệ:`

## 8. Risk Notes

- `Rủi ro lớn nhất:`
- `Phương án fallback:`
- `Điều kiện fail ngay:`
- `Dấu hiệu fail sớm nếu brief còn mơ hồ:`

## 9. Build Readiness Contract

- `Input đủ rõ để build chưa:`
- `Vì sao đủ hoặc chưa đủ:`
- `Worker có đang đoán route không:`
- `Worker có đang đoán style source không:`
- `Worker có đang đoán output expectation không:`
- `Tiêu chí thành công riêng của task này:`
- `Bằng chứng đã khóa route đúng:`
- `Bằng chứng đã khóa style source đúng:`
- `Bằng chứng đã khóa output expectation đúng:`

## 10. Điều Kiện Được Phép Build

- [ ] Đã qua Input Contract
- [ ] Đã chốt loại input
- [ ] Đã chốt output expectation
- [ ] Đã chốt style source
- [ ] Đã chốt reference authority
- [ ] Đã chốt mức độ tự do sáng tạo
- [ ] Đã chốt mục tiêu trang
- [ ] Đã chốt CTA chính
- [ ] Đã chốt Design Mode
- [ ] Đã chốt Style family
- [ ] Đã chốt Pattern family
- [ ] Đã chốt Typography mood
- [ ] Đã chốt Spacing rhythm
- [ ] Đã chốt Motion profile
- [ ] Đã chốt Hero title budget
- [ ] Đã chốt Heading wrapper risk
- [ ] Đã chốt Layout DNA
- [ ] Đã chốt Layout Pool
- [ ] Đã chốt Hero Family
- [ ] Đã chốt Section Order Recipe
- [ ] Đã chốt Macro Sequence Fingerprint
- [ ] Đã có Section Count
- [ ] Đã có Section Map
- [ ] Đã ghi Unknowns
- [ ] Đã ghi Build Readiness Contract
- [ ] Đã ghi Reuse từ block sẵn có
- [ ] Đã so với 3 trang gần nhất
- [ ] Đã kiểm tra No Repeat Law
- [ ] Novelty gate không bị block
- [ ] Đã sẵn sàng triển khai
