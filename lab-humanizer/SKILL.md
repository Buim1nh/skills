---
name: lab-humanizer
description: Duyệt, lọc và chỉnh sửa nội dung hướng dẫn bài lab tiếng Việt sang văn phong kỹ sư thực chiến tự nhiên, chính xác. Thống nhất tên gọi "Lab" (không dùng "Codelab"). Loại bỏ triệt để cả hai thái cực văn AI (dịch máy thô cứng kiểu word-by-word và chatbot nịnh nọt/vỗ về non-tech/spam emoji). Chuẩn hóa thuật ngữ chuyên ngành và bảo toàn dữ kiện kỹ thuật.
license: MIT
---

# Lab Humanizer

Skill chuyên dụng để **duyệt, lọc, chỉnh sửa và đồng bộ tài liệu hướng dẫn bài lab (Lab / Markdown / README / GUIDE)** dành cho sinh viên và kỹ sư công nghệ trong các khóa học AI/ML/DL, Data Science và Kỹ thuật Phần mềm.

Mục tiêu tối thượng: Biến văn bản sinh bởi AI hoặc dịch máy thành **tài liệu lab chuẩn mực, sắc sảo, tự nhiên, mang đúng giọng điệu của một Kỹ sư / Giảng viên thực chiến** đứng lớp; đồng thời **đảm bảo tính tương thích và khả năng mở rộng (scalability) cho toàn bộ các bài lab trong tương lai**.

---

## 0. Quy ước định danh chung
- **Thống nhất tên gọi:** Luôn gọi là **"Lab"** hoặc **"Bài lab"** (ví dụ: *Bài lab Ngày 1*, *Lab #1*, *tài liệu lab*).
- **Cấm sử dụng:** Không dùng từ *"Codelab"*, *"bài codelab"*, *"Codelabs"*.

---

## Hai thái cực "Văn AI" cần loại bỏ

Một bài lab viết dở bởi AI thường rơi vào một trong hai thái cực:

### 1. Thái cực "AI Dịch máy thô cứng" (Translationese Slop)
- Dịch word-by-word từ tiếng Anh: *evidence* $\to$ "bằng chứng" (nghe như hình sự), *local* $\to$ "cục bộ" (*ổ đĩa cục bộ*, *môi trường cục bộ*), *tight box* $\to$ "hộp chặt".
- Dịch giao diện kiểu cũ: "nhấp phải", "nhấp đúp", "tệp tin".
- Hành chính hóa từ ngữ: "thực thi ô mã", "tiến hành triển khai", "đồng nhất trên mọi hệ thống".
- Viết câu rườm rà, máy móc: *"Không có lệnh cài đặt hệ thống, đường dẫn ổ đĩa cục bộ hoặc script riêng cho một hệ điều hành..."*
- Rò rỉ context/prompt nội bộ của AI (ví dụ: tự ý nhét từ khóa "Antigravity", "assistant").

### 2. Thái cực "AI Chatbot vỗ về, nịnh nọt" (Patronizing Chatbot Slop)
- Giọng điệu ru ngủ, hạ thấp người học: *"Chào mừng bạn đến với buổi học đầu tiên!"*, *"Nếu bạn là người mới (non-tech), đừng lo lắng!"*, *"Cầm tay chỉ việc"*, *"Chúc mừng bạn đã hoàn thành!"*.
- Ví von ngô nghê, kỳ cục: ví AI với "con chó, con mèo", ví taxonomy với "thực đơn món ăn", ví bounding box với "thùng carton", polygon với "áo may đo", gọi AI là "mắt thần", bắt học viên "mở mắt xem kết quả".
- Nhân hóa AI phản khoa học: *"AI đoán bừa"*, *"Độ tự tin của AI"*, gọi Ground Truth là *"thước đo chân lý"*.
- Lạm dụng Emoji tràn lan (`💡`, `📖`, `👉`, `🛡️`, `🖥️`, `📁`, `🛠️`).

---

## 5 Trụ cột Quy chuẩn Cốt lõi (Core Quality Gates)

### Trụ cột 1: Tông giọng Kỹ sư thực chiến (Direct Engineering Tone)
- **Vào thẳng vấn đề:** Bắt đầu bằng mục tiêu kỹ thuật hoặc thao tác đầu tiên. Tuyệt đối không có lời mở đầu sáo rỗng.
- **Dùng từ kỹ thuật tự nhiên của kỹ sư:**
  - Dùng: `chạy ô`, `mở`, `chọn`, `lưu`, `click chuột phải`, `click đúp`, `file`, `local`.
  - Cấm: `thực thi`, `tiến hành`, `nhấp phải`, `nhấp đúp`, `tệp`, `cục bộ`, `đồng nhất`.
- **Chỉ dẫn ngắn gọn, cấm là cấm:** Khi có quy định cấm (như không điền MSSV vào báo cáo), ghi trực tiếp mệnh lệnh. Không thêm văn giáo điều, không lên lớp đạo đức hay giải thích dài dòng về PII trừ khi tài liệu gốc yêu cầu.
- **Tiêu đề tiếng Việt tự nhiên:** Giữ nguyên các đề mục chuẩn như *"Kiểm tra trước khi chạy"*, *"Điều kiện hoàn thành"*, không sính ngoại thành *"Pre-run checklist"*, *"Pre-flight"*.

### Trụ cột 2: Chuẩn hóa Thuật ngữ & Quy tắc Song ngữ lần đầu
- **Không dịch cưỡng ép các từ tiếng Anh chuẩn:** 
  - Giữ nguyên: `bounding box` (hoặc `box`), `checkpoint`, `ground truth`, `prediction`, `pipeline`, `score`, `threshold`, `instance segmentation`, `object detection`, `classification`, `polygon`, `prompt`, `token`, `embeddings`, `file ZIP`.
  - Tuyệt đối không dịch thành: "hộp giới hạn", "sự thật mặt đất", "tệp nén", "lời nhắc", "đồng xu".
- **Quy tắc Song ngữ lần đầu (First-Mention Rule):**
  - Chỉ mở ngoặc giải thích tiếng Anh ở **lần đầu tiên** thuật ngữ xuất hiện trong mỗi file (ví dụ: `danh mục nhãn (taxonomy)` hoặc `phân loại ảnh (image classification)`).
  - Từ lần thứ 2 trở đi: Dùng duy nhất **1 từ nhất quán**, cấm lặp lại ngoặc đơn gây rối mắt.
- **Không nhân hóa AI:**
  - Dùng: "điểm số dự đoán (score)", "mô hình tính toán", "kết quả dự đoán".
  - Cấm: "độ tự tin của AI", "AI đoán bừa", "AI phán đoán".
  - Ground truth là "nhãn chuẩn do con người xác nhận theo quy chuẩn (guideline)", không phải "chân lý".

### Trụ cột 3: Xóa sạch Emoji & Phép so sánh ngô nghê
- Xóa 100% các emoji trang trí ở tiêu đề, danh sách, callout.
- Bỏ toàn bộ các bảng ví von "đời thực" kiểu cấp 1 (con mèo, áo may đo, thực đơn). Thay bằng giải thích bản chất kỹ thuật trực diện hoặc lược bỏ nếu không cần thiết.

### Trụ cột 4: Đồng bộ Đa tài liệu trong Repo (Cross-Document Consistency)
- Trong một repo bài lab, các file `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT_TEMPLATE.md` và mã nguồn notebook phải **nhất quán 100%**:
  - Khớp chính xác release tag (ví dụ: cùng là `v1.0.1`).
  - Khớp cú pháp đặt tên repository (`KX-DAYXX-HoVaTen-MSSV` cho cá nhân, `KX-DAYXX-TenNhom` cho nhóm).
  - Khớp tên file nộp bài (`KX-DAYXX-report.zip`).
  - Khớp cấu trúc cây thư mục nộp bài (`report/`, các file con bên trong).
  - Đã chọn một cách dịch thuật ngữ nào thì toàn bộ các file trong bài lab phải dùng chung (không để file này dùng "phân đoạn đối tượng", file kia dùng "phân đoạn cá thể").

### Trụ cột 5: Bảo toàn Dữ kiện & Khả năng Mở rộng (Scalability & Facts)
- Dễ dàng mở rộng cho các bài lab tiếp theo (Tabular, NLP, LLM, MLOps) bằng cách tra cứu các domain tương ứng trong `references/vocabulary-rules.md`.
- Bảo toàn tuyệt đối đường link GitHub template, các tham số dòng lệnh và ô code trong notebook.

---

## Quy trình duyệt & đồng bộ văn bản (Review Workflow)

Khi nhận một file hoặc một bài lab cần duyệt/đồng bộ, thực hiện lần lượt 4 bước:

1. **Bước 1: Quét và loại bỏ rác AI (Scan & Strip Slop)**
   - Đổi toàn bộ các từ "Codelab/Codelabs" $\to$ "Lab/Labs".
   - Quét xóa toàn bộ Emoji trang trí.
   - Xóa bỏ các đoạn văn mở đầu chào mừng, dỗ dành non-tech, cổ vũ sáo rỗng.
   - Xóa bỏ các phép ví von đời thực khập khiễng, các câu nhân hóa AI ("đoán bừa", "mắt thần").
2. **Bước 2: Thay thế từ vựng theo bảng chuẩn đa lĩnh vực (Vocabulary Normalization)**
   - Tra cứu và thay thế theo `references/vocabulary-rules.md`:
     - "cục bộ" $\to$ "local"
     - "bằng chứng" $\to$ "kết quả bài làm" / "số liệu dẫn chứng".
     - "hộp giới hạn" $\to$ "bounding box".
     - "nhấp phải" $\to$ "click chuột phải".
     - "tệp" $\to$ "file".
     - "thực thi" $\to$ "chạy".
3. **Bước 3: Mài giũa câu từ & Áp dụng First-Mention (Polish & Flow)**
   - Rà soát các thuật ngữ: chỉ để song ngữ Anh - Việt ở lần đầu tiên xuất hiện trong file.
   - Chỉnh các câu văn bị động, dài dòng thành câu ngắn gọn, trực diện, mạch lạc.
4. **Bước 4: Kiểm tra Đồng bộ Đa tài liệu & Đối soát Checklist (Multi-Doc & Checklist Gate)**
   - Đối soát chéo giữa `README.md`, `GUIDE.md`, `RUBRIC.md` và notebook theo `references/multi-doc-consistency.md`.
   - Rà soát qua 12 điểm trong `references/anti-ai-checklist.md`.

---

## Tài liệu tham chiếu đi kèm

- `references/vocabulary-rules.md`: Bảng tra cứu từ vựng chuẩn đa lĩnh vực (Universal, CV, NLP/LLM, Tabular, Platforms).
- `references/multi-doc-consistency.md`: Quy chuẩn đồng bộ đa tài liệu giữa `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT.md`.
- `references/anti-ai-checklist.md`: 12 tiêu chí kiểm tra chất lượng trước khi bàn giao/release bài lab.
