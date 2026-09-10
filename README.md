# 🛠️ Agent Skills Collection

Bộ sưu tập các kỹ năng (Agent Skills) chuyên dụng cho Claude Code, Antigravity, Amp, Cline, Codex và các AI coding agents khác, được tối ưu hóa cho quy trình kỹ thuật thực tế.

---

## 📦 Danh sách Skills

| Tên Skill | Mô tả ngắn | Lệnh cài đặt nhanh |
| :--- | :--- | :--- |
| **`lab-humanizer`** | Duyệt, lọc và biên tập nội dung bài lab kỹ thuật; loại bỏ triệt để văn AI (dịch thô word-by-word và chatbot vỗ về/spam emoji); chuẩn hóa thuật ngữ chuyên ngành và thống nhất tên gọi "Lab". | `npx skills add Buim1nh/skills --skill lab-humanizer -g -y` |

---

## 🚀 Hướng dẫn Cài đặt

### Cài đặt toàn bộ skills (Global):
```bash
npx skills add Buim1nh/skills --all -g -y
```

### Cài đặt riêng từng skill:
```bash
npx skills add Buim1nh/skills --skill lab-humanizer -g -y
```

*(Thêm cờ `-g` để cài đặt global cho mọi dự án, hoặc bỏ `-g` nếu chỉ muốn cài riêng cho project hiện tại).*

---

## 🔍 Chi tiết các Kỹ năng

### 1. `lab-humanizer`
* **Mục tiêu:** Chuyển đổi các bài lab hướng dẫn sinh bởi AI hoặc dịch máy thành tài liệu chuẩn mực, gãy gọn, tự nhiên theo đúng phong cách của Kỹ sư / Giảng viên thực chiến.
* **Các quy tắc cốt lõi:**
  - **Thống nhất tên gọi:** Luôn dùng **"Lab" / "Bài lab"**, cấm dùng "Codelab / Codelabs".
  - **Khử 2 thái cực văn AI:**
    - *Anti-Translationese:* Bỏ các từ dịch máy sáo rỗng (*"bằng chứng"*, *"hộp chặt"*, *"tệp"*, *"nhấp phải"*, rò rỉ context AI).
    - *Anti-Chatbot Slop:* Cắt sạch câu chào mừng, dỗ dành non-tech (*"Đừng lo lắng!"*, *"Cầm tay chỉ việc"*), ví von ngô nghê (con chó/mèo, áo may đo, thực đơn), và xóa 100% Emoji trang trí.
  - **Chuẩn hóa thuật ngữ & Quy tắc First-Mention:** Giữ nguyên các thuật ngữ tiếng Anh chuẩn (`bounding box`, `checkpoint`, `ground truth`, `prediction`, `score`, `threshold`, `file ZIP`). Chỉ chú thích song ngữ Anh - Việt ở lần đầu tiên xuất hiện.
  - **Tông giọng kỹ sư:** Dùng từ thao tác tự nhiên (*"chạy ô"*, *"mở"*, *"chọn"*, *"click chuột phải"*), cấm từ ngữ hành chính hóa (*"thực thi"*, *"tiến hành"*, *"đồng nhất"*).
  - **Bảo toàn dữ kiện:** Giữ nguyên 100% URL, release tag, cấu trúc thư mục nộp bài.

---

## 📄 License
MIT License
