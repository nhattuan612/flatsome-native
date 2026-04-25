# 01-platform

Date: 2026-04-24

## Mục Đích

Đây là lớp `source of truth` cho:

- luật vận hành
- ngôn ngữ native của Flatsome Builder
- scoring
- ngoại lệ

Nếu AI không hiểu builder language, phải đọc folder này trước.

## Đọc Gì Trước

Thứ tự ngắn nhất:

1. `01-platform/Operating Law.md`
2. `01-platform/Native Builder Language Map.md`
3. `01-platform/Native Scoring Rule.md`
4. `01-platform/Novelty Scoring Rule.md`
5. `01-platform/Artifact Storage Rule.md`
6. `01-platform/CSS Governance Rule.md`
7. `01-platform/Exception Registry.md`

Nếu cần chi tiết về shortcode:

1. `native-builder-language/01-Overview and Source Rules.md`
2. `native-builder-language/02-Layout and Structure.md`
3. `native-builder-language/03-Content and Media.md`
4. `native-builder-language/04-Commerce and Dynamic.md`
5. `native-builder-language/05-Aliases and Broad Surface.md`
6. `native-builder-language/06-Patterns and Workflow.md`

## File Nào Làm Gì

- `01-platform/Operating Law.md`
  - luật cứng của công ty
- `01-platform/Operating Model.md`
  - mô hình vận hành tổng quát
- `01-platform/Native Builder Language Map.md`
  - file index để route nhanh sang đúng nhóm kiến thức shortcode
- `01-platform/Native Scoring Rule.md`
  - cách chấm độ native
- `01-platform/Novelty Scoring Rule.md`
  - cách chấm độ mới lạ và chặn lặp
- `01-platform/Artifact Storage Rule.md`
  - luật lưu artifact của task UI
- `01-platform/CSS Governance Rule.md`
  - luật dùng CSS
- `01-platform/Exception Registry.md`
  - nơi ghi ngoại lệ hiếm
- `native-builder-language/*`
  - kiến thức shortcode/pattern theo nhóm

## Khi Nào Cập Nhật Folder Này

Chỉ cập nhật khi có một trong các trường hợp sau:

- xác minh thêm shortcode mới
- phát hiện syntax cũ sai hoặc thiếu
- thay đổi luật công ty
- thay đổi scoring rule
- có ngoại lệ mới cần ghi nhận

## Không Được Làm

- không bịa shortcode
- không đưa report dự án cụ thể vào đây
- không dùng folder này để lưu kết quả build một trang riêng

## Kết Luận

Muốn AI code Flatsome đúng, phải nạp folder này trước.
