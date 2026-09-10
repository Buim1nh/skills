# Bảng chuẩn hóa thuật ngữ & Từ ngữ biên tập cho Lab

Bảng quy chuẩn từ vựng dùng để rà soát và thay thế tự động trong các bài lab hướng dẫn tiếng Việt.

---

## 0. Quy ước định danh: Thống nhất gọi là "Lab"

| Cụm từ cấm dùng | Từ chuẩn thống nhất | Ghi chú |
| :--- | :--- | :--- |
| **Codelab / Codelabs** | **Lab / bài lab** | Luôn gọi là: *Bài lab Ngày 1*, *Lab #1*, *tài liệu lab* |
| **bài codelab** | **bài lab** | |
| **hướng dẫn codelab** | **hướng dẫn bài lab** | |

---

## 1. Thuật ngữ kỹ thuật cốt lõi (Core Technical Terms)

### A. Giữ nguyên tiếng Anh (Tuyệt đối không dịch gượng ép)
Các thuật ngữ này đã là ngôn ngữ chuẩn trong ngành kỹ thuật/AI tại Việt Nam. Cố tình dịch ra tiếng Việt làm văn phong trở nên ngô nghê, xa lạ:

| Thuật ngữ | Lỗi dịch thô / Dịch cưỡng ép cần tránh | Ngữ cảnh sử dụng chuẩn |
| :--- | :--- | :--- |
| **instance segmentation** | ❌ phân đoạn cá thể, dán nhãn viền áo | "phân đoạn đối tượng (instance segmentation)" hoặc "phân đoạn thực thể (instance segmentation)" ở lần đầu, sau đó dùng "phân đoạn đối tượng" hoặc "phân đoạn thực thể" |
| **bounding box** (hoặc **box**) | ❌ hộp giới hạn, khung bao, hộp chữ nhật | "tọa độ bounding box", "đối chiếu box với ảnh" |
| **ground truth** | ❌ nhãn sự thật, thước đo chân lý, sự thật mặt đất | "nhãn chuẩn (ground truth)" ở lần đầu, sau đó dùng "ground truth" |
| **prediction** | ❌ lời phán đoán của AI, lời đoán mò | "kết quả dự đoán (prediction)" ở lần đầu, sau đó dùng "prediction" hoặc "kết quả dự đoán" |
| **checkpoint** | ❌ điểm kiểm tra, mốc lưu | "checkpoint của mô hình", "tải checkpoint YOLO11n" |
| **pipeline** | ❌ đường ống dẫn | "quy trình (pipeline)", "pipeline xử lý dữ liệu" |
| **score / confidence** | ❌ độ tự tin của AI | "điểm số dự đoán (score)", "mức độ tin cậy" |
| **threshold** | ❌ ngưỡng cửa | "ngưỡng lọc (threshold)", "hạ threshold", "tăng threshold" |
| **object detection** | ❌ phát hiện vật | "phát hiện vật thể (object detection)" ở lần đầu |
| **image classification** | ❌ phân lớp bức tranh | "phân loại ảnh (image classification)" ở lần đầu |
| **polygon** | ❌ hình đa giác uốn lượn, đa giác mặt nạ | "đa giác (polygon)" ở lần đầu, sau đó dùng "polygon" hoặc "đa giác" |
| **taxonomy** | ❌ thực đơn nhãn | "danh mục nhãn (taxonomy)" ở lần đầu, sau đó dùng "taxonomy" |
| **annotator** | ❌ thợ dán nhãn | "người gán nhãn (annotator)" ở lần đầu, sau đó dùng "annotator" |
| **local** | ❌ cục bộ (khi nói về máy tính/môi trường) | "môi trường Python local", "máy local", "chạy local" (tránh dùng "cục bộ") |
| **file ZIP** | ❌ tệp nén ZIP, gói nén | "file ZIP", ghi rõ phần mở rộng: `KX-DAY01-report.zip` |
| **code cell** | ❌ ô mã thực thi | "ô mã", "ô code" |
---

## 2. Quy tắc Song ngữ lần đầu (First-Mention Rule)

- **Lần đầu tiên xuất hiện:** Viết dạng `Thuật ngữ tiếng Việt (Thuật ngữ tiếng Anh)` hoặc ngược lại nếu từ tiếng Anh phổ biến hơn.
  - *Ví dụ chuẩn:* 
    - `phân loại ảnh (image classification)`
    - `danh mục nhãn (taxonomy)`
    - `kết quả dự đoán (prediction)`
    - `nhãn chuẩn (ground truth)`
- **Từ lần thứ 2 trở đi:** Dùng duy nhất một từ thống nhất, không lặp lại dấu mở đóng ngoặc `(...)`.
  - *Đúng:* "...đọc nhãn chuẩn ground truth. Khi đối chiếu ground truth với..."
  - *Sai (Spam ngoặc):* "...đọc nhãn chuẩn (ground truth). Khi đối chiếu nhãn chuẩn (ground truth) với..."

---

## 3. Thao tác giao diện & Ngôn ngữ máy tính hàng ngày

Tuyệt đối tránh lối dịch máy cổ lỗ sĩ hoặc hành chính hóa:

| Từ máy dịch / Hành chính hóa (TRÁNH) | Từ ngữ kỹ sư tự nhiên (NÊN DÙNG) | Ghi chú |
| :--- | :--- | :--- |
| **nhấp phải / nhấp chuột phải** | **click chuột phải** | Chuẩn ngôn ngữ người dùng |
| **nhấp đúp** | **click đúp** | |
| **tệp / tệp tin** | **file** | "file REPORT.md", "file JSON" |
| **thực thi ô mã / thực thi lệnh** | **chạy ô / chạy lệnh** | Giữ phong cách ngắn gọn của kỹ sư |
| **tiến hành mở / tiến hành tạo** | **mở / tạo** | Bỏ từ rác "tiến hành" |
| **đồng nhất** (trong ngữ cảnh áp dụng) | *(viết trực tiếp hành động)* | Tránh "đồng nhất trên mọi hệ điều hành" |
| **cục bộ** | **local** | "máy local", "môi trường local" (tránh dịch thô "máy cục bộ") |
| **bằng chứng / evidence** | **kết quả bài làm / số liệu dẫn chứng** | Sinh viên làm bài tập, không phải điều tra án |
| **tín hiệu đối soát** | **dùng để đối soát** | Tránh danh từ hóa gượng gạo |
| **trong các artifact** | **trong các file nộp bài** | Dễ hiểu với người học |
| **chạy từ trên xuống dưới** | **chạy các ô theo thứ tự từ trên xuống dưới** | Rõ ràng, tự nhiên |
| **không coi prediction là sự thật** | **không xem prediction là nhãn chuẩn (ground truth)** | Diễn đạt chuẩn khoa học dữ liệu |
| **Không có lệnh cài đặt hệ thống...** | **Toàn bộ thao tác đều chạy online, bạn chưa cần cài đặt Python, thư viện hay script riêng trên máy local.** | Viết lại câu dịch máy rườm rà thành câu kỹ sư tự nhiên |
---

## 4. Danh sách cụm từ "Văn AI Chatbot" cấm sử dụng (Blacklist)

Cắt bỏ hoàn toàn các câu văn mang tính vỗ về, ru ngủ hoặc nhân hóa máy tính:

- ❌ "Chào mừng bạn đến với buổi thực hành..."
- ❌ "Đừng lo lắng!", "Cứ tự tin...", "Không sợ thao tác máy tính..."
- ❌ "Cầm tay chỉ việc – 100% trên trình duyệt"
- ❌ "Chúc mừng bạn! File nộp bài đã được gói gọn gàng..."
- ❌ "Trạm cứu hộ sự cố", "Mở mắt xem kết quả"
- ❌ "AI đoán bừa hoặc đoán trúng", "Độ tự tin của AI", "Mắt thần của AI"
- ❌ Các ví dụ so sánh đời thực ngô nghê: "con mèo / con chó bông", "chiếc áo may đo", "thực đơn món ăn", "thùng carton vuông vức".
- ❌ Mọi loại emoji trang trí (`💡`, `📖`, `👉`, `🛡️`, `🖥️`, `📁`, `🛠️`, v.v.).
