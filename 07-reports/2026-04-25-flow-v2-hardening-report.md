# Flow V2 Hardening Report

Date: 2026-04-25

## Mục Đích

Khóa chặt hơn lớp flow sau stress test để giảm:

- route sai loại task
- loop hỏi lại vô ích
- cập nhật sai `Recent Page Memory`

## Hạng Mục Đã Làm

### 1. Thêm `Task Type Router`

Tạo:

- `05-flows/Task Type Router.md`

Mục đích:

- tách rõ `page-task`
- `harvest-task`
- `extract-task`
- `system-doc-task`

### 2. Harden `Master System Flow Map`

Đã bổ sung:

- `Gate 0: Task Type Gate`
- `Gate 8: Memory Update Gate`
- nhánh `System Docs`
- luật `Anti-Loop`

### 3. Siết `Recent Page Memory`

Đã bổ sung rule:

- khi nào `được` cập nhật
- khi nào `không được` cập nhật
- vì sao không được dùng file này như nhật ký mọi task

### 4. Đồng bộ entry points

Đã nối `Task Type Router` vào:

- `README.md`
- `START HERE.md`
- `MASTER OPERATING MEMORY.md`
- `05-flows/README.md`

## Lỗ Hổng Được Vá

### Lỗ Hổng 1: Route Sai Loại Task

Trước đây flow tổng chưa có bước khóa:

- đây là `page-task`
- hay `harvest-task`
- hay `extract-task`
- hay `system-doc-task`

Hệ quả:

- worker có thể mở `Page Plan` cho task harvest
- worker có thể chạy `Final QA Checklist` cho task extract

### Lỗ Hổng 2: Loop Hỏi Lại Không Cần Thiết

Trước đây đã có vá `Build Readiness -> failed upstream gate`, nhưng chưa có luật tổng quát chống loop.

Đã thêm:

- không lặp `Input Contract <-> Guided Intake` quá `1` vòng nếu unknowns không đổi
- không nhảy từ `Audit` sang `Done` nếu chưa qua re-check đầy đủ

### Lỗ Hổng 3: Nhiễu `Recent Page Memory`

Trước đây `Recent Page Memory` ghi:

- `Mỗi lần hoàn thành page mới phải cập nhật file này`

Câu này đúng nhưng chưa đủ chặt, dễ bị hiểu sai thành:

- task nào xong cũng cập nhật

Đã siết lại:

- chỉ `page-task`
- chỉ page mới hoặc rebuild đủ lớn
- không cập nhật cho docs / harvest / extract / fix nhỏ

## Tác Động Sau Hardening

- flow tổng chặt hơn ngay từ gate đầu
- worker ít mở sai flow hơn
- novelty memory ít nhiễu hơn
- dễ scale thêm route mới mà không phá flow page delivery

## Kết Luận

`Flow V2 Hardening` đã hoàn tất ở mức docs/core.

Sau bước này, lớp flow của hệ đã rõ hơn ở 3 điểm:

- route task type
- anti-loop
- memory update governance
