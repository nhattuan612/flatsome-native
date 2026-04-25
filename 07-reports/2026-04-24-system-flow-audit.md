# System Flow Audit

Date: 2026-04-24

## Mục Tiêu

Rà soát toàn bộ flow của hệ `Flatsome Native Builder` theo 4 tiêu chí:

- tính nhất quán
- tính khoa học
- tính dễ sử dụng
- tính dễ nâng cấp

## Kết Luận Nhanh

Hệ đang có nền tảng tốt, cấu trúc thư mục rõ và luật đủ mạnh để build native ổn định.

Tuy nhiên còn `3 lỗ hổng chính` cần xử lý để hệ thực sự mượt khi scale:

1. output bắt buộc nhiều hơn số template chuẩn đang có
2. lớp `Design Intelligence` chưa được cắm đủ vào flow chính
3. ownership giữa `Design Language Reference` và `08-design-intelligence` còn chồng

## Findings

### 1. [High] Output bắt buộc nhiều hơn template chuẩn đang có

#### Bằng chứng

- `01-platform/Operating Law.md` bắt buộc mỗi task UI phải có:
  - `Page Plan`
  - `Section Map`
  - `Native Build Output`
  - `Native Scoring`
  - `Novelty Scoring`
  - `Audit Checklist`
  - `Fix Pass`
  - `Final Verification`
- `05-flows/Final QA Checklist.md` cũng chặn release nếu các output này không tồn tại
- nhưng `06-templates/README.md` hiện chỉ có:
  - `06-templates/Page Plan Template.md`
  - `06-templates/Native Scoring Template.md`
  - `06-templates/Novelty Scoring Template.md`
  - `06-templates/Exception Report Template.md`
  - `06-templates/Block Entry Template.md`

#### Tác hại

- người làm phải tự phát minh format cho:
  - `Native Build Output`
  - `Audit Checklist`
  - `Fix Pass`
  - `Final Verification`
- dễ sinh ra mỗi page lưu một kiểu
- khó review
- khó tự động hóa về sau

#### File refs

- `01-platform/Operating Law.md`
- `05-flows/Final QA Checklist.md`
- `06-templates/README.md`

### 2. [High] Design Intelligence chưa cắm đủ vào flow thực thi chính

#### Bằng chứng

- `08-design-intelligence/Design Intelligence Operating Model.md` định nghĩa flow:
  - `Brief -> Chọn Mode -> Design Intelligence -> Dịch sang Flatsome Core -> Page Plan -> Build -> Audit`
- `08-design-intelligence/Design Mode Router.md` chia rõ:
  - `Flatsome Default`
  - `Design Assist`
  - `Directed Creative`
- nhưng `05-flows/UI Build Script.md` phần `Trước Plan phải chạy` chưa đưa `08-design-intelligence/*` vào chuỗi chính
- `06-templates/Page Plan Template.md` chưa có field cho:
  - `Design Mode`
  - `Style family`
  - `Pattern family`
  - `Typography mood`
  - `Motion profile`
  - `Anti-patterns cần tránh`

#### Tác hại

- lớp sáng tạo hiện là `sidecar`, chưa phải `native part of the flow`
- worker có thể bỏ qua hoàn toàn design mode dù task rõ là creative
- khó audit xem page được build theo mode nào

#### File refs

- `08-design-intelligence/Design Intelligence Operating Model.md`
- `08-design-intelligence/Design Mode Router.md`
- `05-flows/UI Build Script.md`
- `06-templates/Page Plan Template.md`

### 3. [Medium] Ownership giữa Design Language và Design Intelligence còn chồng nhau

#### Bằng chứng

- `03-factory/Design Language Reference.md` hiện vừa:
  - nói về nguồn tham khảo ngoài
  - nói về cách hấp thụ design system
  - trỏ sang `08-design-intelligence`
- `08-design-intelligence/Reference Sources.md` cũng lại định nghĩa:
  - cách dùng nguồn ngoài
  - cách “chôm khéo”
  - vai trò từng repo

#### Tác hại

- cùng một luật có hai chỗ để sửa
- dễ lệch khi update
- người mới khó biết file nào là chủ cho `source usage`

#### File refs

- `03-factory/Design Language Reference.md`
- `08-design-intelligence/Reference Sources.md`

### 4. [Medium] Quy ước lưu artifact theo task chưa đủ chặt

#### Bằng chứng

- luật bắt nhiều output
- template mới chỉ cover một phần
- chưa có file nào chốt rõ:
  - mỗi task UI lưu artifact ở đâu
  - tên file theo format nào
  - page-specific docs nằm folder nào
  - report nào là bắt buộc, report nào là optional

#### Tác hại

- page sau càng nhiều thì kho docs càng khó quét
- token đọc tăng
- AI mới vào khó biết cần đọc file nào của một task cụ thể

#### File refs

- `01-platform/Operating Law.md`
- `05-flows/UI Build Script.md`
- `06-templates/README.md`

### 5. [Low] Có lỗi hygiene nhỏ ở lớp design reference

#### Bằng chứng

- `03-factory/Design Language Reference.md` đang lặp tên nguồn tham khảo ngoài hai lần trong phần nguồn tham khảo mặc định

#### Tác hại

- không nguy hiểm
- nhưng làm giảm cảm giác gọn và chuẩn

#### File refs

- `03-factory/Design Language Reference.md`

## Điểm Mạnh Hiện Tại

1. `START HERE -> platform -> factory -> flows -> templates` là khung đọc khá tốt.
2. `Operating Law + UI Build Script + Final QA` đã tạo được khung vận hành chặt.
3. `Typography` và `Spacing` đã được nâng thành layer thật, không còn là ý niệm rời.
4. `No Repeat Law + Recent Page Memory` là một lớp kiểm soát novelty đáng giá.
5. `08-design-intelligence` được tách riêng là quyết định đúng về kiến trúc.

## Ưu Tiên Sửa Tiếp Theo

### Ưu tiên 1

Tạo thêm template cho:

- `Native Build Output`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

### Ưu tiên 2

Cắm `Design Intelligence` vào `Page Plan Template` và `UI Build Script`.

### Ưu tiên 3

Tách ranh giới ownership:

- `03-factory/Design Language Reference.md`
  - chỉ giữ vai trò `dịch design language sang Flatsome`
- `08-design-intelligence/Reference Sources.md`
  - giữ vai trò `source usage rule`

### Ưu tiên 4

Tạo một file kiểu:

- `01-platform/Artifact Storage Rule.md`

để chốt:

- task docs lưu đâu
- format tên file
- file nào bắt buộc
- file nào optional

## Phán Quyết CEO

Hệ hiện tại `đủ mạnh để dùng tiếp`, nhưng `chưa đủ kín` để scale lâu dài mà không phát sinh lệch chuẩn.

Nếu vá đúng 4 việc ưu tiên trên, hệ sẽ:

- nhất quán hơn
- dễ đọc hơn
- dễ train AI mới hơn
- dễ tự động hóa hơn
