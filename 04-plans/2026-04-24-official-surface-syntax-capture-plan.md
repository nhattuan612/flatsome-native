# Official Surface Syntax Capture Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Nâng nhóm `officially confirmed surfaces` lên mức `syntax-complete` ở đâu có bằng chứng đủ chắc từ official docs hoặc harvested exports.

**Architecture:** Dùng `official docs` cho syntax có tài liệu rõ và `harvested exports` cho syntax thực chiến trong Studio. Nếu không có đủ bằng chứng, giữ `syntax capture pending` hoặc chuyển thành `pattern` thay vì bịa shortcode.

**Tech Stack:** Markdown docs trong `VPS/docs/superpowers/flatsome-native`, `VPS/data/flatsome-studio/exports`, official docs `docs.uxthemes.com`.

---

### Task 1: Ghi plan và khóa luật chứng cứ

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/04-plans/2026-04-24-official-surface-syntax-capture-plan.md`

- [ ] Chỉ nâng một surface lên `syntax-complete` khi có:
  - official docs rõ syntax
  - hoặc harvested export có shortcode thật
- [ ] Nếu không có chứng cứ đủ:
  - giữ `syntax capture pending`
  - hoặc đổi sang `pattern native composition`

### Task 2: Capture syntax nhóm content/media

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`

- [ ] Bổ sung syntax thật cho:
  - `lightbox`
  - `video_button`
  - `logo`
- [ ] Giữ `hotspot`, `flip book`, `message box` ở trạng thái pending nếu chưa có shortcode thật

### Task 3: Capture syntax nhóm dynamic/content engine

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/04-Commerce and Dynamic.md`

- [ ] Bổ sung syntax thật cho:
  - `map`
  - `tabgroup`
  - `tab`
  - `team_member`
  - `ux_portfolio`
- [ ] Làm rõ:
  - `forms` hiện bám chính vào `contact-form-7`
  - `price table` hiện là native composition pattern, chưa xác minh shortcode riêng

### Task 4: Cập nhật report ingest cũ và ghi report capture mới

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/07-reports/Official Demo Surface Ingestion Report.md`
- Create: `VPS/docs/superpowers/flatsome-native/07-reports/Official Surface Syntax Capture Report.md`

- [ ] Cập nhật report ingest để phản ánh phần nào đã được syntax capture
- [ ] Ghi report mới:
  - nguồn bằng chứng
  - surface nào lên `syntax-complete`
  - surface nào vẫn `pending`
  - surface nào bị đổi thành `pattern`

### Task 5: Verify cuối

**Files:**
- Verify only

- [ ] Mở lại các file vừa sửa
- [ ] Chạy:
  - `rg -n "syntax capture pending|tabgroup|team_member|ux_portfolio|\\[map |\\[lightbox |\\[logo |\\[video_button" VPS/docs/superpowers/flatsome-native`
- [ ] Kỳ vọng:
  - syntax mới chỉ xuất hiện ở các entry đúng
  - `price table` không bị mô tả như shortcode riêng nếu chưa có bằng chứng
