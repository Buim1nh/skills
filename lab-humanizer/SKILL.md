---
name: lab-humanizer
description: Duyệt, lọc và chỉnh sửa nội dung hướng dẫn bài lab tiếng Việt sang văn phong kỹ sư thực chiến tự nhiên, chính xác. Thống nhất tên gọi "Lab" (không dùng "Codelab"). Loại bỏ triệt để cả hai thái cực văn AI (dịch máy thô cứng kiểu word-by-word và chatbot nịnh nọt/vỗ về non-tech/spam emoji). Chuẩn hóa thuật ngữ chuyên ngành và bảo toàn dữ kiện kỹ thuật.
license: MIT
---

# Lab Humanizer

Skill chuyên dụng để **duyệt, lọc, chỉnh sửa và đồng bộ tài liệu hướng dẫn bài lab (Lab / Markdown / README / GUIDE)** dành cho sinh viên và kỹ sư công nghệ trong các khóa học AI/ML/DL, Data Science và Kỹ thuật Phần mềm.

Mục tiêu tối thượng: Biến văn bản sinh bởi AI hoặc dịch máy thành **tài liệu lab chuẩn mực, sắc sảo, tự nhiên, mang đúng giọng điệu của một Kỹ sư / Giảng viên thực chiến** đứng lớp; đồng thời **đảm bảo tính tương thích và khả năng mở rộng (scalability) cho mọi bài lab trong tương lai**.

---

## 0. Quy ước định danh chung
- **Thống nhất tên gọi:** Luôn gọi là **"Lab"** hoặc **"Bài lab"** (ví dụ: *Bài lab Ngày 1*, *Lab #1*, *tài liệu lab*).
- **Cấm sử dụng:** Tuyệt đối không dùng từ *"Codelab"*, *"bài codelab"*, *"Codelabs"*.

---

## Hai thái cực "Văn AI" cần loại bỏ

Một bài lab viết dở bởi AI thường rơi vào một trong hai thái cực:

### 1. Thái cực "AI Dịch máy thô cứng" (Translationese Slop)
- **Dịch word-by-word:** *evidence* $\to$ "bằng chứng" (nghe như hình sự), *local* $\to$ "cục bộ" (*ổ đĩa cục bộ*, *môi trường cục bộ*), *tight box* $\to$ "hộp chặt".
- **Dịch giao diện kiểu cũ:** "nhấp phải", "nhấp đúp", "tệp tin".
- **Hành chính hóa từ ngữ:** "thực thi ô mã", "tiến hành triển khai", "đồng nhất trên mọi hệ thống".
- **Viết câu rườm rà, liệt kê phủ định:** *"Không có lệnh cài đặt hệ thống, đường dẫn ổ đĩa cục bộ hoặc script riêng cho một hệ điều hành..."*

### 2. Thái cực "AI Chatbot vỗ về, nịnh nọt" (Patronizing Chatbot Slop)
- **Giọng điệu ru ngủ, hạ thấp người học:** *"Chào mừng bạn đến với buổi học đầu tiên!"*, *"Nếu bạn là người mới (non-tech), đừng lo lắng!"*, *"Cầm tay chỉ việc"*, *"Chúc mừng bạn đã hoàn thành!"*.
- **Ví von ngô nghê, gượng ép:** Ví thuật toán AI với "con chó, con mèo", ví taxonomy với "thực đơn món ăn", ví bounding box với "thùng carton", polygon với "áo may đo", gọi AI là "mắt thần", bắt học viên "mở mắt xem kết quả".
- **Nhân hóa máy móc phản khoa học:** *"AI đoán bừa"*, *"Độ tự tin của AI"*, gọi Ground Truth là *"thước đo chân lý"*.
- **Lạm dụng Emoji:** Rải emoji vô tội vạ (`💡`, `📖`, `👉`, `🛡️`, `🖥️`, `📁`, `🛠️`).

---

## 4 Trụ cột Quy chuẩn Cốt lõi (Core Quality Gates)

### Trụ cột 1: Tông giọng Kỹ sư thực chiến (Direct Engineering Tone)
- **Vào thẳng vấn đề:** Bắt đầu trực diện bằng bối cảnh kỹ thuật hoặc thao tác đầu tiên. Tuyệt đối không có lời mở đầu sáo rỗng.
- **Quy tắc Động từ Hành động (Action-Oriented Verbs):**
  - Dùng trực tiếp động từ mô tả hành vi giao diện/hệ thống: `chạy ô`, `mở`, `chọn`, `lưu`, `click chuột phải`, `click đúp`, `file`, `local`.
  - Xóa sạch từ đệm quan liêu và dịch máy cũ: `thực thi`, `tiến hành`, `nhấp phải`, `nhấp đúp`, `tệp`, `cục bộ`, `đồng nhất`.
- **Mệnh lệnh ngắn gọn, dứt khoát:** Khi có quy định cấm (như không điền MSSV vào báo cáo), ghi trực tiếp mệnh lệnh. Không thêm văn giáo điều, không lên lớp đạo đức hay giải thích dài dòng về PII trừ khi tài liệu gốc yêu cầu.
- **Tiêu đề tiếng Việt tự nhiên:** Giữ nguyên các đề mục chuẩn như *"Kiểm tra trước khi chạy"*, *"Điều kiện hoàn thành"*, không sính ngoại thành *"Pre-run checklist"*, *"Pre-flight"*.

### Trụ cột 2: Chuẩn hóa Thuật ngữ theo Bộ lọc 3 câu hỏi (The 3-Question Heuristic)
Khi gặp một thuật ngữ tiếng Anh, không phụ thuộc vào danh sách liệt kê cứng mà tự động kiểm tra qua 3 câu hỏi:
1. **Có gắn liền với Code/API/Tham số không?** (ví dụ: `bbox_xyxy`, `conf`, `IoU`, `learning_rate`, `prompt`, `token`) $\rightarrow$ **Giữ 100% tiếng Anh**.
2. **Cộng đồng kỹ sư thực tế dùng trực tiếp không?** (ví dụ: `checkpoint`, `ground truth`, `prediction`, `pipeline`, `score`, `threshold`, `file ZIP`) $\rightarrow$ **Giữ nguyên tiếng Anh**.
3. **Dịch ra có làm sai lệch bản chất kỹ thuật không?** (ví dụ: `ground truth` thành "sự thật", `pipeline` thành "đường ống") $\rightarrow$ **Cấm dịch**.
*(Khi cần tra cứu chuẩn hóa cho các domain cụ thể như CV, NLP, Tabular, tra cứu trực tiếp trong `references/vocabulary-rules.md`).*

- **Quy tắc Song ngữ lần đầu (First-Mention Rule):**
  - Chỉ mở ngoặc giải thích tiếng Anh ở **lần đầu tiên** thuật ngữ xuất hiện trong mỗi file (ví dụ: `danh mục nhãn (taxonomy)` hoặc `phân loại ảnh (image classification)`).
  - Từ lần thứ 2 trở đi: Dùng duy nhất **1 từ nhất quán**, cấm lặp lại ngoặc đơn gây rối mắt.
- **Không nhân hóa AI:**
  - Dùng: "điểm số dự đoán (score)", "mô hình tính toán", "kết quả dự đoán".
  - Cấm: "độ tự tin của AI", "AI đoán bừa", "AI phán đoán".
  - Ground truth là "nhãn chuẩn do con người xác nhận theo quy chuẩn (guideline)", không phải "chân lý".

### Trụ cột 3: Bản chất Khoa học & Xóa sạch Ẩn dụ ngô nghê
- Xóa 100% emoji trang trí ở tiêu đề, danh sách, callout.
- Cấm mượn đồ vật sinh hoạt đời thường (quần áo, thùng hộp, con vật, thần chú) để ví von cho thuật toán. Trình bày hiện tượng thuần túy bằng bản chất toán học và khoa học máy tính (xác suất, phân phối, hàm mục tiêu, ma trận, vector).

### Trụ cột 4: Khóa Đồng bộ Đa tài liệu trong Repo (Cross-Document Consistency)
- Trong một repo bài lab, các file `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT_TEMPLATE.md` và mã nguồn notebook phải **nhất quán 100%**:
  - Khớp chính xác release tag (ví dụ: cùng là `v1.0.1`).
  - Khớp cú pháp đặt tên repository (`KX-DAYXX-HoVaTen-MSSV` cho cá nhân, `KX-DAYXX-TenNhom` cho nhóm).
  - Khớp tên file nộp bài (ví dụ: `KX-DAYXX-report.zip`).
  - Khớp cấu trúc cây thư mục nộp bài (`report/`, các file con bên trong).
  - Khóa thuật ngữ toàn cục: Một thuật ngữ đã chọn phải dùng đồng nhất trên toàn bộ các file trong repository (chi tiết tại `references/multi-doc-consistency.md`).

---

## Quy trình duyệt & đồng bộ văn bản (Review Workflow)

Khi nhận một file hoặc một bài lab cần duyệt/đồng bộ, thực hiện lần lượt 4 bước:

1. **Bước 1: Quét và loại bỏ rác AI (Scan & Strip Slop)**
   - Đổi toàn bộ các từ "Codelab/Codelabs" $\to$ "Lab/Labs".
   - Quét xóa toàn bộ Emoji trang trí.
   - Xóa bỏ các đoạn văn mở đầu chào mừng, dỗ dành non-tech, cổ vũ sáo rỗng.
   - Xóa bỏ các phép ví von đời thực khập khiễng, các câu nhân hóa AI ("đoán bừa", "mắt thần").
2. **Bước 2: Chuẩn hóa thuật ngữ & động từ thao tác (Normalize Terminology & Actions)**
   - Áp dụng Bộ lọc 3 câu hỏi cho thuật ngữ tiếng Anh; tra cứu thêm tại `references/vocabulary-rules.md`.
   - Áp dụng Quy tắc Động từ Hành động: thay các từ hành chính hóa ("thực thi", "tiến hành", "đồng nhất", "cục bộ", "tệp") bằng động từ kỹ sư tự nhiên ("chạy ô", "mở", "chọn", "local", "file").
3. **Bước 3: Mài giũa câu từ & Áp dụng First-Mention (Polish & Flow)**
   - Rà soát các thuật ngữ: chỉ để song ngữ Anh - Việt ở lần đầu tiên xuất hiện trong từng file.
   - Chỉnh các câu văn bị động, dài dòng thành câu ngắn gọn, trực diện, mạch lạc.
4. **Bước 4: Kiểm tra Đồng bộ Đa tài liệu & Đối soát Checklist (Multi-Doc & Checklist Gate)**
   - Đối soát chéo giữa `README.md`, `GUIDE.md`, `RUBRIC.md` và notebook theo `references/multi-doc-consistency.md`.
   - Rà soát qua 10 tiêu chí phán đoán trong `references/anti-ai-checklist.md`.

---

## Tài liệu tham chiếu đi kèm

- `references/vocabulary-rules.md`: Sổ tay tra cứu thuật ngữ chuyên ngành đa lĩnh vực (Universal, CV, NLP/LLM, Tabular, Platforms).
- `references/multi-doc-consistency.md`: Quy chuẩn khóa đồng bộ đa tài liệu giữa `README.md`, `GUIDE.md`, `RUBRIC.md`, `REPORT.md`.
- `references/anti-ai-checklist.md`: 10 tiêu chí phán đoán kiểm tra chất lượng trước khi release bài lab.
