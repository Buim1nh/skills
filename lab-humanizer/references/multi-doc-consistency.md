# Quy chuẩn Đồng bộ Đa tài liệu trong Bài Lab (Multi-Document Consistency)

Trong một bài lab chuẩn, nội dung thường được phân bổ trên nhiều file tài liệu:
1. `README.md`: Giới thiệu tổng quan, phạm vi, yêu cầu trước khi bắt đầu và luồng 7 bước tóm tắt.
2. `GUIDE.md` (hoặc `LAB.md`): Hướng dẫn chi tiết từng thao tác, cách đọc dữ liệu, phân tích kết quả và xử lý lỗi sâu.
3. `RUBRIC.md`: Tiêu chí đánh giá chất lượng bài làm và định hướng tự chấm điểm.
4. `reports/REPORT_TEMPLATE.md`: Mẫu báo cáo cá nhân / nhóm để học viên điền số liệu.

Để đảm bảo **tính tương thích và mở rộng cho mọi bài lab trong tương lai**, bộ kỹ năng `lab-humanizer` bắt buộc phải áp dụng quy tắc **Đồng bộ Đa tài liệu (Cross-Document Consistency)** theo các nguyên tắc dưới đây:

---

## 1. Nguyên tắc "Chân lý Đơn nhất" (Single Source of Truth)

Khi duyệt và biên tập, các thông số kỹ thuật sau đây phải **khớp chính xác 100% giữa mọi file trong repo**:

| Thông số kỹ thuật | Yêu cầu đối soát giữa các file |
| :--- | :--- |
| **Phiên bản phát hành (Release Tag)** | Ví dụ: Nếu `README.md` ghi `v1.0.1` thì link Colab trong `GUIDE.md` và `notebooks/` cũng phải là `v1.0.1`. Tuyệt đối không để file này `v1.0.0`, file kia `v1.0.1`. |
| **Quy tắc đặt tên Repository** | `KX-DAYXX-HoVaTen-MSSV` (cho bài cá nhân) hoặc `KX-DAYXX-TenNhom` (cho bài làm nhóm). Cú pháp này phải giống nhau trên `README`, `GUIDE` và `RUBRIC`. |
| **Quy tắc đặt tên file nộp bài** | Ví dụ: `KX-DAYXX-report.zip` (phải đồng nhất đuôi mở rộng `.zip`, chữ hoa chữ thường). |
| **Cấu trúc thư mục nhận bài** | Thư mục nộp bài luôn là `report/`. Cấu trúc bên trong `report/` (ví dụ: `REPORT.md`, thư mục `outputs/`, file attribution) phải được mô tả giống hệt nhau ở cả `README.md` và `GUIDE.md`. |
| **Tên biến mã khóa học** | Nếu notebook quy định biến `KHOA = "K4"` thì mọi tài liệu hướng dẫn đều phải dùng chữ `KHOA` (không lúc thì `KHOA`, lúc thì `MA_LOP`, `COURSE_ID`). |

---

## 2. Thống nhất Thuật ngữ xuyên suốt (Global Terminology Lock)

- Một thuật ngữ khi đã chọn thì **phải dùng thống nhất trên toàn bộ các file của bài lab**:
  - Đã dùng **"phân đoạn đối tượng (instance segmentation)"** thì không được ở `README` viết "phân đoạn đối tượng", sang `GUIDE` lại đổi thành "phân đoạn cá thể", sang `RUBRIC` lại viết "phân đoạn thực thể".
  - Đã dùng **"bounding box"** thì không được ở file này viết "bounding box", file khác viết "hộp chữ nhật", file khác nữa viết "hộp giới hạn".
  - Đã dùng **"nhãn chuẩn (ground truth)"** thì không được ở file báo cáo dùng "sự thật" hay "ground truth chưa kiểm chứng".
  - Đã thống nhất gọi là **"Lab"** thì cấm xuất hiện chữ "Codelab" ở bất kỳ file nào (`README`, `GUIDE`, `REPORT`, `RUBRIC`, `notebook`).

---

## 3. Quy tắc Song ngữ giữa các tầng tài liệu

- **Quy tắc First-Mention theo cấp độ file:** 
  - Mỗi file tài liệu (`README.md`, `GUIDE.md`) là một điểm vào (entry point) độc lập của người đọc.
  - Do đó, ở mỗi file, thuật ngữ kỹ thuật chính cần được ghi chú song ngữ Anh - Việt ở **lần đầu tiên xuất hiện trong file đó** (ví dụ: `phân loại ảnh (image classification)`).
  - Từ lần thứ 2 trở đi trong file đó: Dùng duy nhất 1 từ thống nhất.
  - Riêng trong bảng biểu tóm tắt hoặc mẫu báo cáo `REPORT_TEMPLATE.md`: Ưu tiên dùng thuật ngữ chuẩn gãy gọn (như `bounding box`, `score`, `taxonomy`) để tiết kiệm diện tích và tránh rườm rà.

---

## 4. Hỗ trợ 2 Chế độ làm việc (Work Modes)

Để mở rộng cho các bài lab sau này, quy trình phải hỗ trợ linh hoạt 2 chế độ:

### Chế độ Cá nhân (`individual`)
- Tên repo: `KX-DAYXX-HoVaTen-MSSV`
- Quy tắc ẩn danh: Không ghi họ tên, MSSV, SĐT, email vào trong nội dung file báo cáo `REPORT.md` (chỉ để ở tên repo để phục vụ chấm ẩn danh/PII).

### Chế độ Nhóm (`team`)
- Tên repo: `KX-DAYXX-TenNhom`
- Bắt buộc có file `TEAMMATES.md` ở thư mục gốc liệt kê đầy đủ danh sách thành viên (Họ tên, MSSV, Vai trò đóng góp).
- Báo cáo nhóm ghi nhận kết quả chung của cả nhóm.

---

## 5. Quy trình Kiểm tra Đồng bộ trước khi Release

Trước khi chốt một bài lab:
1. `git diff` toàn bộ repo để kiểm tra các từ khóa nhạy cảm (`Codelab`, `cục bộ`, `bằng chứng`, `tệp`, `nhấp phải`, `Antigravity`).
2. Chạy lệnh grep kiểm tra sự nhất quán của các đường link release tag:
   ```bash
   grep -rn "v1.0." .
   ```
3. Kiểm tra xem cây thư mục mô tả trong `README.md` có khớp từng ký tự với cây thư mục trong `GUIDE.md` và mã nguồn notebook không.
