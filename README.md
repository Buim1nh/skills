# Agent Skills Collection

Tập hợp các kỹ năng (skills) dành cho Claude Code, Cursor, Cline, Codex và các AI coding agent, được thiết kế và tối ưu cho quy trình kỹ thuật thực tế.

---

| Tên Skill | Mô tả ngắn | Lệnh cài đặt nhanh |
| :--- | :--- | :--- |
| **`lab-humanizer`** | Biên tập và chuẩn hóa tài liệu kỹ thuật đào tạo (Lab, README, Guide, Rubric, Report); loại bỏ văn AI dịch thô và chatbot nịnh nọt; đảm bảo đồng bộ 100% giữa các file trong repository. | `npx skills add Buim1nh/skills --skill lab-humanizer -g -y` |

---

## Hướng dẫn Cài đặt

### Cài đặt toàn bộ skills:
```bash
npx skills add Buim1nh/skills --all -g -y
```

### Cài đặt riêng skill `lab-humanizer`:
```bash
npx skills add Buim1nh/skills --skill lab-humanizer -g -y
```

*(Dùng cờ `-g` để cài đặt global trên máy, hoặc bỏ `-g` nếu chỉ cài cho project hiện tại).*

---

## Chi tiết Kỹ năng

### `lab-humanizer`
Biên tập và chuẩn hóa tài liệu bài lab hướng dẫn (Lab, README, Guide, Rubric, Report) sang văn phong kỹ sư thực chiến tự nhiên, gãy gọn, chuẩn xác.

**Các quy chuẩn cốt lõi:**
- **Định danh theo vai trò:** Đặt tên tài liệu tự nhiên theo đúng chức năng (Bài thực hành/Lab, Hướng dẫn thực hành `GUIDE.md`, Tiêu chí đánh giá `RUBRIC.md`, Báo cáo `REPORT.md`). Tránh dùng từ lai tạp như "Codelab".
- **Khử 2 thái cực văn AI:**
  - *Chống dịch máy thô (Anti-Translationese):* Chuẩn hóa từ ngữ giao diện và kỹ thuật (`local` thay vì `cục bộ`, `file` thay vì `tệp`, `click chuột phải`, `chạy ô`, thay `bằng chứng` bằng `số liệu dẫn chứng / kết quả bài làm`).
  - *Chống chatbot ru ngủ (Anti-Chatbot Slop):* Cắt sạch văn chào đón xã giao, trấn an tâm lý non-tech, khen ngợi cảm tính, các phép ẩn dụ sinh hoạt đời thường và nhân hóa máy móc; 0 emoji trang trí.
- **Bộ lọc 3 câu hỏi cho thuật ngữ tiếng Anh:** Giữ nguyên tiếng Anh cho các từ gắn liền với code, các từ cộng đồng kỹ sư dùng trực tiếp (`bounding box`, `checkpoint`, `ground truth`, `prediction`, `score`, `threshold`, `prompt`, `token`, `file ZIP`), và cấm dịch khi làm sai lệch bản chất kỹ thuật.
- **Quy tắc Song ngữ lần đầu (First-Mention):** Chỉ chú thích song ngữ Anh - Việt ở lần đầu tiên xuất hiện trong từng file; các lần sau dùng 1 từ nhất quán.
- **Khóa Đồng bộ Đa tài liệu (Multi-Document Consistency):** Khóa tính nhất quán 100% giữa `README.md`, `GUIDE.md`, `RUBRIC.md` và `notebook` về release tag, cấu trúc thư mục nộp bài và thuật ngữ kỹ thuật.
- **Bảo toàn dữ kiện:** Giữ nguyên 100% URL template, tham số kỹ thuật và logic code.

---

## License
MIT License
