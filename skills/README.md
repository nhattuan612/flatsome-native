# Skills — Flatsome Native Knowledge Hub

## 📥 Cài Đặt / Installation

Copy 3 thư mục con vào thư mục `skills/` của AI IDE bạn đang dùng:

### Antigravity / Codex

```bash
# Clone repo (nếu chưa có)
git clone https://github.com/nhattuan612/flatsome-native.git

# Copy skills vào Antigravity
cp -r flatsome-native/skills/flatsome-native-builder ~/.gemini/antigravity/skills/
cp -r flatsome-native/skills/flatsome-native-harvest ~/.gemini/antigravity/skills/
cp -r flatsome-native/skills/flatsome-native-design-intelligence ~/.gemini/antigravity/skills/
```

### Claude Desktop / Cursor / VS Code

Đặt toàn bộ thư mục `flatsome-native/` vào workspace, sau đó nạp file `MASTER OPERATING MEMORY.md` vào context đầu tiên.

---

## 🧠 3 Skills Có Sẵn

| Skill | Call Phrase | Mục Đích |
|---|---|---|
| **flatsome-native-builder** | `use flatsome-native-builder_(Build_Trang)` | Build trang Flatsome chuẩn native |
| **flatsome-native-harvest** | `use flatsome-native-harvest_(Hoc_Them_UI)` | Harvest thêm UI từ Flatsome Studio |
| **flatsome-native-design-intelligence** | `use flatsome-native-design-intelligence_(Sang_Tao)` | Sáng tạo nâng cao, đổi design language |

## 🔗 Quan Hệ Giữa 3 Skill

```
Builder (cửa chính) ←→ Design Intelligence (cửa sáng tạo)
    ↕
Harvest (cửa học thêm tri thức)
```

- **Builder** là skill chính, dùng cho mọi task build trang
- **Harvest** mở rộng thư viện tri thức khi cần hút thêm template/slot
- **Design Intelligence** chỉ mở khi cần sáng tạo mạnh hơn mặc định

## 📄 License

MIT — xem [LICENSE](../LICENSE)
