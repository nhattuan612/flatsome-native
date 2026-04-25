# Official Demo Surface Ingestion Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Nạp thêm tri thức có giá trị vận hành từ official demo Flatsome vào knowledge hub mà không làm loãng hệ thống bằng catalogue dư thừa.

**Architecture:** Chỉ đưa vào những gì thật sự giúp sản xuất: `official source layer`, `officially confirmed native surfaces`, `pattern archetypes`, `effect/surface confirmations`, và `factory implications`. Không đưa brand copy, không nhét toàn bộ demo page vào platform layer, không bịa syntax khi chưa có capture chắc chắn.

**Tech Stack:** Markdown docs trong `VPS/docs/superpowers/flatsome-native`, official demo pages tại `demos.flatsome.com`, existing language map, factory docs, reports.

---

### Task 1: Ghi plan và khóa scope cập nhật

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/04-plans/2026-04-24-official-demo-surface-ingestion-plan.md`

- [ ] Xác nhận scope cập nhật chỉ gồm:
  - `official demo source layer`
  - `officially confirmed native surfaces`
  - `officially observed patterns`
  - `factory-level reusable implications`
- [ ] Giữ nguyên luật:
  - không gắn với domain cụ thể
  - không gắn với page test cụ thể
  - không bịa shortcode syntax nếu chưa có bằng chứng đủ chắc

### Task 2: Bổ sung official demo source layer

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/01-Overview and Source Rules.md`

- [ ] Thêm lớp nguồn `Official Flatsome demo surfaces`
- [ ] Liệt kê các nhóm nguồn chính:
  - `features/ux-page-builder`
  - `features/elements-overview`
  - `features/blocks-element`
  - `features/footer-features`
  - `features/blog-features`
  - `features/portfolio-features`
  - `elements/*`
- [ ] Ghi rõ giá trị của lớp nguồn này:
  - xác nhận element/surface tồn tại thật
  - xác nhận pattern vận hành
  - không tự động tương đương với full shortcode parameter map

### Task 3: Bổ sung official-confirmed native surfaces vào language map

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/04-Commerce and Dynamic.md`
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/05-Aliases and Broad Surface.md`

- [ ] Tách rõ `đã có syntax chắc` và `official demo confirmed but syntax capture still pending`
- [ ] Bổ sung media/interaction surfaces có giá trị cao:
  - `lightbox`
  - `hotspot`
  - `flip book`
  - `video button`
  - `message box`
- [ ] Bổ sung dynamic/content surfaces được official demo xác nhận:
  - `forms`
  - `search box`
  - `tabs`
  - `map`
  - `price table`
  - `team member`
  - `portfolio`
  - `logo`
  - `product categories`
  - `products`
  - `pages`
- [ ] Với surface nào chưa có syntax chắc:
  - ghi rõ `syntax capture pending`
  - chỉ ghi `purpose` và `operating value`

### Task 4: Bổ sung pattern và factory implication

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/06-Patterns and Workflow.md`
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Section Archetypes.md`
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Composition Rules.md`

- [ ] Bổ sung các pattern official demo xác nhận:
  - `lookbook / hotspot story`
  - `editorial blog slider / post teaser`
  - `shop hero + category discovery`
  - `footer replace bằng block`
  - `header/blog/shop/category reusable block surfaces`
- [ ] Ghi rõ pattern nào là:
  - `platform pattern`
  - `factory archetype`
  - `operating surface`

### Task 5: Bổ sung effect/surface confirmations ngoài data harvest

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/Effects.md`

- [ ] Thêm một phần riêng cho:
  - `Official demo confirmations beyond harvested exports`
- [ ] Chỉ bổ sung các effect/surface đáng nhớ:
  - `sticky section`
  - `section masks`
  - `lightbox behavior`
  - `flip book interaction`
  - `hotspot interaction`
  - `video button surface`
- [ ] Giữ tách biệt với phần `data-driven harvested attributes`

### Task 6: Ghi report tổng cho đợt nạp này

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/07-reports/Official Demo Surface Ingestion Report.md`

- [ ] Ghi:
  - nguồn đã đọc
  - menu đã quét
  - nhóm tri thức mới thực sự đáng giữ
  - phần nào không đáng nạp
  - file nào đã cập nhật

### Task 7: Verify cuối

**Files:**
- Verify only

- [ ] Mở lại các file vừa sửa để kiểm:
  - không lẫn brand/project cụ thể
  - không bịa syntax
  - không biến platform layer thành catalogue nặng
  - các bổ sung có giá trị vận hành rõ ràng
- [ ] Chạy:
  - `rg -n "syntax capture pending|Official demo|official demo|hotspot|flip book|lightbox|section masks|sticky section" VPS/docs/superpowers/flatsome-native`
- [ ] Kỳ vọng:
  - các khái niệm mới xuất hiện ở đúng file
  - không có nhắc tới domain dự án cụ thể
