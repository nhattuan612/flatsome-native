---
name: flatsome-native-harvest
description: Harvest thêm UI từ Flatsome Studio, cập nhật native map, kiểm coverage catalog, extract template evidence. Dùng khi mục tiêu là mở rộng tri thức hệ, không phải build page.
---

# flatsome-native-harvest — Học Thêm UI

## Mục Đích

Skill này là **cửa học thêm tri thức** của hệ `flatsome-native`.

Dùng khi:
- harvest từ `Flatsome Studio`
- import / kiểm coverage / check catalog
- extract template evidence
- cập nhật native map, slot map, library knowledge

Không dùng khi:
- mục tiêu chính là giao 1 page hoàn chỉnh → dùng `flatsome-native-builder`
- mục tiêu chính là đề xuất design language → dùng `flatsome-native-design-intelligence`

## Call Phrase

```
use flatsome-native-harvest_(Hoc_Them_UI)
```

## Thứ Tự Đọc Tối Thiểu

1. `05-flows/Task Type Router.md`
2. `05-flows/Verifiable Harvest Flow.md`
3. `05-flows/Direct Harvest Flow.md`
4. `05-flows/Imported Template Extraction Flow.md`
5. `01-platform/Artifact Storage Rule.md`
6. `01-platform/Native Builder Language Map.md`
7. `02-platform-studio-library/CATALOG-INDEX.md`

## Các Loại Harvest

### Verifiable Harvest
- dùng khi cần bằng chứng kiểm tra được
- đi qua: `05-flows/Verifiable Harvest Flow.md`

### Direct Harvest
- dùng khi thu thập nhanh không cần verify nghiêm ngặt
- đi qua: `05-flows/Direct Harvest Flow.md`

### Imported Template Extraction
- dùng khi extract từ template đã import vào Studio
- đi qua: `05-flows/Imported Template Extraction Flow.md`

## Luật Harvest

- Không hardcode credential/token trong script harvest
- Đọc credential từ `env` hoặc file local ngoài snapshot
- Mọi kết quả harvest phải lưu theo `01-platform/Artifact Storage Rule.md`
- Không bê nguyên assets/wording của hệ khác

## Studio Catalog Hiện Tại

- visible Studio slots: `492`
- unique template IDs: `337`
- duplicate slots: `155`

Catalog chi tiết: `02-platform-studio-library/CATALOG-INDEX.md`

## Hub Reference

Repo: https://github.com/nhattuan612/flatsome-native
File chính: `02-platform-studio-library/CATALOG-INDEX.md`, `05-flows/Verifiable Harvest Flow.md`
