# Checklist 12 điểm kiểm duyệt & Xuất bản Bài Lab (Anti-AI & Scalability Gate)

Trước khi xuất bản hoặc hoàn tất chỉnh sửa bất kỳ bài Lab nào (bao gồm cả `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT_TEMPLATE.md`), hãy rà soát văn bản qua 12 tiêu chí sau:

---

### Nhóm 1: Khử rác AI & Giọng điệu kỹ sư (Tone & Anti-Slop)

1. **Đã thống nhất gọi là "Lab" chưa?**
   - *Đạt:* Dùng "Lab", "Bài lab", "Lab #X". Tuyệt đối không có bất kỳ chữ "Codelab" hay "Codelabs" nào.

2. **Có dính emoji trang trí không?**
   - *Đạt:* 0 emoji trong toàn bộ văn bản (trừ các ký hiệu kỹ thuật như nút chạy `▶` hoặc mũi tên luồng `→`).

3. **Có câu chào mừng / dỗ dành non-tech không?**
   - *Đạt:* Bắt đầu trực diện vào mục tiêu kỹ thuật hoặc thao tác đầu tiên. Không có *"Chào mừng..."*, *"Đừng lo lắng..."*, *"Cầm tay chỉ việc..."*.

4. **Có ví von ngô nghê / nhân hóa AI không?**
   - *Đạt:* Trình bày bản chất khoa học (xác suất, mô hình tính toán, hàm mục tiêu). Không có *"mắt thần"*, *"AI đoán bừa"*, *"áo may đo"*, *"thùng carton"*.

---

### Nhóm 2: Thuật ngữ & Quy chuẩn dịch thuật (Terminology)

5. **Có giữ nguyên các thuật ngữ tiếng Anh chuẩn không?**
   - *Đạt:* `bounding box`, `checkpoint`, `ground truth`, `prediction`, `score`, `threshold`, `file ZIP`, `pipeline`, `token`, `prompt` được giữ nguyên, không bị dịch gượng ép sang "hộp giới hạn", "sự thật", "tệp", v.v.

6. **Đã áp dụng đúng quy tắc Song ngữ lần đầu (First-Mention) chưa?**
   - *Đạt:* Chỉ mở ngoặc chú thích tiếng Anh ở lần đầu tiên từ đó xuất hiện trong file. Các lần sau dùng duy nhất 1 từ nhất quán, không lặp lại dấu ngoặc đơn.

7. **Có dùng từ ngữ thao tác máy tính tự nhiên không?**
   - *Đạt:* Dùng "chạy ô", "mở", "chọn", "click chuột phải", "click đúp", "file", "local". Không dùng "thực thi", "tiến hành", "nhấp phải", "nhấp đúp", "tệp", "cục bộ".

8. **Các mệnh lệnh cấm có ngắn gọn, dứt khoát không?**
   - *Đạt:* Nêu rõ điều cấm trực tiếp (ví dụ: *"Không ghi lại họ tên, MSSV trong báo cáo"*). Không lên lớp đạo đức hay giải thích dài dòng về PII trừ khi tài liệu gốc yêu cầu.

---

### Nhóm 3: Tính Đồng bộ Đa tài liệu & Tính Kế thừa (Multi-Doc & Scalability)

9. **Tính đồng bộ tuyệt đối giữa các file trong bài lab (Cross-Document Consistency):**
   - *Đạt:* Các thông số giữa `README.md`, `GUIDE.md`, `RUBRIC.md` và `notebook` khớp nhau 100%:
     - Release tag giống hệt nhau (ví dụ: cùng là `v1.0.1`).
     - Tên file nộp bài giống hệt nhau (ví dụ: cùng là `KX-DAYXX-report.zip`).
     - Cấu trúc cây thư mục nộp bài khớp từng thư mục con.

10. **Thống nhất thuật ngữ xuyên suốt các file:**
    - *Đạt:* Không có hiện tượng file này dùng "phân đoạn đối tượng", file kia lại tự ý đổi thành "phân đoạn cá thể" hay "phân đoạn thực thể".

11. **Rõ ràng về chế độ làm việc (Work Mode):**
    - *Đạt:* Xác định rõ là bài cá nhân (`individual` $\to$ repo `KX-DAYXX-HoVaTen-MSSV`, chấm ẩn danh) hay bài nhóm (`team` $\to$ repo `KX-DAYXX-TenNhom`, có file `TEAMMATES.md`).

12. **Bảo toàn dữ kiện & Không rò rỉ context AI:**
    - *Đạt:* Giữ nguyên link GitHub template chính thức; không rò rỉ các từ khóa AI nội bộ như "Antigravity", "assistant", "system prompt".
