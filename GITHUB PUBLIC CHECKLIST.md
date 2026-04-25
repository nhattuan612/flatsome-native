# GITHUB PUBLIC CHECKLIST

Date: 2026-04-25

## Mục Đích

Đây là checklist ngắn nhất để đưa `flatsome-native` lên GitHub theo cách an toàn và sạch.

Mục tiêu:

- không lộ thông tin nội bộ
- không làm public reader hiểu sai luật
- không làm history lẫn với source of truth

## 1. Giữ Lại

Giữ public các lớp core:

- `README.md`
- `START HERE.md`
- `MASTER OPERATING MEMORY.md`
- `SKILL SURFACE MAP.md`
- `V1.1 RELEASE GUIDE.md`
- `PUBLIC READER GUIDE.md`
- `AI HANDOFF GUIDE.md`
- `HOW THIS HUB WORKS.md`
- `01-platform/`
- `02-platform-studio-library/`
- `03-factory/`
- `05-flows/`
- `06-templates/`
- `08-design-intelligence/`

## 2. Không Đưa Lên Hoặc Dọn Trước Khi Public

- credential
- cookie
- token
- browser profile path
- absolute path kiểu `/Users/...`
- domain / page thật không cần thiết trong lớp core
- page-specific spec/report không phục vụ public reader
- report lịch sử gây hiểu nhầm là luật hiện hành

## 3. Rà Soát Bắt Buộc

Phải search toàn bộ repo trước khi public:

- `Aa123`
- `token`
- `cookie`
- `/Users/`
- `primelandhcm.com`
- `wp-admin`
- tên page test
- thông tin VPS nội bộ

Nếu còn xuất hiện trong lớp core:

- phải xóa, ẩn, hoặc chuyển sang archive/private

## 4. Tách Đúng Lớp

### Public core

Là phần đưa lên GitHub để người đọc học hệ:

- luật
- flow
- factory
- template
- design intelligence

### Private / local only

Là phần nên giữ ngoài repo public hoặc dọn trước:

- `VPS/tmp/`
- page-specific delivery artifacts
- runtime helper gắn với site thật
- log thao tác nội bộ

### History / archive

Chỉ giữ nếu còn giá trị giải thích.
Nếu giữ thì phải ghi rõ:

- không phải source of truth

## 5. File Repo-Level Nên Có

Trước khi public nên có:

- `README.md`
- `LICENSE`
- `.gitignore`
- `V1.1 RELEASE GUIDE.md`
- `GITHUB PUBLIC CHECKLIST.md`

Nếu muốn public đẹp hơn:

- `CHANGELOG.md`

## 6. Đường Public An Toàn Nhất

1. rà secret và path nội bộ
2. tách `core` và `private/history`
3. dọn report gây nhiễu
4. kiểm lại entry docs
5. push `V1.1 public-safe`

## 7. Điều Không Được Làm

- không public khi chưa rà secret
- không để absolute path đầy trong core docs
- không để report task cụ thể giả làm luật
- không đưa runtime site-specific lên repo công khai nếu chưa dọn sạch

## 8. Kết Luận

Muốn đưa lên GitHub nhanh và an toàn, phải public `core knowledge hub`, không public cả đống local artifact.
