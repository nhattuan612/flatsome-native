# Factory Pattern Upgrade Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Nâng lớp `factory` để dùng được ngay các surface đã xác minh syntax, giúp build nhanh hơn mà vẫn giữ `section-first`, `native-first`, và editability trong UX Builder.

**Architecture:** Không tạo syntax mới. Chỉ chuyển phần đã xác minh ở `language map` thành `section archetypes`, `page composition rules`, và `block governance` có thể tái sử dụng trên nhiều dự án.

**Tech Stack:** Markdown docs trong `VPS/docs/superpowers/flatsome-native`, existing `language map`, `factory`, và `reports`.

---

### Task 1: Ghi plan và khóa scope

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/04-plans/2026-04-24-factory-pattern-upgrade-plan.md`

- [ ] Chỉ dùng các surface đã có chứng cứ mạnh:
  - `map`
  - `tabgroup/tab`
  - `team_member`
  - `ux_portfolio`
  - `logo`
  - `video_button`
  - `blog_posts`
  - `ux_products`
  - `ux_product_categories`
- [ ] Không bịa thêm element mới
- [ ] Không gắn brand/project cụ thể

### Task 2: Mở rộng Section Archetypes

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Section Archetypes.md`

- [ ] Bổ sung archetype cho:
  - `contact split with map`
  - `team roster grid`
  - `portfolio showcase rail`
  - `tabbed FAQ / pricing panel`
  - `testimonial + logo proof rail`
  - `video trigger banner`
  - `instagram / social proof strip`

### Task 3: Mở rộng Composition Rules

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Composition Rules.md`

- [ ] Bổ sung skeleton cho:
  - `contact page`
  - `portfolio / case-study landing`
  - `service / agency page`
  - `pricing / faq page`
- [ ] Ghi rule chọn archetype theo page goal

### Task 4: Nâng Block Registry

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Block Registry.md`

- [ ] Bổ sung:
  - block nào nên ưu tiên tách block từ các archetype mới
  - naming rule cho block thư viện theo surface/mood/layout
  - tín hiệu khi một archetype nên nâng thành `Core Library Block`

### Task 5: Ghi report tổng

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/07-reports/Factory Pattern Upgrade Report.md`

- [ ] Ghi:
  - những archetype mới thêm
  - skeleton mới thêm
  - block governance mới
  - giá trị vận hành

### Task 6: Verify cuối

**Files:**
- Verify only

- [ ] Chạy:
  - `rg -n "contact split with map|team roster grid|portfolio showcase rail|tabbed FAQ|video trigger banner|instagram / social proof strip|pricing / faq page|Core Library Block" VPS/docs/superpowers/flatsome-native`
- [ ] Kỳ vọng:
  - concept mới nằm đúng file factory
  - không có project-specific copy
  - không mâu thuẫn với luật native hiện có
