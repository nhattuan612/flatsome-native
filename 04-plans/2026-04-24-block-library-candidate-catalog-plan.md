# Block Library Candidate Catalog Implementation Plan

> **For AI workers:** Execute this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Tách riêng danh sách `block library candidates` khỏi `Block Registry` để worker có inventory rõ ràng khi chọn block tái dùng cho page plan mới.

**Architecture:** `Block Registry` giữ luật quản trị. `Block Library Candidates` giữ inventory ứng viên theo mức ưu tiên, độ tái dùng và trạng thái sẵn sàng. `Page Goal Routing` chỉ trỏ sang các ứng viên đúng mục tiêu.

**Tech Stack:** Markdown docs trong `./`, existing factory docs, templates và reports.

---

### Task 1: Ghi plan và khóa scope

**Files:**
- Create: `04-plans/2026-04-24-block-library-candidate-catalog-plan.md`

- [ ] Không tạo block implementation cụ thể
- [ ] Chỉ tạo catalog ứng viên
- [ ] Không gắn project cụ thể

### Task 2: Tạo catalog ứng viên block

**Files:**
- Create: `03-factory/Block Library Candidates.md`

- [ ] Tạo inventory theo:
  - `Tên ứng viên`
  - `Archetype nguồn`
  - `Loại block đề xuất`
  - `Mức ưu tiên`
  - `Khả năng tái dùng`
  - `Đầu vào có thể thay`
  - `Trạng thái sẵn sàng`
  - `Ghi chú`

### Task 3: Nối catalog vào registry, routing và start file

**Files:**
- Modify: `03-factory/Block Registry.md`
- Modify: `03-factory/Page Goal Routing.md`
- Modify: `START HERE.md`

- [ ] `Block Registry` trỏ sang catalog mới
- [ ] `Page Goal Routing` nhắc kiểm catalog trước khi đề xuất block mới
- [ ] `START HERE` đưa catalog vào đường đọc nhanh của AI worker

### Task 4: Ghi report tổng

**Files:**
- Create: `07-reports/Block Library Candidate Catalog Report.md`

- [ ] Ghi:
  - catalog mới có gì
  - khác gì với registry
  - giá trị vận hành

### Task 5: Verify cuối

**Files:**
- Verify only

- [ ] Chạy:
  - `rg -n "Block Library Candidates|Mức ưu tiên|Trạng thái sẵn sàng|kiểm catalog block" ./`
- [ ] Kỳ vọng:
  - catalog mới xuất hiện đúng chỗ
  - registry/routing/start file đã liên kết với nó
