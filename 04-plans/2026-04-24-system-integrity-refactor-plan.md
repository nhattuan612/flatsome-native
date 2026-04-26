# System Integrity Refactor Implementation Plan

> **For AI workers:** Execute this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Vá các lỗ hổng flow đã audit để hệ Flatsome Native nhất quán hơn, dễ dùng hơn, và khó làm rơi artifact hơn sau nhiều lần chỉnh sửa.

**Architecture:** Refactor này chỉ tác động lớp tài liệu vận hành. Nó thêm các template còn thiếu, cắm `Design Intelligence` vào flow chính, tách ownership giữa các file đang chồng nhau, rồi thêm một luật lưu artifact làm source of truth cho toàn hệ.

**Tech Stack:** Markdown documentation, existing flatsome-native knowledge hub structure

---

### Task 1: Bổ Sung Template Còn Thiếu

**Files:**
- Create: `06-templates/Native Build Output Template.md`
- Create: `06-templates/Audit Checklist Template.md`
- Create: `06-templates/Fix Pass Template.md`
- Create: `06-templates/Final Verification Template.md`
- Modify: `06-templates/README.md`

- [ ] Tạo 4 template mới đúng tên artifact mà `Operating Law` và `Final QA Checklist` đang yêu cầu.
- [ ] Cập nhật `06-templates/README.md` để liệt kê đầy đủ toàn bộ template chuẩn.
- [ ] Bảo đảm tên template khớp thuật ngữ đang dùng trong law/flow/checklist.

### Task 2: Cắm Design Intelligence Vào Flow Chính

**Files:**
- Modify: `05-flows/Brief Intake Flow.md`
- Modify: `05-flows/UI Build Script.md`
- Modify: `06-templates/Page Plan Template.md`
- Modify: `05-flows/Final QA Checklist.md`

- [ ] Thêm bước `Design Mode` vào intake và build flow.
- [ ] Thêm field `Design Mode`, `Style family`, `Pattern family`, `Typography mood`, `Spacing rhythm`, `Motion profile`, `Anti-patterns cần tránh` vào `Page Plan Template`.
- [ ] Thêm tiêu chí QA để audit đúng mode sáng tạo đã chọn.
- [ ] Giữ `Flatsome Default` là mặc định khi không có yêu cầu sáng tạo rõ.

### Task 3: Tách Ownership Rõ Giữa Hai Lớp Design

**Files:**
- Modify: `03-factory/Design Language Reference.md`
- Modify: `08-design-intelligence/Reference Sources.md`
- Modify: `08-design-intelligence/README.md`

- [ ] Rút `03-factory/Design Language Reference.md` về đúng vai trò: dịch design language sang Flatsome.
- [ ] Giữ `08-design-intelligence/Reference Sources.md` là source of truth cho source usage rule và cách hấp thụ repo ngoài.
- [ ] Loại bỏ lặp ý và cleanup phần source reference bị trùng.

### Task 4: Thêm Luật Lưu Artifact

**Files:**
- Create: `01-platform/Artifact Storage Rule.md`
- Modify: `01-platform/README.md`
- Modify: `01-platform/Operating Law.md`
- Modify: `05-flows/UI Build Script.md`
- Modify: `README.md`
- Modify: `START HERE.md`

- [ ] Định nghĩa nơi lưu, naming, và tính bắt buộc/optional cho từng artifact task UI.
- [ ] Nối `01-platform/Artifact Storage Rule.md` vào law, flow, onboarding path.
- [ ] Bảo đảm người mới đọc vào biết lưu file ở đâu mà không phải đoán.

### Task 5: Rà Tính Toàn Vẹn Sau Refactor

**Files:**
- Create: `07-reports/2026-04-24-system-integrity-refactor-report.md`

- [ ] Rà references chéo bằng `rg` cho các thuật ngữ artifact, design mode, storage rule.
- [ ] Kiểm tra các file entry (`README`, `START HERE`, `01-platform/README`, `06-templates/README`, `08-design-intelligence/README`) còn nhất quán không.
- [ ] Ghi report ngắn mô tả đã sửa gì, còn rủi ro nào.
