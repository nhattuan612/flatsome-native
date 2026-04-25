# V1.1 Public Onboarding Docs Report

Date: 2026-04-25

## Mục Đích

Ghi lại lần hardening tài liệu để chốt `V1.1` và chuẩn bị public source.

## Đầu Vào

Mục tiêu được chốt:

- tạo các file MD diễn giải chức năng, flow, cách làm
- giúp người đọc công khai hiểu hub nhanh
- giúp AI mới vào nạp toàn bộ hệ với ít token hơn
- không làm xáo trộn lõi law/flow/build đã ổn định

## File Đã Tạo

- `V1.1 RELEASE GUIDE.md`
- `PUBLIC READER GUIDE.md`
- `AI HANDOFF GUIDE.md`
- `HOW THIS HUB WORKS.md`

## File Đã Cập Nhật

- `README.md`
- `START HERE.md`
- `MASTER OPERATING MEMORY.md`

## Tác Dụng Chính

- thêm một bundle `V1.1` ở root để public reader không phải nhảy thẳng vào file kỹ thuật sâu
- tách rõ đường đọc cho `human public reader` và `AI worker`
- giảm nhầm giữa `source of truth` với `history/evidence`
- thêm lớp diễn giải end-to-end cho toàn hub

## Điều Không Thay Đổi

- không đổi luật build
- không đổi flow build
- không đổi nơi lưu artifact
- không đổi novelty gate / repair gate / native rule

## Việc Còn Để Sau

- dọn naming cũ trong history khi chuẩn bị push GitHub
- rà internal path còn sót trong archived page-task docs
- nếu cần, bổ sung machine-readable manifest ở `V2`

## Kết Luận

V1.1 đã có lớp onboarding riêng đủ rõ cho:

- public reader
- AI worker
- người vận hành nội bộ
