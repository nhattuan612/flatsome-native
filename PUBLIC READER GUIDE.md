# PUBLIC READER GUIDE

Date: 2026-04-25

## Mục Đích

Đây là file dành cho người đọc công khai.

Nếu bạn vừa mở repo và muốn hiểu `flatsome-native` là gì, đọc file này trước.

## Flatsome Native Là Gì

Đây là một knowledge hub để giúp AI worker và human operator build giao diện bằng `Flatsome UX Builder` theo cách:

- có cấu trúc
- kéo thả chỉnh sửa lại được
- ưu tiên native elements của Builder
- giảm lệ thuộc vào `ux_html`

Mục tiêu không phải chỉ là tạo ra `1 page`.
Mục tiêu là tạo ra một hệ tri thức có thể dùng lặp lại trên nhiều dự án.

## Điều Gì Là Lõi Của Hệ

Ba ý quan trọng nhất:

- mọi UI đi theo `section-first`
- mọi thành phần nằm trong `section -> row -> col -> element`
- mặc định phải đạt `native >= 90%`

## Đọc Theo Đường Nào

### Đường ngắn nhất để hiểu toàn hệ

1. `README.md`
2. `MASTER OPERATING MEMORY.md`
3. `HOW THIS HUB WORKS.md`
4. `05-flows/Master System Flow Map.md`
5. `GITHUB PUBLIC CHECKLIST.md`

### Nếu muốn hiểu luật

1. `01-platform/README.md`
2. `01-platform/Operating Law.md`
3. `01-platform/Artifact Storage Rule.md`
4. `01-platform/Novelty Scoring Rule.md`

### Nếu muốn hiểu khả năng build

1. `03-factory/README.md`
2. `03-factory/Layout DNA.md`
3. `03-factory/Section Archetypes.md`
4. `03-factory/Typography System.md`
5. `03-factory/Spacing System.md`

### Nếu muốn hiểu flow làm việc

1. `05-flows/README.md`
2. `05-flows/Input Contract.md`
3. `05-flows/UI Build Script.md`
4. `05-flows/Final QA Checklist.md`

## Folder Nào Làm Gì

- `01-platform/`
  - luật cứng, syntax native, storage, scoring, exception
- `02-platform-studio-library/`
  - thư viện knowledge về catalog của Flatsome Studio
- `03-factory/`
  - tư duy dựng trang, anti-repeat, typography, spacing, layout
- `04-plans/`
  - kế hoạch nâng cấp hệ, không phải luật vận hành hằng ngày
- `05-flows/`
  - trình tự thao tác thực tế
- `06-templates/`
  - biểu mẫu chuẩn cho task UI
- `07-reports/`
  - audit, evidence, history
- `08-design-intelligence/`
  - lớp sáng tạo mở rộng, chỉ dùng khi cần
- `09-archive/`
  - lịch sử nặng, ngoài đường đọc chính

## Source Of Truth Nằm Ở Đâu

Đọc như sau:

- luật thật
  - `01-platform/`
- build factory thật
  - `03-factory/`
- flow vận hành thật
  - `05-flows/`
- artifact chuẩn thật
  - `06-templates/`

Không nên dùng các nơi sau làm luật:

- `04-plans/`
- `07-reports/`
- `09-archive/`

Ngoại lệ hẹp:

- `07-reports/Recent Page Memory.md`
  - đây không phải luật
  - nhưng là dữ liệu vận hành cho novelty gate

## Một Task UI Đi Qua Những Gì

Một task UI chuẩn đi theo:

`Brief -> Route -> Page Plan -> Build -> Audit -> Repair -> Release`

Và phải để lại các artifact chính:

- `Spec`
- `Input Contract`
- `Page Plan`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

## Public Reader Không Nên Hiểu Sai Điều Gì

- đây không phải bộ HTML template thuần
- đây không phải no-code drag-drop tùy hứng
- đây không lấy `report lịch sử` làm luật
- đây không coi `ux_html` là cách dựng layout chính

## Nếu Chỉ Có 10 Phút

Hãy đọc:

1. `V1.1 RELEASE GUIDE.md`
2. `MASTER OPERATING MEMORY.md`
3. `HOW THIS HUB WORKS.md`
4. `GITHUB PUBLIC CHECKLIST.md`

## Kết Luận

Muốn hiểu hub này đúng, phải nhìn nó như một `operating system for Flatsome-native work`, không phải chỉ là một folder tài liệu rời rạc.
