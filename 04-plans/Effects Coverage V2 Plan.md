# Flatsome Effects Coverage V2 Plan

**Goal:** Nâng `02-platform-studio-library/Effects.md` từ danh sách effect rời rạc thành bản đồ effect có cấu trúc, bám trên `337` export unique đã harvest.

**Why this exists**

- bản `02-platform-studio-library/Effects.md` cũ mới bao quát phần lõi, chưa tách effect theo nhóm vận hành
- dữ liệu raw đã có đủ để map sâu hơn mà không cần harvest lại
- đội ngũ cần một map effect dễ tra cứu khi build trang bằng Flatsome Native Builder

**Outputs**

- cập nhật `VPS/docs/superpowers/flatsome-native/02-platform-studio-library/Effects.md`
- thêm `VPS/docs/superpowers/flatsome-native/07-reports/Effects Coverage V2 Report.md`

**Execution outline**

1. đọc lại `337` export trong `VPS/data/flatsome-studio/exports`
2. gom các effect theo nhóm vận hành:
   - overlay and contrast
   - motion and reveal
   - hover and interactive states
   - depth and elevation
   - slider and carousel behavior
   - video behavior
3. cập nhật `02-platform-studio-library/Effects.md` với observed count, common values, sample shortcode
4. ghi report xác nhận mức phủ effect hiện tại và phần chưa nằm trong scope
