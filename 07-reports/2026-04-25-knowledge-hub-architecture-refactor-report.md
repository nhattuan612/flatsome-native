# Knowledge Hub Architecture Refactor Report

Date: 2026-04-25

## Mục Đích

Report này ghi lại đợt refactor tài liệu tập trung vào:

- route tri thức
- source of truth hygiene
- tách `system docs` và `page-specific docs`
- tạo một entry file duy nhất cho AI session khác

## Đã Làm

- tạo `flatsome-native/MASTER OPERATING MEMORY.md`
- siết `04-plans/` về `system-upgrade plans only`
- chuyển page-specific plans ra `VPS/docs/superpowers/specs/page-task-plans/`
- thêm `README.md` cho các folder còn thiếu
- làm rõ `README.md` vs `START HERE.md` vs `flatsome-native/MASTER OPERATING MEMORY.md`
- tách extraction flow và execution role boundaries khỏi lớp platform
- dọn `05-flows/Verifiable Harvest Flow.md` theo hướng generic hơn

## Kết Quả Mong Muốn

- AI mới vào có một đường đọc rõ hơn
- ít nhầm report/history với luật hiện hành
- ít token waste do phải dò cây thư mục
- dễ mở rộng hub sau này
