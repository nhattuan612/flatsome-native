# Flatsome Native Knowledge Hub

Date: 2026-04-25

## Purpose

This is the company knowledge hub for `Flatsome shortcode-native` work.

It exists to keep all durable Flatsome knowledge in one folder for:

- Codex production work
- OpenClaw operator work
- local backup inside `VPS/docs`
- cross-session AI onboarding with minimal token waste

## Canonical Skill Identity

Nếu đóng gói bộ tri thức này thành skill cho Codex hoặc AI worker khác, lớp skill surface được chốt là `3 skill`.

File giải thích đầy đủ:

- `SKILL SURFACE MAP.md`

### Canonical ID

- `flatsome-native-builder`
- `flatsome-native-harvest`
- `flatsome-native-design-intelligence`

### Display Label

- `flatsome-native-builder_(Build_Trang)`
- `flatsome-native-harvest_(Hoc_Them_UI)`
- `flatsome-native-design-intelligence_(Sang_Tao)`

### Call Phrase

- `use flatsome-native-builder_(Build_Trang)`
- `use flatsome-native-harvest_(Hoc_Them_UI)`
- `use flatsome-native-design-intelligence_(Sang_Tao)`

### Quy Tắc Dùng Nhanh

- build UI:
  - `builder`
- harvest tri thức:
  - `harvest`
- tăng sáng tạo:
  - `design-intelligence`

Lưu ý:

- bên ngoài có thể gọi bằng `Display Label`
- bên trong vẫn nên map về `Canonical ID`
- cú pháp kiểu `/flatsome-native` không phải mặc định chuẩn của Codex
- nếu muốn dùng slash alias, phải tự map thêm ở lớp vận hành riêng

## Strategic Model

- `platform`
  - language, syntax, Studio inventory, effects, page settings
- `factory`
  - reusable section archetypes, routing, design-language translation, anti-repeat rules, and assembly rules

## Root Entry Files

- `flatsome-native/MASTER OPERATING MEMORY.md`
  - single-file memory for AI sessions
  - fastest way to understand the whole system end-to-end
- `SKILL SURFACE MAP.md`
  - map 3 skill chính, tên hiển thị, call phrase, và route nội bộ
- `START HERE.md`
  - shortest reading route
  - quickest entry for daily operation
- `README.md`
  - structural catalog of the hub
  - explains folder roles and canonical layout

## V1.1 Reader Bundle

Đây là bundle mới để chuẩn bị public source và giúp AI mới đọc nhanh:

- `V1.1 RELEASE GUIDE.md`
  - chốt V1.1 đang ổn ở đâu, chưa ổn ở đâu, nên đọc gì trước
- `GITHUB PUBLIC CHECKLIST.md`
  - checklist ngắn để dọn repo trước khi public GitHub
- `PUBLIC READER GUIDE.md`
  - dành cho người đọc repo công khai
- `AI HANDOFF GUIDE.md`
  - dành cho Codex, GPT, OpenClaw, worker khác
- `HOW THIS HUB WORKS.md`
  - diễn giải hub vận hành từ đầu tới cuối bằng ngôn ngữ dễ đọc

## New Input Layer

Từ mốc này, hệ có thêm lớp vào cửa để mọi task Flatsome không còn nhảy thẳng từ brief sang build:

- `05-flows/Task Type Router.md`
  - khóa loại task trước khi mở flow chi tiết
- `05-flows/Quick Start Menu.md`
  - menu chọn nhánh cực nhanh cho người mới
- `05-flows/Guided Intake Questions.md`
  - script hỏi đáp ngắn theo từng lượt
- `05-flows/Input Contract.md`
  - khóa loại input, output expectation, style source, reference authority
- `05-flows/Master System Flow Map.md`
  - lưu đồ tổng từ intake đến release để check toàn hệ
- `03-factory/Task Route Matrix.md`
  - route input vào đúng mode build
- `05-flows/Best Result Playbook.md`
  - file dành cho người giao task để mô tả ngắn nhưng vẫn đủ rõ

## Canonical Layout

- `flatsome-native/MASTER OPERATING MEMORY.md`
  - single-file operating memory
  - summary of rules, flow, storage, anti-repeat, and known gaps
- `START HERE.md`
  - shortest entry file for humans and AI
- `01-platform/`
  - platform operating model
  - native builder language map
  - split builder language files
- `02-platform-studio-library/`
  - full Studio slot catalog
  - category files
  - effects and page settings
- `03-factory/`
  - reusable section archetypes
  - design language translation layer
  - task route matrix
  - typography system
  - spacing system
  - layout DNA
  - layout pool
  - hero rotation matrix
  - no-repeat rules
  - section order recipes
  - composition rules
  - starter snippets
- `06-templates/`
  - company templates for planning, scoring, exception, and block records
- `08-design-intelligence/`
  - optional design intelligence layer
  - mode routing
  - style / typography / spacing / motion reasoning
  - master + page override templates
- `05-flows/`
  - task type router
  - input contract
  - master system flow map
  - best result playbook
  - brief intake flow
  - repeatable harvest and verification flows
- `04-plans/`
  - system-upgrade plans only
- `07-reports/`
  - company-level evidence and audit reports
- `09-archive/`
  - optional historical evidence kept outside the main reading path

## Non-Hub But Related Task Paths

- `VPS/docs/superpowers/specs/`
  - task specs and page-specific design docs
- `VPS/docs/superpowers/specs/page-task-plans/`
  - page-specific implementation plans that must not live in `04-plans/`
- `VPS/docs/superpowers/reports/`
  - page/task-specific delivery reports
- `VPS/tmp/`
  - shortcode files and temporary execution helpers

## Source Of Truth

- repo path:
  - `VPS/docs/superpowers/flatsome-native`

Operational source of truth lives in:

- `01-platform/`
- `03-factory/`
- `05-flows/`
- `06-templates/`

Evidence and history live in:

- `04-plans/`
- `07-reports/`
- `09-archive/`

## Current Core Totals

- visible Studio slots: `492`
- unique template IDs: `337`
- duplicate slots: `155`

## Key Files

- `flatsome-native/MASTER OPERATING MEMORY.md`
- `START HERE.md`
- `01-platform/Native Builder Language Map.md`
- `01-platform/native-builder-language/README.md`
- `01-platform/Operating Model.md`
- `01-platform/Operating Law.md`
- `01-platform/Native Scoring Rule.md`
- `01-platform/Novelty Scoring Rule.md`
- `01-platform/Artifact Storage Rule.md`
- `01-platform/CSS Governance Rule.md`
- `01-platform/Exception Registry.md`
- `02-platform-studio-library/CATALOG-INDEX.md`
- `02-platform-studio-library/Effects.md`
- `02-platform-studio-library/Page Settings.md`
- `03-factory/Factory Overview.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`
- `08-design-intelligence/README.md`
- `08-design-intelligence/Design Mode Router.md`
- `03-factory/Layout DNA.md`
- `03-factory/Layout Pool.md`
- `03-factory/Hero Family Matrix.md`
- `03-factory/No Repeat Law.md`
- `03-factory/Section Order Recipes.md`
- `03-factory/Section Starter Snippets.md`
- `05-flows/Brief Intake Flow.md`
- `05-flows/Master System Flow Map.md`
- `03-factory/Block Registry.md`
- `05-flows/UI Build Script.md`
- `05-flows/Final QA Checklist.md`
- `07-reports/Recent Page Memory.md`
- `06-templates/README.md`
- `06-templates/Page Plan Template.md`
- `06-templates/Native Scoring Template.md`
- `06-templates/Novelty Scoring Template.md`
- `06-templates/Exception Report Template.md`
- `06-templates/Block Entry Template.md`
- `09-archive/README.md`

## Reading Strategy

### AI mới vào

- `AI HANDOFF GUIDE.md`
- `flatsome-native/MASTER OPERATING MEMORY.md`
- `START HERE.md`
- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`
- `05-flows/Task Type Router.md`
- `05-flows/Master System Flow Map.md`
- `03-factory/Task Route Matrix.md`
- `01-platform/`
- `03-factory/`
- `05-flows/`
- `06-templates/`
- `07-reports/` chỉ khi cần bằng chứng

### Human Operator

- `PUBLIC READER GUIDE.md`
- `README.md`
- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `flatsome-native/MASTER OPERATING MEMORY.md`
- `START HERE.md`
- folder liên quan đúng task
