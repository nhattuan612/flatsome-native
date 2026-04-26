# HOW THIS HUB WORKS

Date: 2026-04-25

## Mục Đích

File này giải thích hub vận hành từ đầu tới cuối theo ngôn ngữ dễ đọc.

Nếu `MASTER OPERATING MEMORY.md` là bản nạp nhanh, thì file này là bản diễn giải.

## Hub Này Đang Giải Quyết Việc Gì

Hub này tồn tại để giúp AI và human operator tạo giao diện bằng `Flatsome UX Builder` một cách:

- có luật
- có flow
- có artifact
- có kiểm tra
- có khả năng mở lại để chỉnh sửa kéo thả

Nó không chỉ dạy `cú pháp shortcode`.
Nó dạy cả `cách route task`, `cách lên plan`, `cách build`, `cách kiểm`, và `cách lưu tri thức`.

## 5 Lớp Chính

### 1. Luật

Nằm ở `01-platform/`.

Đây là nơi định nghĩa:

- luật cứng
- syntax native
- scoring
- nơi lưu artifact
- rule cho exception

### 2. Thư viện Studio

Nằm ở `02-platform-studio-library/`.

Đây là lớp tri thức về:

- catalog template của Flatsome Studio
- effect
- page settings
- category map

### 3. Factory

Nằm ở `03-factory/`.

Đây là lớp biến brief thành cấu trúc build:

- route mục tiêu trang
- section archetype
- layout DNA
- layout pool
- hero family
- typography
- spacing
- anti-repeat

### 4. Flow

Nằm ở `05-flows/`.

Đây là lớp chỉ `làm theo thứ tự nào`.

Ví dụ:

- hỏi đầu vào thế nào
- route task ra sao
- build theo script nào
- kiểm cuối bằng checklist nào
- repair theo loop nào

### 5. Template

Nằm ở `06-templates/`.

Đây là lớp chốt `phải tạo ra giấy tờ gì`.

Ví dụ:

- `Page Plan`
- `Native Scoring`
- `Novelty Scoring`
- `Fix Pass`
- `Final Verification`

## Một Task Page Chạy Thực Tế Thế Nào

Trình tự chuẩn:

1. nhận brief
2. khóa task type
3. hỏi dẫn dắt để đủ input
4. khóa `Input Contract`
5. route sang kiểu build phù hợp
6. chốt `Page Plan`
7. build bằng native structure
8. audit
9. repair nếu fail
10. release khi pass
11. lưu artifact đúng chỗ

Viết ngắn gọn:

`Brief -> Route -> Page Plan -> Build -> Audit -> Repair -> Release`

## Vì Sao Không Được Nhảy Thẳng Vào Build

Vì nếu nhảy thẳng vào build, AI thường sai ở 4 chỗ:

- hiểu sai kỳ vọng `clone hay sáng tạo`
- lặp lại bố cục cũ
- đặt heading quá dài làm vỡ layout
- lưu nhầm artifact vào sai lớp

Cho nên hub buộc phải có:

- `Input Contract`
- `Novelty Gate`
- `Build Readiness Gate`
- `Repair Gate`

## Một Page Tốt Theo Hub Này Nghĩa Là Gì

Một page chỉ được xem là đạt khi:

- public ổn
- edit ổn
- builder mở lại được
- native structure còn nguyên
- không còn lỗi lớn
- artifact cuối đã lưu đúng chỗ

## System Docs Khác Gì Page Docs

### System docs

Là tri thức dùng chung cho nhiều task.

Nằm trong hub này:

- `01-platform/`
- `03-factory/`
- `05-flows/`
- `06-templates/`
- `08-design-intelligence/`

### Page docs

Là tài liệu gắn với một page hoặc một task cụ thể.

Không nằm trong lớp core của hub.
Chúng phải để ở:

- `specs/ (ngoài hub)`
- `reports/ (ngoài hub)`
- `tmp/ (ngoài hub, `

## Cách Cập Nhật Hub Mà Không Làm Rối

Nếu phát hiện lỗi luật:

- sửa `01-platform/`

Nếu phát hiện flow thiếu bước:

- sửa `05-flows/`

Nếu thấy artifact đang thiếu:

- sửa `06-templates/`

Nếu rút ra pattern build mới:

- cập nhật `03-factory/`

Nếu chỉ là bằng chứng task:

- ghi vào `07-reports/`

## Khi Nào Dùng Design Intelligence

Mặc định hệ bám `Flatsome Native Core`.

Chỉ mở `08-design-intelligence/` khi:

- cần tăng độ sáng tạo
- cần bám một design language ngoài
- user yêu cầu reinterpret thay vì clone

## Cách Đọc Ít Mà Vẫn Hiểu Đúng

Nếu là người mới:

1. `PUBLIC READER GUIDE.md`
2. `AI HANDOFF GUIDE.md`
3. `MASTER OPERATING MEMORY.md`
4. `05-flows/Master System Flow Map.md`

## Kết Luận

Hub này là một hệ điều phối tri thức cho `Flatsome Native Builder`.

Nó chỉ hiệu quả khi người dùng và AI cùng tôn trọng:

- luật
- flow
- artifact
- ranh giới giữa source of truth và history
