# Bảng chuẩn hóa thuật ngữ & Từ ngữ biên tập cho Lab (Đa lĩnh vực)

Bảng quy chuẩn từ vựng kỹ thuật đa lĩnh vực (Multi-Domain Technical Vocabulary), được thiết kế để mở rộng và tương thích cho mọi bài lab AI/ML/DL, Data Science và Phần mềm.

---

## 0. Định danh theo vai trò tài liệu

| Loại tài liệu | Cách đặt tên chuẩn chức năng | Tránh dùng |
| :--- | :--- | :--- |
| **Đề bài / Bài tập** | **Bài thực hành**, **Lab**, **Bài lab** | ❌ Codelab, bài codelab |
| **Tài liệu giới thiệu (`README.md`)** | **Tên đề tài / Bài thực hành Ngày X** | ❌ Codelab Ngày X |
| **Hướng dẫn chi tiết (`GUIDE.md`)** | **Hướng dẫn thực hành / Cẩm nang** | ❌ Hướng dẫn codelab |
| **Tiêu chí chấm (`RUBRIC.md`)** | **Tiêu chí đánh giá / Rubric** | |
| **Báo cáo học viên (`REPORT.md`)** | **Báo cáo thực hành / Báo cáo bài làm** | |

## 1. Thuật ngữ Môi trường & Thao tác Máy tính (Universal & Platforms)
Áp dụng cho 100% các bài lab thuộc mọi chủ đề:

| Thuật ngữ gốc | Lỗi dịch thô / Hành chính hóa (CẤM) | Từ ngữ chuẩn kỹ sư (DÙNG) | Ngữ cảnh sử dụng |
| :--- | :--- | :--- | :--- |
| **local** | ❌ cục bộ, tại chỗ | **local** | "máy local", "môi trường Python local", "chạy local" |
| **file** | ❌ tệp, tệp tin | **file** | "file JSON", "file PNG", "file README.md" |
| **file ZIP** | ❌ tệp nén ZIP, gói nén | **file ZIP** | Luôn ghi rõ phần mở rộng: `KX-DAYXX-report.zip` |
| **code cell** | ❌ ô mã thực thi | **ô mã**, **ô code** | "chạy ô mã", "ô code bên dưới" |
| **run cell** | ❌ thực thi ô mã, tiến hành chạy | **chạy ô** | "chạy các ô theo thứ tự từ trên xuống dưới" |
| **right click** | ❌ nhấp phải, nhấp chuột phải | **click chuột phải** | "click chuột phải vào file ZIP" |
| **double click**| ❌ nhấp đúp | **click đúp** | "click đúp vào file để mở" |
| **evidence** | ❌ bằng chứng | **kết quả bài làm**, **số liệu dẫn chứng** | Sinh viên làm bài tập, không phải điều tra án |
| **open / create**| ❌ tiến hành mở, tiến hành tạo | **mở / tạo** | Bỏ từ rác hành chính "tiến hành" |
| **identical** | ❌ đồng nhất trên mọi HĐH | *(viết trực tiếp thao tác)* | "áp dụng giống nhau trên Windows, macOS và Ubuntu" |
| **cross-check** | ❌ tín hiệu đối soát | **dùng để đối soát** | Tránh danh từ hóa gượng gạo |
| **artifacts** | ❌ các artifact | **các file nộp bài**, **kết quả đầu ra** | Dễ hiểu với người học |

---

## 2. Thuật ngữ Học máy & Khoa học Dữ liệu chung (Core Machine Learning)

| Thuật ngữ | Lỗi dịch thô / Nhân hóa AI (CẤM) | Từ ngữ chuẩn kỹ sư (DÙNG) |
| :--- | :--- | :--- |
| **ground truth** | ❌ nhãn sự thật, thước đo chân lý, sự thật mặt đất | **nhãn chuẩn (ground truth)** ở lần đầu, sau đó dùng **ground truth** |
| **prediction** | ❌ lời phán đoán của AI, AI đoán mò | **kết quả dự đoán (prediction)** ở lần đầu, sau đó dùng **prediction** |
| **checkpoint** | ❌ điểm kiểm tra, mốc lưu | **checkpoint** ("checkpoint của mô hình", "tải checkpoint") |
| **pipeline** | ❌ đường ống dẫn | **quy trình (pipeline)** ở lần đầu, sau đó dùng **pipeline** |
| **score / confidence** | ❌ độ tự tin của AI, mức tin tưởng | **điểm số dự đoán (score)**, **mức độ tin cậy** (không nhân hóa AI) |
| **threshold** | ❌ ngưỡng cửa | **ngưỡng lọc (threshold)**, "hạ threshold", "tăng threshold" |
| **taxonomy** | ❌ thực đơn nhãn, bảng món ăn | **danh mục nhãn (taxonomy)** ở lần đầu, sau đó dùng **taxonomy** |
| **annotator** | ❌ thợ dán nhãn | **người gán nhãn (annotator)** ở lần đầu, sau đó dùng **annotator** |
| **data leakage** | ❌ rò rỉ dữ liệu (dễ nhầm với security) | **rò rỉ dữ liệu huấn luyện (data leakage)** |
| **overfitting** | ❌ quá khớp, học vẹt | **hiện tượng quá khớp (overfitting)** ở lần đầu, sau đó dùng **overfitting** |
| **underfitting** | ❌ chưa khớp | **chưa khớp (underfitting)** |
| **baseline** | ❌ đường cơ sở | **mô hình cơ sở (baseline)** |
| **metric** | ❌ số liệu đo | **chỉ số đánh giá (metric)** |
| **train/val/test split** | ❌ phân chia tàu xe | **chia tập train / validation / test** |
| **epoch / batch size** | ❌ kỷ nguyên / kích thước lô | **epoch** / **batch size** (giữ nguyên tiếng Anh) |
| **learning rate** | ❌ tốc độ học tập của AI | **tốc độ học (learning rate)** |

---

## 3. Thuật ngữ Chuyên ngành Thị giác Máy tính (Computer Vision Domain)

| Thuật ngữ | Lỗi dịch thô (CẤM) | Từ ngữ chuẩn kỹ sư (DÙNG) |
| :--- | :--- | :--- |
| **instance segmentation** | ❌ phân đoạn cá thể, dán nhãn viền áo | **phân đoạn đối tượng (instance segmentation)** hoặc **phân đoạn thực thể** |
| **semantic segmentation** | ❌ phân đoạn ngữ nghĩa từng điểm | **phân đoạn ngữ nghĩa (semantic segmentation)** |
| **object detection** | ❌ phát hiện đồ vật | **phát hiện vật thể (object detection)** ở lần đầu |
| **image classification** | ❌ phân lớp tranh ảnh | **phân loại ảnh (image classification)** ở lần đầu |
| **bounding box** (hoặc **box**) | ❌ hộp giới hạn, khung bao, thùng carton | **bounding box** hoặc **box** (tuyệt đối không dịch thành hộp giới hạn) |
| **polygon** | ❌ hình đa giác uốn lượn, đa giác mặt nạ | **đa giác (polygon)** ở lần đầu, sau đó dùng **polygon** |
| **mask** | ❌ mặt nạ che mặt | **mặt nạ phân đoạn (mask)** ở lần đầu, sau đó dùng **mask** |
| **IoU (Intersection over Union)** | ❌ giao trên hợp | **chỉ số IoU (Intersection over Union)** |
| **tight bounding box** | ❌ hộp chặt | **quy tắc đóng bounding box bám sát vật thể** |
| **occlusion** | ❌ sự bế tắc | **vật thể bị che khuất (occlusion)** |
| **truncation** | ❌ sự cắt ngắn | **vật thể bị cắt mép ảnh (truncation)** |

---

## 4. Thuật ngữ Xử lý Ngôn ngữ Tự nhiên & LLM (NLP / GenAI Domain)
Sẵn sàng mở rộng cho các bài lab xử lý văn bản, RAG và LLM sau này:

| Thuật ngữ | Lỗi dịch thô (CẤM) | Từ ngữ chuẩn kỹ sư (DÙNG) |
| :--- | :--- | :--- |
| **prompt** | ❌ lời nhắc nhở, câu xúi giục | **câu lệnh (prompt)** ở lần đầu, sau đó dùng **prompt** |
| **token / tokenization** | ❌ đồng xu, mã thông báo | **token** / **tách token (tokenization)** |
| **context window** | ❌ cửa sổ ngữ cảnh | **độ dài ngữ cảnh (context window)** |
| **embeddings** | ❌ phép nhúng vào | **vector đặc trưng (embeddings)** |
| **fine-tuning** | ❌ tinh chỉnh nhẹ nhàng | **tinh chỉnh mô hình (fine-tuning)** |
| **RAG (Retrieval-Augmented Generation)** | ❌ thế hệ tăng cường thu hồi | **kỹ thuật RAG (Retrieval-Augmented Generation)** |
| **hallucination** | ❌ ảo giác điên rồ | **hiện tượng ảo giác / sinh thông tin sai (hallucination)** |
| **benchmark** | ❌ mốc chuẩn điểm chuẩn | **bộ tiêu chuẩn đánh giá (benchmark)** |

---

## 5. Quy tắc Song ngữ lần đầu (First-Mention Rule)
- **Lần đầu tiên xuất hiện trong file:** Viết dạng `Thuật ngữ tiếng Việt (Thuật ngữ tiếng Anh)`.
  - *Ví dụ:* `phân loại ảnh (image classification)`, `phân đoạn đối tượng (instance segmentation)`, `danh mục nhãn (taxonomy)`.
- **Từ lần thứ 2 trở đi trong file đó:** Dùng duy nhất **1 từ nhất quán** (ưu tiên thuật ngữ kỹ thuật ngắn gọn, tự nhiên), tuyệt đối không lặp lại dấu mở đóng ngoặc đơn.

---

## 6. Danh sách đen các câu văn "Văn AI Chatbot" (Absolute Blacklist)
Cắt bỏ 100% trong mọi bài lab:
- ❌ Lời chào & dỗ dành: *"Chào mừng bạn..."*, *"Nếu bạn là người mới (non-tech), đừng lo lắng!"*, *"Cầm tay chỉ việc"*, *"Chúc mừng bạn đã hoàn thành!"*, *"Cứ tự tin..."*.
- ❌ Ví von đời thực khập khiễng: con chó/mèo, thùng carton, áo may đo, thực đơn món ăn, "mắt thần AI", lệnh *"Mở mắt xem kết quả"*.
- ❌ Nhân hóa AI phản khoa học: *"AI đoán bừa"*, *"Độ tự tin của AI"*, *"thước đo chân lý"*.
- ❌ Tất cả các loại Emoji trang trí (`💡`, `📖`, `👉`, `🛡️`, `🖥️`, `📁`, `🛠️`...).
