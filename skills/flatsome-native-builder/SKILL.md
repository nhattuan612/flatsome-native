---
name: flatsome-native-builder
description: Build trang Flatsome UX Builder theo quy trình chuẩn section-first, native >= 90%. Dùng khi cần tạo page mới, clone UI, hoặc rebuild từ brief/ảnh/link/markdown spec.
---

# flatsome-native-builder — Build Trang

## Mục Đích

Skill này là **cửa chính** của hệ `flatsome-native`.

Dùng khi:
- build page mới bằng `Flatsome UX Builder`
- clone hoặc rebuild UI từ brief, ảnh, link, markdown spec
- tạo `Page Plan`, build native, audit, repair, release

Không dùng khi:
- mục tiêu chính là hút thêm thư viện UI → dùng `flatsome-native-harvest`
- mục tiêu chính là sáng tạo mạnh hoặc đổi design language → dùng `flatsome-native-design-intelligence`

## Call Phrase

```
use flatsome-native-builder_(Build_Trang)
```

## Luật Cứng Phải Nạp Trước Khi Làm

- `section-first`
- `section -> row -> col -> element`
- `native >= 90%`
- không dùng `ux_html` làm layout shell chính
- output phải mở lại được bằng `Flatsome UX Builder`
- không dùng report thay cho law

## Thứ Tự Đọc Tối Thiểu

Đọc theo thứ tự này trước khi bắt đầu task:

1. `MASTER OPERATING MEMORY.md`
2. `START HERE.md`
3. `05-flows/Task Type Router.md`
4. `05-flows/Quick Start Menu.md`
5. `05-flows/Guided Intake Questions.md`
6. `05-flows/Input Contract.md`
7. `05-flows/Brief Intake Flow.md`
8. `03-factory/Task Route Matrix.md`
9. `01-platform/Operating Law.md`
10. `01-platform/Native Builder Language Map.md`
11. `06-templates/Page Plan Template.md`
12. `05-flows/UI Build Script.md`
13. `05-flows/Final QA Checklist.md`

## Flow Chuẩn

```
Brief -> Route -> Page Plan -> Build -> Audit -> Repair -> Release
```

### Trước Khi Sang Page Plan — Phải Khóa

- `loại input` (text / ảnh / link / markdown / mixed)
- `output expectation` (new page / clone / rebuild)
- `style source` (Flatsome Native Core / design language cụ thể)
- `reference authority`
- `CTA chính`
- `thiết bị ưu tiên`

Nếu thiếu: ghi `không xác định`, dùng default an toàn, không tự bịa.

### Novelty Gate — Chốt Trước Khi Build

- `Layout DNA`
- `Layout Pool`
- `Hero Family`
- `Section Order Recipe`
- `Similarity Risk`
- `Novelty Score dự kiến`

Không được build nếu `Similarity Risk = Blocked` hoặc `Novelty Score dự kiến < 10`.

## Artifact Bắt Buộc Cho Mỗi Task

- `Spec`
- `Input Contract`
- `Page Plan`
- `Native Build Output`
- `Native Scoring`
- `Novelty Scoring`
- `Audit Checklist`
- `Fix Pass`
- `Final Verification`

Nơi lưu: xem `01-platform/Artifact Storage Rule.md`

## Check Trước Khi Báo Xong

- builder mở lại được
- public page ổn
- edit page ổn
- không còn lỗi blocking
- artifact lưu đúng nơi

## Hub Reference

Repo: https://github.com/nhattuan612/flatsome-native
File chính: `MASTER OPERATING MEMORY.md`, `START HERE.md`
