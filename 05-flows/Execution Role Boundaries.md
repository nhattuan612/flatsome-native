# Execution Role Boundaries

Date: 2026-04-25

## Mục Đích

File này tách riêng phần vai trò worker khỏi lớp syntax/platform.

Mục tiêu là để:

- `01-platform/` chỉ giữ luật và ngôn ngữ
- `05-flows/` giữ workflow và boundary vận hành

## Vai Trò Của Codex

- hiểu luật
- lập plan
- chọn route
- quyết định kiến trúc page
- viết shortcode-native
- kiểm `public + edit + builder`
- quyết định cuối cho ngoại lệ hiếm

## Vai Trò Của OpenClaw

- mở đúng surface
- dán shortcode-native đã biết
- thay biến rõ ràng
- save
- verify cơ bản
- báo tiến trình

## OpenClaw Không Nên Gánh

- tự nghĩ ra layout lớn từ số 0
- quyết định design architecture
- cứu các trạng thái drag-drop UI quá mong manh
- tự diễn giải luật công ty nếu chưa có plan rõ

## Quy Tắc CEO

- luật build luôn do `Codex` giữ
- worker chỉ là lớp thực thi hỗ trợ
- output cuối vẫn phải bám `01-platform/Operating Law.md`

## File Liên Quan

- `01-platform/Operating Law.md`
- `05-flows/UI Build Script.md`
- `flatsome-native/MASTER OPERATING MEMORY.md`
