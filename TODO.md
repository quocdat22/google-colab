# TODO: Xây dựng hệ thống huấn luyện phân loại biển báo giao thông

## 1. Thu thập và chuẩn bị dữ liệu
- [x] Tìm và tải bộ dữ liệu biển báo giao thông (ví dụ: GTSRB)
- [x] Phân tích cấu trúc dữ liệu (số lượng lớp, định dạng ảnh, nhãn, ...)
- [x] Khám phá dữ liệu (thống kê số lượng ảnh, hiển thị ảnh mẫu, kiểm tra kích thước, ...)
- [x] Tiền xử lý dữ liệu:
  - [x] Resize ảnh về cùng kích thước (ví dụ: 32x32 hoặc 64x64)
  - [x] Chuẩn hóa giá trị pixel (0-1 hoặc -1 đến 1)
  - [x] Chia dữ liệu thành tập train, validation, test
  - [ ] (Tùy chọn) Thực hiện data augmentation (xoay, lật, thay đổi độ sáng, ...)

## 2. Xây dựng mô hình phân loại
- [ ] Chọn framework (TensorFlow/Keras)
- [ ] Thiết kế mô hình CNN cơ bản hoặc sử dụng transfer learning:
  - [ ] Xây dựng mô hình CNN từ đầu (LeNet, AlexNet, ...)
  - [ ] Hoặc sử dụng mô hình pretrained (ResNet, MobileNet, ...)
- [ ] Định nghĩa hàm mất mát (loss function) và optimizer
- [ ] Thiết lập các tham số huấn luyện (batch size, epochs, learning rate, ...)

## 3. Huấn luyện mô hình
- [ ] Viết script huấn luyện mô hình với dữ liệu đã chuẩn bị
- [ ] Theo dõi quá trình huấn luyện (loss, accuracy trên train/validation)
- [ ] Lưu lại mô hình tốt nhất (checkpoint)

## 4. Đánh giá và tinh chỉnh mô hình
- [ ] Đánh giá mô hình trên tập test (accuracy, confusion matrix, ...)
- [ ] Phân tích các trường hợp dự đoán sai
- [ ] Tinh chỉnh hyperparameters hoặc kiến trúc mô hình nếu cần
- [ ] Áp dụng thêm các kỹ thuật regularization (dropout, batch normalization, ...)

## 5. Triển khai mô hình
- [ ] Lưu mô hình đã huấn luyện (dạng .h5, .pt, .onnx, ...)
- [ ] Xây dựng script hoặc API để nhận diện biển báo từ ảnh mới
- [ ] (Tùy chọn) Tích hợp vào ứng dụng thực tế (web, mobile, ...)

---

**Ghi chú:**
- Mỗi bước nên có file notebook hoặc script riêng biệt để dễ kiểm soát và tái sử dụng.
- Ghi chú lại các vấn đề gặp phải và cách giải quyết trong quá trình thực hiện. 