# Unresolved Surface Hunt Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Chốt trạng thái thật cho `hotspot`, `flip book`, `message box` mà không bịa syntax.

**Architecture:** Dùng đủ 3 tầng chứng cứ: `official demo text`, `harvested exports`, `runtime extraction attempt`. Nếu vẫn không có shortcode thật, ghi đúng là `official surface / pattern only / syntax unresolved`.

**Tech Stack:** Markdown docs trong `VPS/docs/superpowers/flatsome-native`, `VPS/data/flatsome-studio/exports`, public demo pages `demos.flatsome.com`.

---

### Task 1: Ghi plan và khóa luật

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/04-plans/2026-04-24-unresolved-surface-hunt-plan.md`

- [ ] Chỉ xác nhận syntax khi có shortcode thật
- [ ] Nếu chỉ có official demo text thì chỉ được nâng lên `surface` hoặc `pattern`
- [ ] Nếu runtime extraction không chạy được trong môi trường hiện tại thì phải ghi rõ giới hạn đó

### Task 2: Cập nhật entry của 3 surface khó

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`

- [ ] Ghi rõ cho `hotspot`:
  - official demo text xác nhận dùng với `banner + hotspot + slider`
  - chưa có shortcode thật trong harvested exports
- [ ] Ghi rõ cho `flip book`:
  - official demo xác nhận surface tồn tại
  - chưa có shortcode thật trong harvested exports
- [ ] Ghi rõ cho `message box`:
  - official demo xác nhận CTA/callout use case
  - chưa có shortcode thật trong harvested exports

### Task 3: Ghi report và cập nhật report cũ

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/07-reports/Official Surface Syntax Capture Report.md`
- Create: `VPS/docs/superpowers/flatsome-native/07-reports/Unresolved Surface Hunt Report.md`

- [ ] Ghi:
  - đã tìm ở đâu
  - thấy gì từ official demo text
  - không thấy gì trong harvested exports
  - runtime extraction attempt failed in current environment
  - kết luận vận hành cho từng surface

### Task 4: Verify cuối

**Files:**
- Verify only

- [ ] Chạy:
  - `rg -n "hotspot|flip book|message box|runtime extraction|syntax unresolved|pattern only" VPS/docs/superpowers/flatsome-native`
- [ ] Kỳ vọng:
  - 3 surface được mô tả rõ ràng hơn
  - không có syntax bịa thêm
