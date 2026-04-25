# 03-factory

Date: 2026-04-24

## Mục Đích

Đây là lớp biến `kiến thức nền` thành `khả năng build thực tế`.

`01-platform` trả lời:

- shortcode nào có
- syntax nào đã xác minh

`03-factory` trả lời:

- brief này nên dùng skeleton nào
- section nào nên đi trước
- archetype nào hợp nhất
- block nào nên tái dùng
- khung native nào nên khởi động

## Đọc Gì Trước

1. `03-factory/Factory Overview.md`
2. `03-factory/Task Route Matrix.md`
3. `03-factory/Page Goal Routing.md`
4. `03-factory/Design Language Reference.md`
5. `03-factory/Typography System.md`
6. `03-factory/Spacing System.md`
7. `03-factory/Layout DNA.md`
8. `03-factory/Layout Pool.md`
9. `03-factory/Hero Family Matrix.md`
10. `03-factory/No Repeat Law.md`
11. `03-factory/Section Order Recipes.md`
12. `03-factory/Section Archetypes.md`
13. `03-factory/Block Library Candidates.md`
14. `03-factory/Section Starter Snippets.md`
15. `03-factory/Composition Rules.md`
16. `03-factory/Block Registry.md`

## File Nào Làm Gì

- `03-factory/Factory Overview.md`
  - mô tả toàn bộ lớp factory
- `03-factory/Page Goal Routing.md`
  - route brief -> skeleton -> archetype
- `03-factory/Task Route Matrix.md`
  - route loại input -> mode build -> style source
- `03-factory/Design Language Reference.md`
  - cách tiếp thu design language hiện đại mà vẫn giữ gốc native
- `03-factory/Typography System.md`
  - cách chốt hierarchy chữ và readability
- `03-factory/Spacing System.md`
  - cách chốt spacing tokens và rhythm
- `03-factory/Layout DNA.md`
  - chốt DNA bố cục trước khi build
- `03-factory/Layout Pool.md`
  - chọn pool bố cục bắt buộc trước khi build
- `03-factory/Hero Family Matrix.md`
  - điều phối rotation của hero family
- `03-factory/No Repeat Law.md`
  - luật chống lặp bố cục giữa các task
- `03-factory/Section Order Recipes.md`
  - nhiều công thức sắp thứ tự section để build nhanh và khác nhau
- `03-factory/Section Archetypes.md`
  - các họ section dùng lại nhiều lần
- `03-factory/Section Starter Snippets.md`
  - khung shortcode-native bắt đầu nhanh
- `03-factory/Block Library Candidates.md`
  - ứng viên block nên tái dùng hoặc nâng cấp
- `03-factory/Block Registry.md`
  - luật quản trị block
- `03-factory/Composition Rules.md`
  - luật ghép section thành page

## Khi Nào Cập Nhật Folder Này

- có page type mới đáng lặp lại
- có archetype mới đã dùng ổn định
- có starter snippet mới đủ mạnh
- có block candidate mới
- có rule ghép section tốt hơn
- có rule chống lặp hoặc design-language tốt hơn

## Source Of Truth Trong Folder Này

- route: `03-factory/Page Goal Routing.md`
- route input: `03-factory/Task Route Matrix.md`
- design language: `03-factory/Design Language Reference.md`
- typography: `03-factory/Typography System.md`
- spacing: `03-factory/Spacing System.md`
- DNA: `03-factory/Layout DNA.md`
- layout pool: `03-factory/Layout Pool.md`
- hero rotation: `03-factory/Hero Family Matrix.md`
- anti-repeat: `03-factory/No Repeat Law.md`
- recipe: `03-factory/Section Order Recipes.md`
- archetype: `03-factory/Section Archetypes.md`
- snippet: `03-factory/Section Starter Snippets.md`
- governance block: `03-factory/Block Registry.md`

## Không Được Làm

- không đưa content của một thương hiệu cụ thể vào đây
- không biến snippet thành dump HTML
- không thêm block candidate khi chưa có lý do tái dùng

## Kết Luận

AI muốn đi từ brief sang build nhanh thì phải dùng folder này.
