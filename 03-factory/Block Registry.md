# Sổ Đăng Ký Block Của Công Ty

Date: 2026-04-24

## Mục Đích

Tài liệu này tồn tại để biến `UX Block` thành tài sản có quản trị, không phải đống block tăng dần vô tổ chức.

Inventory ứng viên block nằm riêng tại:

- `03-factory/Block Library Candidates.md`

Mục tiêu:

- biết block nào đang tồn tại
- block nào dùng ở đâu
- block nào là tài sản công ty
- block nào chỉ là block riêng của dự án hoặc trang

## Phân Loại Block

Mọi block phải thuộc đúng một loại:

### 1. Core Library Block

Block cấp công ty, có thể dùng lại trên nhiều dự án.

Ví dụ:

- hero cơ bản
- CTA chuẩn công ty
- grid lợi ích
- testimonial row

### 2. Project Block

Block dùng cho một dự án cụ thể, có thể tái dùng giữa nhiều trang trong cùng dự án.

Ví dụ:

- CTA riêng cho một dự án bất động sản
- header proof riêng cho một thương hiệu

### 3. Page-only Block

Block chỉ phục vụ một trang duy nhất và không nên coi là block thư viện.

Ví dụ:

- section rất đặc thù cho một landing campaign

## Trường Bắt Buộc Của Mỗi Block

Mỗi block phải có đủ:

- `Tên block`
- `Loại block`
- `Mục đích`
- `Đầu vào có thể thay`
- `Dự án / trang đang dùng`
- `Tình trạng tái sử dụng`
- `Ghi chú`

## Mẫu Ghi Block

```md
- Tên block: Hero cơ bản sáng
  - Loại block: Core Library Block
  - Mục đích: hero dùng cho landing sáng, CTA chính + ảnh phải
  - Đầu vào có thể thay:
    - tiêu đề
    - mô tả
    - ảnh
    - CTA chính
    - CTA phụ
    - màu nền
  - Dự án / trang đang dùng:
    - Homepage sản phẩm mẫu
    - Landing tuyển dụng mẫu
  - Tình trạng tái sử dụng: cao
  - Ghi chú: dùng khi cần hero sáng, gọn, section-first
```

## Quy Tắc Dùng Block

1. Nếu một section lặp lại từ `2 lần` trở lên, phải tách block, trừ khi đã có ngoại lệ hiếm được ghi log.
2. Nếu block có khả năng dùng lại trên nhiều dự án, phải cân nhắc nâng lên `Core Library Block`.
3. Không tạo block trùng mục đích nhưng khác tên một cách tùy tiện.
4. Nếu block rất đặc thù, giữ nó ở mức `Page-only Block`.

## Handshake Với Flow Và Page Plan

Trước khi worker rời factory để sang `Page Plan`, phải chốt rõ:

- `Tái sử dụng từ block sẵn có`
- `Ứng viên block nên tái dùng`
- `Ứng viên block nên tạo mới`
- `Block nào là page-local`
- `Block nào có thể nâng lên thư viện công ty`

Nếu bỏ qua lớp này:

- `Page Plan` sẽ thiếu quyết định tái dùng
- worker dễ dựng lại section lặp từ đầu

## Ứng Viên Block Thư Viện Ưu Tiên

Những archetype sau nên được ưu tiên cân nhắc tách thành block khi đã dùng ổn định:

- `Contact split with map`
- `Team roster grid`
- `Portfolio showcase rail`
- `Tabbed FAQ / pricing panel`
- `Testimonial + logo proof rail`
- `Video trigger banner`
- `Instagram / social proof strip`
- `Footer block replacement`
- `Reusable header/content region block`

Chi tiết mức ưu tiên và trạng thái sẵn sàng xem tại:

- `03-factory/Block Library Candidates.md`

## Quy Tắc Đặt Tên Block

Tên block phải:

- ngắn
- rõ mục đích
- không mơ hồ
- không dùng kiểu `block-1`, `new-block-final`, `test-block-ok`

Ví dụ tên tốt:

- `Hero sáng cơ bản`
- `CTA tối 2 cột`
- `Grid lợi ích 3 cột`
- `Testimonial 2 cột ảnh phải`

Mẫu tên nên theo công thức:

- `Loại section + mood/layout + mục đích`

Ví dụ:

- `Contact split map sáng`
- `Proof rail logo tối`
- `FAQ tabs line-bottom`
- `Portfolio rail 2 cột`
- `Video banner centered`

## Quy Tắc CEO

Nếu thư viện block có dấu hiệu phình to:

- block trùng mục đích
- block không ai dùng lại
- block khó hiểu

thì phải dọn lại sổ block trước khi tạo thêm block mới cùng loại.

Không để thư viện lớn dần mà không có cấu trúc.

## Điều Kiện Một Block Được Nâng Cấp Thành Tài Sản Công Ty

Một block có thể được nâng thành `Core Library Block` khi:

- dùng được ở nhiều bối cảnh
- không quá phụ thuộc vào brand cụ thể
- native structure rõ
- dễ chỉnh sửa trong UX Builder
- đã được dùng thực tế và cho kết quả tốt

## Dấu Hiệu Nên Tách Block Ngay

Phải cân nhắc tách block sớm nếu một section:

- đã xuất hiện từ `2 lần` trở lên ở nhiều page plan
- có cấu trúc native ổn định nhưng chỉ thay content/media
- có nhiều phần lồng nhau nên copy-paste dễ sai
- nằm ở vị trí lặp lại như:
  - proof band
  - contact split
  - team grid
  - portfolio rail
  - faq tabs
