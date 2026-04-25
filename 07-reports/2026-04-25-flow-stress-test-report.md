# Flow Stress Test Report

Date: 2026-04-25

## Mục Đích

Stress test lưu đồ tổng của hệ `flatsome-native` bằng các case giả lập để tìm:

- gate nào còn hở
- loop nào còn mơ hồ
- điểm nào dễ làm worker route sai

## Phạm Vi Đã So

- `05-flows/Master System Flow Map.md`
- `05-flows/Input Contract.md`
- `05-flows/Brief Intake Flow.md`
- `03-factory/Task Route Matrix.md`
- `06-templates/Page Plan Template.md`
- `05-flows/Final QA Checklist.md`
- `05-flows/Common Error Repair Playbook.md`

## Kết Luận Nhanh

- `5/5` case đi qua được flow
- có `2` lỗ hở logic nhẹ ở lớp diễn đạt của lưu đồ
- đã sửa ngay trong `05-flows/Master System Flow Map.md`

## Case 1: Brief Ngắn, Thiếu CTA

### Input

- loại input: `text thường`
- user nói: `làm cho tôi một homepage đẹp hơn theo Flatsome`
- chưa có `CTA`
- chưa có `thiết bị ưu tiên`

### Kỳ vọng đúng

- không được route tiếp sang `Page Plan`
- phải bị chặn ở `Input Contract` / `Guided Intake`

### Kết quả stress test

- pass
- flow chặn đúng ở `Gate 1: Intake Gate`

### Lý do pass

`Input Contract` và `Guided Intake Questions` đều yêu cầu:

- `CTA chính`
- `thiết bị ưu tiên`

## Case 2: Ảnh Landing Page, Yêu Cầu Clone Nhưng Chưa Trích Cấu Trúc

### Input

- loại input: `ảnh`
- user muốn `clone`
- reference authority = `primary`
- chưa trích:
  - `layout tổng`
  - `hero type`
  - `CTA pattern`
  - `proof pattern`

### Kỳ vọng đúng

- chưa được route là `clone`
- phải quay lại bước trích xuất ảnh

### Kết quả stress test

- pass
- flow chặn đúng ở `Brief Intake Flow` + `Task Route Matrix`

### Lý do pass

`Brief Intake Flow` và `Task Route Matrix` đều ghi rõ:

- ảnh/link phải trích đủ cấu trúc tối thiểu
- nếu chưa trích được thì chưa khóa route `clone`

## Case 3: Mixed Input, Nguồn Xung Đột

### Input

- `text + ảnh + link + repo style`
- text muốn `Flatsome mặc định`
- repo style muốn `creative-modern`
- link tham chiếu muốn `clone gần giống`
- user chưa chốt nguồn nào là chính

### Kỳ vọng đúng

- chưa được route
- phải khóa:
  - `output expectation`
  - `style source`
  - `reference authority`

### Kết quả stress test

- pass
- flow chặn đúng ở `Input Contract` và `Task Route Matrix`

### Lý do pass

`Task Route Matrix` đã ghi:

- mixed input route theo `output expectation`
- nếu nguồn xung đột thì phải hỏi thêm

## Case 4: Creative-Modern Nhưng Novelty Gate Bị Block

### Input

- loại input: `text thường`
- output expectation: `original`
- style source: `Flatsome Native Core + Design Intelligence`
- user muốn sáng tạo mạnh
- sau khi so với `3` trang gần nhất:
  - `Hero Family` trùng
  - `Layout Pool` trùng
  - `CTA Pattern` trùng mạnh
  - `Similarity Risk = Blocked`

### Kỳ vọng đúng

- không được build
- phải quay lại đổi:
  - `Layout Pool`
  - hoặc `Hero Family`
  - hoặc `Section Order Recipe`

### Kết quả stress test

- pass
- flow chặn đúng ở `Novelty Gate`

### Lý do pass

`Master System Flow Map`, `Operating Law`, `Page Plan Template`, `Final QA Checklist` đều khóa:

- `Similarity Risk = Blocked` => không được build

## Case 5: Build Xong, Audit Fail Vì Raw Shortcode Và Mobile Vỡ

### Input

- page đã build xong
- public page lộ raw shortcode
- mobile bị vỡ ngang
- builder vẫn mở được

### Kỳ vọng đúng

- không được release
- phải đi đúng loop:
  - `Audit`
  - `Classify`
  - `Fix`
  - `Re-check`
  - `Re-open Builder`
  - `Public Re-check`
  - quay lại `Audit`

### Kết quả stress test

- pass
- flow buộc quay lại `Repair Gate`

### Lý do pass

`Final QA Checklist` và `Common Error Repair Playbook` đã khóa đúng:

- raw shortcode public = blocking
- mobile vỡ = blocking
- không publish trước khi qua `Repair Gate`

## Lỗ Hở Đã Tìm Thấy

### Lỗ Hở 1

`Build Readiness Pass? -> No` trong lưu đồ cũ đang quay về quá thô, dễ làm người đọc hiểu là luôn quay về `Guided Intake`.

### Vì sao nguy hiểm

Thực tế `Build Readiness` có thể fail do:

- `Intake`
- `Route`
- `Novelty`
- hoặc `Page Plan`

Nếu quay sai, worker có thể hỏi lại lan man dù lỗi thật nằm ở novelty hoặc page plan.

### Cách sửa

Đã thêm rule:

- phải quay về `đúng gate bị fail`
- không mặc định coi đây là lỗi intake

## Lỗ Hở 2

Nhánh `Build UI Chuẩn` trong flow summary cũ thiếu:

- `Page Goal Routing`
- `Design Mode / Native Core`
- `Novelty Gate`
- `Build Readiness`

### Vì sao nguy hiểm

Người đọc bản tóm tắt có thể tưởng chỉ cần:

`Input Contract -> Page Plan -> Build`

trong khi flow thật chặt hơn nhiều.

### Cách sửa

Đã mở rộng nhánh tóm tắt để phản ánh flow thật.

## Đầu Ra Sau Stress Test

- `05-flows/Master System Flow Map.md` đã được vá
- flow tổng rõ hơn ở điểm quay lui và nhánh build chuẩn

## Phán Quyết

Tại thời điểm report này:

- flow tổng `đúng`
- gate chính `đủ chặt`
- không thấy lỗ hở blocking mới
- các lỗi phát hiện chỉ là `diễn đạt flow`, không phải lỗi luật lõi
