# MASTER OPERATING MEMORY

Date: 2026-04-25

## Mục Đích

Đây là file nạp nhanh toàn bộ hệ `flatsome-native` cho AI ở phiên chat khác.

Nếu chỉ được đọc `1 file` trước khi bắt đầu, hãy đọc file này.

Nếu cần bản diễn giải dễ đọc hơn cho public repo hoặc AI handoff, mở thêm:

- `V1.1 RELEASE GUIDE.md`
- `PUBLIC READER GUIDE.md`
- `AI HANDOFF GUIDE.md`
- `HOW THIS HUB WORKS.md`
- `SKILL SURFACE MAP.md`

## Skill Surface Đã Chốt

Hệ đóng gói gọn ở `3 skill`:

- `flatsome-native-builder_(Build_Trang)`
- `flatsome-native-harvest_(Hoc_Them_UI)`
- `flatsome-native-design-intelligence_(Sang_Tao)`

Map nội bộ:

- `builder`
  - build page
- `harvest`
  - học thêm UI, hút thêm tri thức
- `design-intelligence`
  - tăng sáng tạo, đổi design language

AI nên đọc:

- `SKILL SURFACE MAP.md`

trước khi quyết định gọi skill nào.

## Mục Tiêu Tối Cao

Toàn bộ hệ tồn tại để bảo đảm:

- `section-first`
- `native >= 90%`
- output mở lại được bằng `Flatsome UX Builder`
- AI có thể code bằng ngôn ngữ của chính Flatsome Builder

## Capability Input Hiện Có

Hệ hiện hỗ trợ:

- nhận người dùng mới bằng `quick start menu`
- hỏi dẫn dắt theo `guided intake questions`
- nhận `text thường` rồi route sang build native
- nhận `ảnh` để route `clone` hoặc `reinterpret`
- nhận `markdown spec` để route `rebuild`
- nhận `link tham chiếu`
- nhận `mixed input`
- nhận brief ngắn và dùng `Flatsome Native Core` làm mặc định an toàn
- nhận yêu cầu sáng tạo mạnh và mở `08-design-intelligence/` khi cần

## Chuỗi Vận Hành Chuẩn

Flow lõi không đổi:

`Brief -> Route -> Page Plan -> Build -> Audit -> Repair -> Release`

Mặc định phải đi qua:

- `05-flows/Task Type Router.md`
- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`
- `05-flows/Master System Flow Map.md`
- `05-flows/Brief Intake Flow.md`
- `03-factory/Task Route Matrix.md`
- `03-factory/Page Goal Routing.md`
- `06-templates/Page Plan Template.md`
- `05-flows/UI Build Script.md`
- `05-flows/Final QA Checklist.md`

## Source Of Truth Thật

### Luật và ngôn ngữ

- `01-platform/`

### Factory và anti-repeat

- `03-factory/`

### Flow vận hành

- `05-flows/`

### Biểu mẫu chuẩn

- `06-templates/`

## Không Phải Source Of Truth

### Chỉ là kế hoạch hệ thống

- `04-plans/`

### Chỉ là evidence và history

- `07-reports/`
- `09-archive/`

### Ngoại lệ hẹp duy nhất

- `07-reports/Recent Page Memory.md`
  - không phải luật
  - nhưng là dữ liệu bắt buộc cho novelty gate

## Thứ Tự Đọc Nhanh

1. `MASTER OPERATING MEMORY.md`
2. `START HERE.md`
3. `05-flows/Task Type Router.md`
4. `05-flows/Quick Start Menu.md`
5. `05-flows/Guided Intake Questions.md`
6. `05-flows/Input Contract.md`
7. `05-flows/Master System Flow Map.md`
8. `05-flows/Brief Intake Flow.md`
9. `03-factory/Task Route Matrix.md`
10. `01-platform/Operating Law.md`
11. `01-platform/Native Builder Language Map.md`
12. `01-platform/Artifact Storage Rule.md`
13. `03-factory/Page Goal Routing.md`
14. `03-factory/Layout DNA.md`
15. `03-factory/Layout Pool.md`
16. `03-factory/No Repeat Law.md`
17. `05-flows/UI Build Script.md`
18. `05-flows/Final QA Checklist.md`
19. `06-templates/README.md`
20. `07-reports/Recent Page Memory.md`

## Folder Map Ngắn Gọn

- `01-platform/`
  - luật cứng
  - syntax native
  - scoring
  - storage
  - ngoại lệ
- `02-platform-studio-library/`
  - catalog Studio
  - effects
  - page settings
- `03-factory/`
  - route brief -> skeleton -> archetype
  - design language translation
  - typography
  - spacing
  - layout DNA / pool / hero rotation
  - anti-repeat
- `04-plans/`
  - system-upgrade plans only
- `05-flows/`
  - task type router
  - quick start menu
  - guided intake questions
  - input contract
  - master system flow map
  - best-result playbook
  - build flow
  - harvest flow
  - extraction flow
  - execution role boundaries
- `06-templates/`
  - page plan
  - scoring
  - audit / fix / verification
- `07-reports/`
  - evidence
  - audits
  - reports
- `08-design-intelligence/`
  - optional creativity layer
- `09-archive/`
  - heavy history / raw evidence

## Gói Artifact Bắt Buộc Cho Mọi Task UI

Mọi task UI phải có:

- `Spec`
- `Input Contract`
- `Page Plan`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

Nơi lưu xem tại:

- `01-platform/Artifact Storage Rule.md`

## Novelty Gate

Trước khi build phải chốt:

- `Layout DNA`
- `Layout Pool`
- `Hero Family`
- `Section Order Recipe`
- `Similarity Risk`
- `Novelty Score dự kiến`

Không được build nếu:

- `Similarity Risk = Blocked`
- `Novelty Score dự kiến < 10`

## Design Intelligence Dùng Khi Nào

Chỉ mở `08-design-intelligence/` khi:

- user muốn sáng tạo mạnh hơn
- user muốn theo một design language cụ thể
- cần đề xuất nhiều hướng thiết kế

Nếu không có yêu cầu sáng tạo rõ, mặc định bám:

- `Flatsome Native Core`

## Route Cứng Trước Khi Build

Trước khi build phải khóa:

- `loại input`
- `output expectation`
- `style source`
- `reference authority`

Nếu chưa khóa 4 mục này:

- chưa được sang `Page Plan`

## Điều Đã Chốt Và Không Nên Tranh Luận Lại

- `UX Builder shortcode-native` là hướng chính
- không dùng HTML làm layout chính
- `ux_html` chỉ cho iframe/embed/link/map hoặc ngoại lệ hiếm
- CSS ưu tiên ở `Theme Options`
- build phải mở lại được bằng builder
- report không được thay luật
- page-specific implementation plan không được nằm trong `04-plans/`

## Sai Lầm Cũ Đã Bỏ

- batch import trên một page duy nhất và tin `controller.progress === 100`
- dùng report cũ như thể là luật hiện hành
- để page-specific plan chen vào `04-plans/`
- tham chiếu filename rút gọn làm AI phải đoán file nằm ở đâu
- để file platform trộn cả syntax, workflow extract, và vai trò agent trong cùng một chỗ

## Hiệu Suất Mong Đợi Sau Refactor

- AI mới vào ít phải dò thư mục hơn
- ít token waste vì có `1` file master
- ít đọc nhầm report/history hơn
- route tài liệu rõ hơn
- dễ scale thêm docs mới mà không lẫn lớp

## Current Known Gaps / V2 Backlog

- chưa chuẩn hóa `100%` tất cả filename-only references trong toàn bộ reports lịch sử
- một số plan/report lịch sử vẫn dùng naming convention cũ
- chưa tách riêng một lớp machine-readable manifest cho toàn hub
- chưa có automation check bắt buộc cho broken references

## Khi Cập Nhật Hệ

Nếu thay luật:

- sửa `01-platform/`

Nếu thay flow:

- sửa `05-flows/`

Nếu thay biểu mẫu:

- sửa `06-templates/`

Nếu chỉ thêm bằng chứng:

- ghi vào `07-reports/`

Nếu là page/task cụ thể (nằm ngoài Hub này):

- Lưu Spec tại thư mục Specs của dự án
- Lưu Report tại thư mục Reports của dự án
- (Ví dụ: `../specs/` hoặc `../reports/` tùy cấu trúc dự án của bạn)
