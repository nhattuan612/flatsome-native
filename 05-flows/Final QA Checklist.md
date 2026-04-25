# Checklist Kiểm Tra Cuối Cho Trang Flatsome Native

Date: 2026-04-24

## Mục Đích

Checklist này là điều kiện pass cuối cùng trước khi được phép báo hoàn thành một trang build bằng `Flatsome UX Builder`.

Nếu còn bất kỳ mục `blocking` nào chưa pass thì chưa được báo xong.

## Điều Kiện Pass Chung

Một trang chỉ được coi là pass khi có đủ:

- `link public`
- `edit page`
- `builder openable`
- native structure còn chỉnh sửa được
- `Fix Pass` đã đóng mọi lỗi `blocking`

## 1. Checklist Cấu Trúc Builder

- [ ] `[blocking]` Mọi phần chính đều nằm trong `section`.
- [ ] `[blocking]` Mọi phần chính đều đi qua `row`.
- [ ] `[blocking]` Không có layout quan trọng nào dựng bằng `ux_html`.
- [ ] `[warn]` `row_inner` và `col_inner` nếu có thì dùng đúng mục đích.
- [ ] `[blocking]` Không có section/rule cấu trúc bị bỏ sót so với `Page Plan`.
- [ ] `[blocking]` Không có element quan trọng bị rơi khỏi cây native.
- [ ] `[blocking]` `UX Builder` mở lại được.
- [ ] `[blocking]` `UX Builder` chỉnh sửa kéo thả lại được.
- [ ] `[blocking]` `edit page` không bị vỡ content.
- [ ] `[blocking]` Native structure còn nguyên sau khi save.

## 2. Checklist Native Và HTML

- [ ] `[blocking]` Trang đạt tinh thần `>=90% native`.
- [ ] `[blocking]` HTML không bị dùng làm khung layout chính.
- [ ] Nếu có `ux_html`, nó chỉ dùng cho:
  - `iframe`
  - `embed`
  - `link` đặc biệt
  - `map`
- [ ] `[blocking]` Không có đoạn HTML dùng để che lỗi cấu trúc.
- [ ] `[blocking]` Nếu có ngoại lệ hiếm, đã có `report + file/log`.

## 3. Checklist Spacing

- [ ] `[blocking]` Spacing đi theo một `profile` rõ ràng, không ngẫu hứng.
- [ ] `[warn]` Spacing giữa các section hợp lý.
- [ ] `[warn]` Spacing trong row và col không bị chồng chéo vô tổ chức.
- [ ] `[warn]` Không có khoảng trắng thừa lớn bất thường.
- [ ] `[warn]` Không có section bị nén quá chặt.
- [ ] `[warn]` Card padding giữ đúng cấp và đều.
- [ ] `[warn]` CTA có đủ khoảng thở để nhìn ra hành động chính.
- [ ] `[warn]` Negative margin nếu có là có chủ đích và không phá mobile.
- [ ] `[warn]` Spacing desktop ổn.
- [ ] `[warn]` Spacing tablet ổn.
- [ ] `[blocking]` Spacing mobile ổn.

## 4. Checklist Typography

- [ ] `[blocking]` Thứ bậc tiêu đề rõ ràng.
- [ ] `[warn]` Font đúng tone đã chốt.
- [ ] `[blocking]` `Typography direction` khớp với `Page Plan`.
- [ ] `[blocking]` `Design Mode` thực tế khớp với `Page Plan`.
- [ ] `[warn]` `Style family` thực tế không lệch khỏi hướng đã chốt.
- [ ] `[warn]` `Typography mood` thực tế không lệch khỏi hướng đã chốt.
- [ ] `[warn]` `Spacing rhythm` thực tế không lệch khỏi hướng đã chốt.
- [ ] `[warn]` Hero title và section title không cùng cấp cảm nhận.
- [ ] `[blocking]` Hero title không vượt `Hero title budget` đã chốt.
- [ ] `[blocking]` Hero title không vượt số dòng mobile đã chốt.
- [ ] `[blocking]` Không có lỗi `compound scaling` giữa `ux_text` và `h1/h2/h3`.
- [ ] `[blocking]` `Heading wrapper risk` thực tế không vượt mức đã chốt.
- [ ] `[warn]` Cỡ chữ đọc được trên desktop.
- [ ] `[blocking]` Cỡ chữ đọc được trên mobile.
- [ ] `[warn]` Chiều rộng dòng body không quá dài gây khó đọc.
- [ ] `[warn]` Line-height không bị đặc khó đọc.
- [ ] `[warn]` Không có đoạn text bị vỡ dòng xấu bất thường.
- [ ] `[warn]` Không có đoạn text quá dài gây nặng nhịp đọc.

## 5. Checklist CTA

- [ ] `[blocking]` CTA chính rõ ràng.
- [ ] `[warn]` CTA phụ không lấn át CTA chính.
- [ ] `[blocking]` Nút bấm nhìn thấy rõ.
- [ ] `[warn]` CTA đặt đúng vị trí theo nhịp đọc.
- [ ] `[warn]` Trạng thái hover/focus hợp lý nếu có.

## 6. Checklist Hình Ảnh

- [ ] `[blocking]` Không có ảnh trống.
- [ ] `[blocking]` Không có ảnh sai tỷ lệ.
- [ ] `[blocking]` Không có ảnh sai nội dung.
- [ ] `[warn]` Ảnh đúng tone trang.
- [ ] `[warn]` Ảnh hero đủ nổi bật nếu trang có hero.
- [ ] `[warn]` Crop và fit không gây mất ý nghĩa chính.

## 7. Checklist Responsive

- [ ] `[warn]` Desktop ổn.
- [ ] `[warn]` Tablet ổn.
- [ ] `[blocking]` Mobile ổn.
- [ ] `[blocking]` Không có vỡ khung ngang.
- [ ] `[blocking]` Không có cột chồng bất thường.
- [ ] `[warn]` Không có block biến mất sai chủ đích.
- [ ] `[blocking]` Menu / navigation nếu có vẫn dùng được trên mobile.
- [ ] `[blocking]` Tap target đủ dễ bấm trên mobile.

## 8. Checklist Public Page

- [ ] `[blocking]` Link public mở được.
- [ ] `[warn]` Giao diện public khớp với mục tiêu trang.
- [ ] `[blocking]` Không có lỗi hiển thị lớn trên public.
- [ ] `[blocking]` Không có phần bị thiếu sau khi save.
- [ ] `[blocking]` Không có lỗi rõ ràng về UI/UX/code ở public surface.
- [ ] `[blocking]` Không có raw shortcode lộ ra public như `[/text_box]`, `[/tab]`, `[/ux_text]`, `[/ux_banner]`, `[/tabgroup]`.

## 9. Checklist CSS

- [ ] `[blocking]` Mọi CSS thêm mới đều nằm ở `Theme Options` của Flatsome.
- [ ] `[blocking]` Không dùng CSS cục bộ tại trang như đường mặc định.
- [ ] `[blocking]` Mọi CSS thêm mới có comment tiếng Việt giải thích rõ.
- [ ] `[blocking]` CSS không phá khả năng chỉnh sửa native của Builder.

## 10. Checklist Hoàn Thành

- [ ] `[blocking]` `Page Plan` tồn tại.
- [ ] `[blocking]` `Section Map` tồn tại.
- [ ] `[blocking]` `Native Build Output` tồn tại.
- [ ] `[blocking]` `Native Scoring` tồn tại.
- [ ] `[blocking]` `Novelty Scoring` tồn tại.
- [ ] `[blocking]` `Audit Checklist` đã được đi qua.
- [ ] `[blocking]` `Fix Pass` đã hoàn tất.
- [ ] `[blocking]` `Fix Pass` có `nhóm lỗi`, `lỗi gốc`, `cách sửa`, `bề mặt kiểm lại`, `kết quả sau sửa`.
- [ ] `[blocking]` `Final Verification` đã có bằng chứng cuối.

## 10A. Checklist Repair Gate

- [ ] `[blocking]` Mọi lỗi sau `Audit` đã được phân loại trước khi sửa.
- [ ] `[blocking]` Đã sửa lỗi gốc, không chỉ vá triệu chứng.
- [ ] `[blocking]` Sau mỗi vòng fix đã re-check đúng bề mặt đã lỗi.
- [ ] `[blocking]` Sau mỗi vòng fix đã mở lại `builder`.
- [ ] `[blocking]` Sau mỗi vòng fix đã kiểm lại `public`.
- [ ] `[blocking]` Nếu gặp lỗi thường gặp, đã đối chiếu `05-flows/Common Error Repair Playbook.md`.
- [ ] `[blocking]` Không publish/công khai trước khi qua `Repair Gate`.

## 11. Checklist Novelty

- [ ] `[blocking]` Đã so với ít nhất `3` trang gần nhất.
- [ ] `[blocking]` `Similarity Risk` không phải `Blocked`.
- [ ] `[blocking]` `Novelty Score cuối >= 10`.
- [ ] `[blocking]` Đã kiểm `Macro Sequence Fingerprint`.
- [ ] `[blocking]` `Macro Sequence Risk` không phải `Blocked`.
- [ ] `[blocking]` Không rơi lại vào `safe pattern` đã bị cấm.
- [ ] `[warn]` `Hero Family` khác hoặc có lý do rõ nếu trùng.
- [ ] `[warn]` `Layout Pool` khác hoặc có lý do rõ nếu trùng.
- [ ] `[warn]` `CTA Pattern` không lặp vô thức.

## Phán Quyết Cuối

### Pass

Chỉ pass khi:

- toàn bộ mục `blocking` đạt
- trang `public` ổn
- `edit page` ổn
- `UX Builder` mở được
- native structure còn nguyên
- `Repair Gate` pass
- novelty gate pass
- có `link public`

### Ngoại Lệ Hiếm

Chỉ được chấp nhận ngoại lệ hiếm khi đồng thời đúng:

- `public page` hoàn hảo
- `native >= 90%`
- có `report + file/log`
- `Codex` là người phê chuẩn cuối cùng

### Fail

Fail nếu có bất kỳ điều nào sau đây:

- không mở lại được bằng `UX Builder`, trừ khi đã được phê chuẩn theo `Ngoại Lệ Hiếm`
- native structure bị gãy
- dùng HTML làm layout chính
- không đạt ngưỡng native tối thiểu
- novelty score không đạt
- public page còn lỗi lớn
- chưa có bằng chứng kiểm tra cuối
