# Task Type Router

Date: 2026-04-25

## Mục Đích

File này tồn tại để chặn lỗi route từ quá sớm:

- nhầm `page-task` với `harvest-task`
- nhầm `harvest-task` với `extract-task`
- nhầm `system-doc-task` với `UI build task`

Nếu route sai ngay từ đầu, worker sẽ mở sai flow và làm hỏng nhịp vận hành.

## 4 Loại Task Chính

### 1. `page-task`

Dùng khi:

- mục tiêu là tạo / sửa / clone / tối ưu một trang
- đầu ra cuối là `public page`, `edit page`, `builder page`
- cần `Page Plan`, `Native Build Output`, `Audit Checklist`, `Fix Pass`, `Final Verification`

Mở tiếp:

- `05-flows/Quick Start Menu.md`
- `05-flows/Guided Intake Questions.md`
- `05-flows/Input Contract.md`
- `05-flows/Brief Intake Flow.md`
- `05-flows/Master System Flow Map.md`

### 2. `harvest-task`

Dùng khi:

- mục tiêu là hút template, catalog, effect, page setting
- không tạo page delivery cho user cuối
- đầu ra là `catalog`, `slot map`, `raw export`, `evidence`

Mở tiếp:

- `05-flows/Verifiable Harvest Flow.md`
- `05-flows/Direct Harvest Flow.md`

Không mở flow build page như đường chính.

### 3. `extract-task`

Dùng khi:

- đã có page hoặc template import sẵn
- mục tiêu là đọc shortcode / tag / snippet / section pattern
- đầu ra là snippet, tag list, evidence note

Mở tiếp:

- `05-flows/Imported Template Extraction Flow.md`

Không dùng flow này để thay cho build page.

### 4. `system-doc-task`

Dùng khi:

- mục tiêu là sửa luật, flow, template, routing, memory
- đầu ra là cập nhật tri thức của hub
- không có page delivery cho end user

Mở tiếp:

- `MASTER OPERATING MEMORY.md`
- `START HERE.md`
- folder core liên quan

Không cập nhật `Recent Page Memory` cho loại task này.

## Cách Chọn Nhanh

Nếu câu hỏi chính là:

- `Trang này sẽ lên web cho người xem?`
  - `page-task`
- `Mục tiêu là hút / import / verify template catalog?`
  - `harvest-task`
- `Mục tiêu là đọc code native từ page đã có?`
  - `extract-task`
- `Mục tiêu là sửa bộ não / luật / flow / docs?`
  - `system-doc-task`

## Luật Cứng

1. Mỗi task chỉ được có `1 route chính`.
2. Nếu task có nhiều phần, phải chốt `route chính` trước rồi mới mở route phụ.
3. Không dùng `page-task` flow cho `harvest-task`.
4. Không dùng `harvest-task` flow để tuyên bố page delivery đã pass.
5. Không cập nhật `Recent Page Memory` cho:
   - `harvest-task`
   - `extract-task`
   - `system-doc-task`

## Dấu Hiệu Route Sai

- đang sửa docs nhưng lại mở `Page Plan Template`
- đang hút template nhưng lại đi `Input Contract`
- đang build page nhưng không có `Page Plan`
- đang extract snippet nhưng lại chạy `Final QA Checklist`

## Kết Luận

Muốn đỡ mở sai flow ngay từ đầu, phải khóa `task type` trước khi vào flow chi tiết.
