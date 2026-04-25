# Imported Template Extraction Flow

Date: 2026-04-25

## Mục Đích

Flow này dùng để hút shortcode-native từ một page đã import hoặc một surface demo đã mở được.

Nó không phải luật build page.

Nó chỉ là workflow đọc và trích xuất để cập nhật tri thức.

## Khi Nào Dùng

- khi đã import một template vào WordPress
- khi có page demo cần đọc shortcode/native surface
- khi cần xác minh nhanh tag list, content length, và section snippet

## Đầu Ra Cần Lấy

- `page ID`
- `title`
- `content length`
- `unique tag list`
- `section snippet` có giá trị
- `evidence note` nếu pattern mới đáng đưa về hub

## Quy Trình Chuẩn

1. xác định page cần đọc
2. mở edit surface hoặc classic editor HTML
3. đọc `#content`
4. trích tag shortcode
5. lưu các snippet có giá trị
6. chỉ cập nhật hub khi pattern thật sự reusable

## Browser-Side Extraction Pattern

```js
fetch(editPageUrl)
  .then(r => r.text())
  .then(html => {
    const d = new DOMParser().parseFromString(html, "text/html");
    const title = d.querySelector("#title")?.value || "";
    const content = d.querySelector("#content")?.value || "";
    const tags = [...content.matchAll(/\[([a-zA-Z_][a-zA-Z0-9_-]*)/g)].map(m => m[1]);
    return {
      title,
      len: content.length,
      tags: [...new Set(tags)].sort()
    };
  });
```

## Quy Tắc CEO

- không coi extract workflow là build workflow
- không đưa snippet kém chất lượng vào hub
- không để extraction note chen vào `01-platform/` nếu chưa đủ reusable

## File Liên Quan

- `01-platform/Native Builder Language Map.md`
- `01-platform/native-builder-language/06-Patterns and Workflow.md`
- `05-flows/Verifiable Harvest Flow.md`
