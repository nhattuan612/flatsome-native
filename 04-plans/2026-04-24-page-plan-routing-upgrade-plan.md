# Page Plan Routing Upgrade Implementation Plan

> **For AI workers:** Execute this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Chuẩn hóa tuyến đường từ brief sang build theo công thức `page goal -> skeleton -> archetype -> block candidate -> native build`.

**Architecture:** Không thêm syntax mới. Chỉ thêm lớp routing và chuẩn hóa Page Plan để mọi worker bắt đầu từ cùng một logic thay vì tự ứng biến.

**Tech Stack:** Markdown docs trong `./`, existing factory docs, page plan template, start file.

---

### Task 1: Ghi plan và khóa scope

**Files:**
- Create: `04-plans/2026-04-24-page-plan-routing-upgrade-plan.md`

- [ ] Chỉ nâng lớp routing và template
- [ ] Không thêm project-specific example
- [ ] Không tạo syntax mới

### Task 2: Tạo page-goal routing doc

**Files:**
- Create: `03-factory/Page Goal Routing.md`

- [ ] Tạo bảng route từ:
  - `Loại trang`
  - `Mục tiêu chính`
  - `Skeleton nên dùng`
  - `Archetype ưu tiên`
  - `Ứng viên block`
  - `Risk note`

### Task 3: Nâng Page Plan Template

**Files:**
- Modify: `06-templates/Page Plan Template.md`

- [ ] Thêm trường:
  - `Skeleton đã chọn`
  - `Archetype ưu tiên`
  - `Ứng viên block nên tái dùng`
  - `Ứng viên block nên tạo mới`
  - `Route lý do chọn`

### Task 4: Cập nhật START HERE và Composition Rules

**Files:**
- Modify: `START HERE.md`
- Modify: `03-factory/Composition Rules.md`

- [ ] Gắn `03-factory/Page Goal Routing.md` vào fast reading path
- [ ] Ghi rõ rule:
  - brief mới phải đi qua routing trước khi lập section map

### Task 5: Ghi report tổng

**Files:**
- Create: `07-reports/Page Plan Routing Upgrade Report.md`

- [ ] Ghi:
  - routing mới thêm
  - template thay đổi gì
  - giá trị vận hành

### Task 6: Verify cuối

**Files:**
- Verify only

- [ ] Chạy:
  - `rg -n "Page Goal Routing|Skeleton đã chọn|Archetype ưu tiên|Ứng viên block nên tái dùng|brief mới phải đi qua routing" ./`
- [ ] Kỳ vọng:
  - routing doc và template cùng dùng một logic
  - không có ví dụ gắn project cụ thể
