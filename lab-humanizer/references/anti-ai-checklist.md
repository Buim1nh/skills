# Checklist 10 điểm kiểm duyệt Bài Lab (Anti-AI & Scalability Gate)

Trước khi xuất bản hoặc hoàn tất chỉnh sửa bất kỳ bài Lab nào (bao gồm cả `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT_TEMPLATE.md`), hãy rà soát văn bản qua 10 tiêu chí phán đoán (Heuristics) sau:

---

### Nhóm 1: Giọng điệu kỹ sư & Khử rác AI (Tone & Anti-Slop)

1. **Định danh chuẩn xác theo vai trò tài liệu (Loại bỏ hoàn toàn từ "Codelab"):**
   - *Nguyên tắc:* 
     - **Tuyệt đối loại bỏ:** 0 chữ "Codelab" hoặc "Codelabs" trong toàn bộ văn bản.
     - **Gọi tên tự nhiên theo đúng vai trò tài liệu:**
       - Tài liệu bài tập / thực hành: Dùng **"Bài thực hành"**, **"Lab"**, hoặc **"Bài lab"** (ví dụ: *Bài thực hành Ngày 1*, *Lab #1*).
       - Tài liệu giới thiệu repo (`README.md`): Dùng **"Bài thực hành Ngày X"** hoặc tên đề tài/dự án kỹ thuật tương ứng.
       - Tài liệu hướng dẫn chi tiết / cẩm nang (`GUIDE.md`): Dùng **"Hướng dẫn thực hành"**, **"Cẩm nang hướng dẫn"**.
       - Tài liệu tiêu chí đánh giá (`RUBRIC.md`): Dùng **"Tiêu chí đánh giá"**, **"Rubric đánh giá"**.
       - Tài liệu báo cáo sinh viên (`REPORT.md`): Dùng **"Báo cáo thực hành"**, **"Báo cáo bài làm"**.
2. **Bộ lọc Ký tự thừa (Visual & Decoration Filter):**
   - *Nguyên tắc:* 0 emoji trang trí trong toàn bộ văn bản (chỉ chấp nhận các ký hiệu kỹ thuật như nút chạy `▶` hoặc mũi tên luồng `→`).

3. **Bộ lọc Cảm xúc & Xã giao (Emotional & Social Tone Filter):**
   - *Nguyên tắc:* Bất kỳ câu nào mang tính chất: (1) Chào đón xã giao, (2) Trấn an tâm lý/trình độ người học (non-tech), (3) Cổ vũ/khen ngợi cảm tính, hoặc (4) Quảng bá khóa học $\rightarrow$ **Cắt bỏ 100%**. 
   - *Tiêu chuẩn:* Bài lab mở đầu trực diện bằng: Bối cảnh kỹ thuật $\rightarrow$ Thao tác $\rightarrow$ Kết quả cần quan sát.

4. **Bộ lọc Bản chất Khoa học (Scientific Grounding Filter):**
   - *Nguyên tắc:* 
     - Cấm mượn đồ vật sinh hoạt đời thường (con vật, đồ gia dụng, thần chú, quần áo) để ví von cho thuật toán.
     - Cấm nhân hóa máy móc (không dùng "AI đoán bừa", "độ tự tin của AI", "thước đo chân lý").
     - Định nghĩa và giải thích hiện tượng thuần túy bằng bản chất toán học/khoa học máy tính (xác suất, ma trận, vector, mô hình tính toán, nhãn chuẩn theo guideline).

---

### Nhóm 2: Thuật ngữ & Thao tác kỹ thuật (Terminology & Actions)

5. **Bộ lọc 3 câu hỏi cho Thuật ngữ tiếng Anh (The 3-Question Heuristic):**
   - *Nguyên tắc phán đoán khi gặp thuật ngữ tiếng Anh:*
     1. **Có gắn liền với Code/API/Tham số không?** (ví dụ: `bbox_xyxy`, `conf`, `IoU`, `learning_rate`, `prompt`, `token`) $\rightarrow$ **Giữ 100% tiếng Anh**.
     2. **Cộng đồng kỹ sư thực tế dùng trực tiếp không?** (ví dụ: `checkpoint`, `ground truth`, `prediction`, `file ZIP`) $\rightarrow$ **Giữ nguyên tiếng Anh**.
     3. **Dịch ra có làm sai lệch bản chất kỹ thuật không?** (ví dụ: `ground truth` thành "sự thật", `pipeline` thành "đường ống") $\rightarrow$ **Cấm dịch**.
   - *Tra cứu mở rộng:* Tra cứu bảng từ điển chuyên ngành trong `references/vocabulary-rules.md` khi gặp các thuật ngữ trong vùng xám.

6. **Quy tắc Song ngữ lần đầu (First-Mention Scope):**
   - *Nguyên tắc:* Mỗi file tài liệu là một điểm vào độc lập. Chỉ mở ngoặc chú thích tiếng Anh ở **lần đầu tiên** thuật ngữ xuất hiện trong file đó (ví dụ: `phân loại ảnh (image classification)`). Từ lần thứ 2 trở đi: Dùng duy nhất 1 từ thống nhất, không lặp lại dấu ngoặc đơn.

7. **Quy tắc Động từ Hành động Thực tế (Action-Oriented Verbs):**
   - *Nguyên tắc:* 
     - **1 Thao tác = 1 Động từ kỹ sư tự nhiên:** Dùng trực tiếp động từ mô tả hành vi giao diện/hệ thống (`chạy ô`, `mở`, `chọn`, `lưu`, `click chuột phải`, `click đúp`, `file`, `local`).
     - **Khử sạch từ đệm quan liêu:** Xóa toàn bộ các từ hành chính hóa và dịch máy cũ kỹ (`thực thi`, `tiến hành`, `triển khai việc`, `nhấp phải`, `tệp`, `cục bộ`, `đồng nhất`).

8. **Mệnh lệnh Trực diện (Direct Constraint Rule):**
   - *Nguyên tắc:* Khi có quy định cấm hoặc hạn chế, nêu mệnh lệnh ngắn gọn, dứt khoát (ví dụ: *"Không ghi lại họ tên, MSSV trong báo cáo"*). Không thêm văn giáo điều, không lên lớp đạo đức hay giải thích dài dòng về PII trừ khi tài liệu gốc yêu cầu.

---

### Nhóm 3: Tính Đồng bộ Đa tài liệu & Mở rộng (Multi-Doc & Scalability)

9. **Khóa Chân lý Đơn nhất (Single Source of Truth Lock):**
   - *Nguyên tắc:* Các thông số kỹ thuật (release tag, tên file nộp bài, cấu trúc thư mục nhận bài) phải khớp chính xác 100% giữa `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT_TEMPLATE.md` và mã nguồn notebook (theo hướng dẫn `references/multi-doc-consistency.md`).

10. **Khóa Thuật ngữ Toàn cục (Global Terminology Lock):**
    - *Nguyên tắc:* Một thuật ngữ kỹ thuật đã được chọn thì phải dùng đồng nhất trên toàn bộ các file trong repository của bài lab (không để hiện tượng file này dùng "phân đoạn đối tượng", file kia lại đổi thành "phân đoạn cá thể").
