# Flatsome Knowledge Hub Readability Refactor Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Tối ưu kho `flatsome-native` để AI và người đọc nắm nhanh hơn, tốn ít token hơn, nhưng không làm mất tri thức đã tích lũy.

**Architecture:** Giữ nguyên source of truth hiện tại, đưa raw evidence nặng sang lớp archive rõ ràng, biến `01-platform/Native Builder Language Map.md` thành file vào cổng gọn hơn, và tách nội dung nặng thành các file nhóm nhỏ có logic đọc tuần tự.

**Tech Stack:** Markdown docs, local filesystem, existing `flatsome-native` knowledge hub.

---

### Task 1: Chuẩn bị cấu trúc mới

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/04-plans/Knowledge Hub Readability Refactor Plan.md`
- Create: `VPS/docs/superpowers/flatsome-native/09-archive/README.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/README.md`

- [ ] Tạo plan và thư mục mới cho `native-builder-language` và `09-archive`
- [ ] Xác nhận không đụng dữ liệu harvest gốc

### Task 2: Bảo toàn tri thức cũ

**Files:**
- Archive or remove raw project-specific evidence so it does not stay in the reusable system layer

- [ ] Sao lưu nguyên bản full map cũ vào archive
- [ ] Loại project-specific artifacts khỏi lớp tri thức tái sử dụng
- [ ] Cập nhật các reference sau khi dọn archive/history

### Task 3: Tách map để đọc nhanh

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/Native Builder Language Map.md`
- Create: `VPS/docs/superpowers/flatsome-native/START HERE.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/01-Overview and Source Rules.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/02-Layout and Structure.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/03-Content and Media.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/04-Commerce and Dynamic.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/05-Aliases and Broad Surface.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/native-builder-language/06-Patterns and Workflow.md`

- [ ] Tạo file vào cổng ngắn cho người và AI
- [ ] Tách nội dung map thành các nhóm logic nhỏ hơn
- [ ] Giữ rõ quy tắc `section-first`, `>=90% native`, và scope của từng file

### Task 4: Cập nhật navigation và verify

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/README.md`
- Modify: reusable navigation and report references that remain after cleanup

- [ ] Cập nhật README gốc để phản ánh cấu trúc mới
- [ ] Gỡ các project profile links không còn phù hợp với system layer
- [ ] Verify không còn ref cũ tới artifact path cũ
- [ ] Verify `START HERE` và `01-platform/Native Builder Language Map.md` đủ để dẫn người đọc sang đúng file
