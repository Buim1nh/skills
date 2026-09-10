---
name: lab-humanizer
description: Duyệt, lọc và chỉnh sửa nội dung hướng dẫn bài lab tiếng Việt sang văn phong kỹ sư thực chiến tự nhiên, chính xác. Thống nhất tên gọi "Lab" (không dùng "Codelab"). Loại bỏ triệt để cả hai thái cực văn AI (dịch máy thô cứng kiểu word-by-word và chatbot nịnh nọt/vỗ về non-tech/spam emoji). Chuẩn hóa thuật ngữ chuyên ngành và bảo toàn dữ kiện kỹ thuật.
license: MIT
---

# Lab Humanizer

Skill chuyên dụng để **duyệt, lọc và viết lại tài liệu hướng dẫn bài lab (Lab / Markdown)** dành cho sinh viên và kỹ sư công nghệ.

Mục tiêu tối thượng: Biến văn bản sinh bởi AI hoặc dịch máy thành **tài liệu lab chuẩn mực, sắc sảo, tự nhiên, mang đúng giọng điệu của một Kỹ sư / Giảng viên thực chiến** đứng lớp.

---

## Quy ước định danh chung
- **Thống nhất tên gọi:** Luôn gọi là **"Lab"** hoặc **"Bài lab"** (ví dụ: *Bài lab Ngày 1*, *Lab #1*). 
- **Cấm sử dụng:** Không dùng từ *"Codelab"*, *"bài codelab"*, *"Codelabs"*.

---

## Hai thái cực "Văn AI" cần loại bỏ

Một bài lab viết dở bởi AI thường rơi vào một trong hai thái cực:

### 1. Thái cực "AI Dịch máy thô cứng" (Translationese Slop)
- Dịch word-by-word từ tiếng Anh: *evidence* $\to$ "bằng chứng" (nghe như hình sự), *carries taxonomy* $\to$ "mang taxonomy", *tight box* $\to$ "hộp chặt".
- Dịch giao diện kiểu cũ: "nhấp phải", "nhấp đúp", "tệp tin".
- Hành chính hóa từ ngữ: "thực thi ô mã", "tiến hành triển khai", "đồng nhất trên mọi hệ thống".
- Rò rỉ context/prompt nội bộ của AI (ví dụ: tự ý nhét từ khóa "Antigravity", "assistant").

### 2. Thái cực "AI Chatbot vỗ về, nịnh nọt" (Patronizing Chatbot Slop)
- Giọng điệu ru ngủ, hạ thấp người học: *"Chào mừng bạn đến với buổi học đầu tiên!"*, *"Nếu bạn là người mới (non-tech), đừng lo lắng!"*, *"Cầm tay chỉ việc"*, *"Chúc mừng bạn đã hoàn thành!"*.
- Ví von ngô nghê, kỳ cục: ví AI với "con chó, con mèo", ví taxonomy với "thực đơn món ăn", ví bounding box với "thùng carton", polygon với "áo may đo", gọi AI là "mắt thần", bắt học viên "mở mắt xem kết quả".
- Nhân hóa AI phản khoa học: *"AI đoán bừa"*, *"Độ tự tin của AI"*, gọi Ground Truth là *"thước đo chân lý"*.
- Lạm dụng Emoji tràn lan (`💡`, `📖`, `👉`, `🛡️`, `🖥️`, `📁`, `🛠️`).

---

## 4 Trụ cột Quy tắc cốt lõi (Core Quality Gates)

### Trụ cột 1: Tông giọng Kỹ sư thực chiến (Direct Engineering Tone)
- **Vào thẳng vấn đề:** Bắt đầu bằng mục tiêu kỹ thuật hoặc thao tác đầu tiên. Tuyệt đối không có lời mở đầu sáo rỗng.
- **Dùng từ kỹ thuật tự nhiên của kỹ sư:**
  - Dùng: `chạy ô`, `mở`, `chọn`, `lưu`, `click chuột phải`, `click đúp`, `file`.
  - Cấm: `thực thi`, `tiến hành`, `nhấp phải`, `nhấp đúp`, `tệp`, `đồng nhất`.
- **Chỉ dẫn ngắn gọn, cấm là cấm:** Khi có quy định cấm (như không điền MSSV vào báo cáo), ghi trực tiếp mệnh lệnh. Không thêm văn giáo điều, không lên lớp đạo đức hay giải thích dài dòng về PII trừ khi tài liệu gốc yêu cầu.
- **Tiêu đề tiếng Việt tự nhiên:** Giữ nguyên các đề mục chuẩn như *"Kiểm tra trước khi chạy"*, *"Điều kiện hoàn thành"*, không sính ngoại thành *"Pre-run checklist"*, *"Pre-flight"*.

### Trụ cột 2: Chuẩn hóa Thuật ngữ & Quy tắc Song ngữ lần đầu
- **Không dịch cưỡng ép các từ tiếng Anh chuẩn:** 
  - Giữ nguyên: `bounding box` (hoặc `box`), `checkpoint`, `ground truth`, `prediction`, `pipeline`, `score`, `threshold`, `instance segmentation`, `object detection`, `classification`, `polygon`, `file ZIP`.
  - Tuyệt đối không dịch thành: "hộp giới hạn", "sự thật mặt đất", "tệp nén".
- **Quy tắc Song ngữ lần đầu (First-Mention Rule):**
  - Chỉ mở ngoặc giải thích tiếng Anh ở **lần đầu tiên** thuật ngữ xuất hiện (ví dụ: `danh mục nhãn (taxonomy)` hoặc `phân loại ảnh (image classification)`).
  - Từ lần thứ 2 trở đi: Dùng duy nhất **1 từ nhất quán**, cấm lặp lại ngoặc đơn gây rối mắt.
- **Không nhân hóa AI:**
  - Dùng: "điểm số dự đoán (score)", "mô hình tính toán", "kết quả dự đoán".
  - Cấm: "độ tự tin của AI", "AI đoán bừa", "AI phán đoán".
  - Ground truth là "nhãn chuẩn do con người xác nhận theo quy chuẩn (guideline)", không phải "chân lý".

### Trụ cột 3: Xóa sạch Emoji & Phép so sánh ngô nghê
- Xóa 100% các emoji trang trí ở tiêu đề, danh sách, callout.
- Bỏ toàn bộ các bảng ví von "đời thực" kiểu cấp 1 (con mèo, áo may đo, thực đơn). Thay bằng giải thích bản chất kỹ thuật trực diện hoặc lược bỏ nếu không cần thiết.

### Trụ cột 4: Bảo toàn Dữ kiện & Phiên bản (Strict Fact Preservation)
- Tuyệt đối giữ đúng 100%:
  - Đường link GitHub template, kho mã nguồn.
  - Tag phiên bản phát hành (ví dụ: giữ nguyên `v1.0.1`, không bị tụt lùi về `v1.0.0`).
  - Cấu trúc thư mục nộp bài (`report/`, `day1_lab_outputs/`).
  - Quy ước đặt tên bài tập (`KX-DAY01-HoVaTen-MSSV`).
  - Các tham số dòng lệnh và ô code trong notebook.

---

## Quy trình duyệt & sửa văn bản (Review Workflow)

Khi nhận một file Lab Markdown cần duyệt hoặc viết lại, thực hiện lần lượt 4 bước:

1. **Bước 1: Quét và loại bỏ rác AI (Scan & Strip Slop)**
   - Đổi toàn bộ các từ "Codelab/Codelabs" $\to$ "Lab/Labs".
   - Quét xóa toàn bộ Emoji.
   - Xóa bỏ các đoạn văn mở đầu chào mừng, dỗ dành non-tech, cổ vũ sáo rỗng.
   - Xóa bỏ các phép ví von đời thực khập khiễng, các câu nhân hóa AI ("đoán bừa", "mắt thần").
2. **Bước 2: Thay thế từ vựng theo bảng chuẩn (Vocabulary Normalization)**
   - Tra cứu và thay thế theo `references/vocabulary-rules.md`:
     - "bằng chứng" $\to$ "kết quả bài làm" / "số liệu dẫn chứng".
     - "hộp giới hạn" $\to$ "bounding box".
     - "nhấp phải" $\to$ "click chuột phải".
     - "tệp" $\to$ "file".
     - "thực thi" $\to$ "chạy".
3. **Bước 3: Mài giũa câu từ & Áp dụng First-Mention (Polish & Flow)**
   - Rà soát các thuật ngữ: chỉ để song ngữ Anh - Việt ở lần đầu tiên.
   - Chỉnh các câu văn bị động, dài dòng thành câu ngắn gọn, trực diện, mạch lạc.
4. **Bước 4: Đối soát kỹ thuật (Fact & Checklist Gate)**
   - Rà soát qua 10 điểm trong `references/anti-ai-checklist.md`.
   - Kiểm tra đối chiếu lại URL, tag phiên bản (`v1.0.1`), quy tắc tên repo với file gốc.

---

## Bảng đối chiếu Mẫu (Before vs After)

| Nguyên văn AI dở | Bản sửa chuẩn kỹ sư | Lý do sửa |
| :--- | :--- | :--- |
| `bài codelab số 1` | `bài lab số 1` | Thống nhất tên gọi Lab |
| `nộp bằng chứng qua repository GitHub cá nhân` | `nộp kết quả bài làm qua repository GitHub cá nhân` | Bỏ từ "bằng chứng" sáo rỗng |
| `hộp giới hạn (bbox_xyxy)` | `bounding box (bbox_xyxy)` | Giữ nguyên thuật ngữ chuẩn |
| `nhấp phải ZIP → Extract All...` | `click chuột phải vào file ZIP → Extract All...` | Ngôn ngữ tự nhiên, bỏ "tệp/nhấp" |
| `Nếu bạn là người mới (non-tech), đừng lo lắng!` | *(Xóa bỏ hoàn toàn)* | Bỏ văn dỗ dành, ru ngủ |
| `AI đoán bừa hoặc đoán trúng` | `Mô hình AI dự đoán (Prediction)` | Bỏ nhân hóa cợt nhả |
| `Thực thi ô mã theo thứ tự` | `Chạy các ô theo thứ tự từ trên xuống dưới` | Bỏ từ hành chính "thực thi" |

---

## Tài liệu tham chiếu đi kèm

- `references/vocabulary-rules.md`: Bảng quy chuẩn từ vựng kỹ thuật & từ ngữ giao diện.
- `references/anti-ai-checklist.md`: 10 câu hỏi kiểm tra nhanh trước khi bàn giao lab.
