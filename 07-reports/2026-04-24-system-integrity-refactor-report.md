# System Integrity Refactor Report

Date: 2026-04-24

## Mục Đích

Chốt kết quả rà soát tính toàn vẹn của toàn bộ hệ `flatsome-native` sau nhiều vòng chỉnh sửa.

Report này tập trung vào:

- tính nhất quán giữa `law -> flow -> template -> storage`
- việc có bị rơi artifact hay không
- việc layer `Design Intelligence` có chồng ownership với `Factory` hay không
- việc lớp tri thức lõi có bị lẫn brand/page-specific hay không

## Những Gì Đã Sửa

### 1. Vá nhóm template còn thiếu

Đã có đủ:

- `06-templates/Native Build Output Template.md`
- `06-templates/Audit Checklist Template.md`
- `06-templates/Fix Pass Template.md`
- `06-templates/Final Verification Template.md`

### 2. Nối luật lưu artifact vào hệ chính

Đã thêm và nối:

- `01-platform/Artifact Storage Rule.md`

Các entry/file lõi đã tham chiếu tới rule này:

- `README.md`
- `START HERE.md`
- `01-platform/README.md`
- `01-platform/Operating Law.md`
- `05-flows/README.md`
- `05-flows/UI Build Script.md`
- `06-templates/README.md`

### 3. Cắm `Design Intelligence` vào flow build

Đã có mặt trong:

- `05-flows/Brief Intake Flow.md`
- `05-flows/UI Build Script.md`
- `06-templates/Page Plan Template.md`
- `05-flows/Final QA Checklist.md`

Các trường đã hiện diện xuyên suốt:

- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`

### 4. Tách ownership giữa `Factory` và `Design Intelligence`

Kết quả sau refactor:

- `03-factory/Design Language Reference.md`
  - giữ vai trò `dịch ngôn ngữ thiết kế sang quyết định build Flatsome`
- `08-design-intelligence/Reference Sources.md`
  - giữ vai trò `source usage rule`
  - giữ rule hấp thụ repo ngoài

Điểm này giúp tránh lặp ý và tránh 2 file cùng làm một việc.

### 5. Dọn nhiễu brand-specific khỏi lớp core

Đã loại ví dụ `Primeland` khỏi:

- `03-factory/Block Registry.md`

Sau kiểm tra tươi mới, các thư mục lõi sau không còn match:

- `01-platform/`
- `03-factory/`
- `05-flows/`
- `06-templates/`
- `08-design-intelligence/`
- `README.md`
- `START HERE.md`

với các từ khóa:

- `Primeland`
- `primeland`
- `Obsidian`
- `sync`

### 6. Siết lại quan hệ giữa template và artifact

`06-templates/README.md` đã được sửa để phân biệt rõ:

- `template file`
- `artifact đầu ra`

thay vì diễn đạt mơ hồ kiểu task phải “có template”.

### 7. Làm rõ đường lưu ngoại lệ hiếm

`01-platform/Artifact Storage Rule.md` đã bổ sung rõ:

- `07-reports/exceptions/`

Điều này khớp với:

- `01-platform/Exception Registry.md`
- `05-flows/UI Build Script.md`
- `06-templates/Exception Report Template.md`
- `07-reports/exceptions/README.md`

## Kiểm Tra Đã Chạy

Đã rà bằng `rg` cho các nhóm sau:

- `Artifact Storage Rule`
- `Design Mode`
- `Style family`
- `Pattern family`
- `Typography mood`
- `Spacing rhythm`
- `Motion profile`
- `Anti-patterns cần tránh`
- tên 4 template mới
- `08-design-intelligence/Reference Sources.md`
- `03-factory/Design Language Reference.md`
- rule ngoại lệ hiếm

## Kết Luận Kiểm Tra

### Pass

- entry points đã nối đúng về source of truth
- flow build đã nhận đủ lớp `Design Intelligence`
- template layer không còn thiếu 4 artifact quan trọng
- ownership giữa `Factory` và `Design Intelligence` đã rõ hơn
- storage rule đã được cắm vào lớp law, flow, onboarding
- lớp core không còn ví dụ brand-specific rõ ràng đã phát hiện trước đó

### Rủi Ro Còn Lại

1. `07-reports/Recent Page Memory.md` vẫn là trí nhớ vận hành theo page thật, nên còn chứa tên page cụ thể.
2. Một số report lịch sử vẫn nhắc lại issue cũ; điều này là đúng vai trò report lịch sử, không phải lỗi của lớp core.
3. `01-platform/Artifact Storage Rule.md` hiện cho phép `Page Plan` nằm chung spec hoặc file riêng; linh hoạt nhưng đòi hỏi kỷ luật naming tốt để không rơi file ở layer task.

## Phán Quyết Toàn Vẹn

`Đạt` cho mục tiêu hiện tại.

Hệ thống hiện đã:

- nhất quán hơn
- ít chồng chéo hơn
- dễ đọc hơn cho AI worker
- khó rơi artifact hơn

và chưa thấy dấu hiệu mất mảnh tri thức lõi nào trong lớp vận hành chính sau vòng refactor này.
