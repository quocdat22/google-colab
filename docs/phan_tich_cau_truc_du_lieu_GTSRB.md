# Phân tích cấu trúc dữ liệu GTSRB (German Traffic Sign Recognition Benchmark)

## 1. Số lượng lớp (số lượng nhãn)
- GTSRB có **43 lớp** (class), mỗi lớp tương ứng với một loại biển báo giao thông khác nhau.
- Mỗi lớp được đánh số từ 0 đến 42.

## 2. Định dạng ảnh
- Ảnh gốc có định dạng **PPM** (Portable Pixmap Format).
- Kích thước ảnh không đồng nhất, thường dao động từ 15x15 đến 250x250 pixels.
- Ảnh là ảnh màu (RGB).

## 3. Cấu trúc thư mục
- Dữ liệu huấn luyện nằm trong: `data/GTSRB/Final_Training/Images/`
  - Mỗi thư mục con (ví dụ: `00000`, `00001`, ..., `00042`) là một lớp, chứa các ảnh thuộc lớp đó.
- Dữ liệu kiểm tra nằm trong: `data/GTSRB/Final_Test/Images/`
  - Tất cả ảnh test nằm chung một thư mục.
- Thường đi kèm file CSV chứa thông tin nhãn, bounding box, v.v.

## 4. Thông tin nhãn
- Với tập train, nhãn được xác định qua tên thư mục chứa ảnh.
- Với tập test, nhãn thực tế thường nằm trong file CSV (ví dụ: `GT-final_test.csv`).

## 5. Số lượng ảnh
- Tổng số ảnh train: khoảng 39.000 ảnh.
- Tổng số ảnh test: khoảng 12.600 ảnh.

## 6. Một số lưu ý khác
- Ảnh có thể cần resize về cùng kích thước (thường dùng 32x32 hoặc 48x48).
- Nên chuẩn hóa giá trị pixel về [0, 1] hoặc [-1, 1] khi huấn luyện.

---

**Checklist thực hiện:**
- [x] Xác định số lượng lớp: 43
- [x] Xác định định dạng ảnh: PPM, RGB, kích thước không đồng nhất
- [x] Xác định cấu trúc thư mục: mỗi lớp là một thư mục con, test chung một thư mục
- [x] Xác định cách lấy nhãn: tên thư mục (train), file CSV (test)
- [x] Thống kê số lượng ảnh train/test 