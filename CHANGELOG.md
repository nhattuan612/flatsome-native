# CHANGELOG

All notable changes to `flatsome-native` are documented here.

Format: `[VERSION] - DATE - Summary`

---

## [V1.1] - 2026-04-25

### Added
- `MASTER OPERATING MEMORY.md` — single-file nạp nhanh toàn hệ
- `SKILL SURFACE MAP.md` — định nghĩa 3 skill chính
- `AI HANDOFF GUIDE.md` — onboarding nhanh cho AI worker mới
- `PUBLIC READER GUIDE.md` — hướng dẫn người đọc công khai
- `HOW THIS HUB WORKS.md` — diễn giải hub từ đầu tới cuối
- `V1.1 RELEASE GUIDE.md` — chốt trạng thái V1.1
- `GITHUB PUBLIC CHECKLIST.md` — checklist dọn repo trước khi public
- `05-flows/Quick Start Menu.md` — menu chọn nhánh nhanh
- `05-flows/Guided Intake Questions.md` — hỏi dẫn dắt theo lượt
- `05-flows/Input Contract.md` — khóa input/output trước khi build
- `05-flows/Task Type Router.md` — route loại task trước khi mở flow
- `05-flows/Master System Flow Map.md` — lưu đồ tổng toàn hệ
- `03-factory/Task Route Matrix.md` — route input vào đúng mode build
- `05-flows/Best Result Playbook.md` — hướng dẫn giao task hiệu quả
- `08-design-intelligence/` — lớp sáng tạo mở rộng (toàn bộ folder)
- `01-platform/Artifact Storage Rule.md` — luật lưu artifact
- `03-factory/Block Registry.md` — registry block đã build
- `06-templates/` — đủ 9 template chuẩn cho task UI
- Repair Gate runtime: preflight lint, draft fallback, auto-artifact

### Changed
- Refactor toàn bộ naming convention sang absolute filename
- Tách ownership rõ giữa `03-factory/Design Language Reference.md` và `08-design-intelligence/`
- Cắm Design Intelligence vào flow chính (intake + build + QA)
- Thêm Novelty Gate bắt buộc trước khi build

### Fixed
- Loại bỏ lặp ý giữa `03-factory/` và `08-design-intelligence/`
- Sửa các reference filename rút gọn gây AI phải đoán path

---

## [V1.0] - 2026-04-24

### Added
- Initial hub structure: `01-platform/`, `02-platform-studio-library/`, `03-factory/`, `05-flows/`, `06-templates/`
- Native Builder Language Map — syntax shortcode native
- Operating Law — luật cứng section-first, native >= 90%
- Studio slot catalog: 492 slots, 337 unique template IDs
- Factory: Layout DNA, Layout Pool, Hero Family Matrix, No Repeat Law, Section Archetypes
- Typography System, Spacing System
- Brief Intake Flow, UI Build Script, Final QA Checklist
- Novelty Scoring Rule, Native Scoring Rule
- Design Language Reference
