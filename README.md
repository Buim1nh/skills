# 🛠️ Agent Skills Collection

Bộ sưu tập các kỹ năng (Agent Skills) chuyên dụng cho Claude Code, Antigravity, Amp, Cline, Codex và các AI coding agents khác, được tối ưu hóa cho quy trình kỹ thuật thực tế.

---
| Tên Skill | Mô tả ngắn | Lệnh cài đặt nhanh |
| :--- | :--- | :--- |
| **`lab-humanizer`** | Duyệt, lọc, chuẩn hóa và đồng bộ tài liệu lab kỹ thuật đa lĩnh vực (CV, NLP/LLM, Tabular ML); loại bỏ triệt để văn AI; đảm bảo tính nhất quán 100% giữa README, GUIDE, RUBRIC và REPORT. | `npx skills add Buim1nh/skills --skill lab-humanizer -g -y` |

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
* **Các tính năng & Quy chuẩn cốt lõi:**
  - **Kiến trúc mở rộng đa lĩnh vực (Multi-Domain):** Hỗ trợ tra cứu từ vựng chuẩn cho cả Thị giác máy tính (CV), Xử lý ngôn ngữ tự nhiên (NLP/LLM), Dữ liệu bảng (Tabular ML) và MLOps.
  - **Đồng bộ đa tài liệu (Multi-Document Consistency):** Khóa chặt sự nhất quán 100% giữa các file trong cùng một repo bài lab (`README.md` $\leftrightarrow$ `GUIDE.md` $\leftrightarrow$ `RUBRIC.md` $\leftrightarrow$ `REPORT_TEMPLATE.md`).
  - **Hỗ trợ 2 chế độ bài làm:** Bài cá nhân (`individual` với định danh chấm ẩn danh) và bài nhóm (`team` với `TEAMMATES.md`).
  - **Khử 2 thái cực văn AI:**
    - *Anti-Translationese:* Bỏ các từ dịch máy sáo rỗng (*"cục bộ" $\to$ "local"*, *"bằng chứng" $\to$ "số liệu dẫn chứng"*, *"hộp chặt"*, *"tệp"*, *"nhấp phải"*, rò rỉ context AI).
    - *Anti-Chatbot Slop:* Cắt sạch câu chào mừng, dỗ dành non-tech (*"Đừng lo lắng!"*, *"Cầm tay chỉ việc"*), ví von ngô nghê (con chó/mèo, áo may đo, thực đơn), và xóa 100% Emoji trang trí.
  - **Chuẩn hóa thuật ngữ & Quy tắc First-Mention:** Giữ nguyên các thuật ngữ tiếng Anh chuẩn (`bounding box`, `checkpoint`, `ground truth`, `prediction`, `score`, `threshold`, `prompt`, `token`, `embeddings`, `file ZIP`). Chỉ chú thích song ngữ Anh - Việt ở lần đầu tiên xuất hiện trong file.
  - **Tông giọng kỹ sư:** Dùng từ thao tác tự nhiên (*"chạy ô"*, *"mở"*, *"chọn"*, *"click chuột phải"*), cấm từ ngữ hành chính hóa (*"thực thi"*, *"tiến hành"*, *"đồng nhất"*).
  - **Bảo toàn dữ kiện:** Giữ nguyên 100% URL, release tag, cấu trúc thư mục nộp bài.

---

## 📄 License
MIT License
