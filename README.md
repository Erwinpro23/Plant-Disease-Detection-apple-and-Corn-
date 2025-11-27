
# Plant Disease Detection (Apple and Corn)

Dự án này sử dụng học máy để phát hiện bệnh trên cây táo và ngô dựa trên hình ảnh của lá cây. Mô hình học sâu (deep learning) được huấn luyện với các loại bệnh phổ biến trên táo và ngô, sau đó ứng dụng vào một ứng dụng web để nhận dạng bệnh qua ảnh.

## Mô tả

Dự án này bao gồm một ứng dụng Flask đơn giản với các chức năng sau:

- Nhận ảnh của cây táo hoặc ngô từ người dùng.
- Dự đoán bệnh cây dựa trên ảnh.
- Cung cấp kết quả dự đoán cùng với độ tin cậy của mô hình.

Ứng dụng sử dụng một mô hình học sâu (deep learning) được huấn luyện sẵn, có thể nhận dạng các bệnh sau:

- **Táo**: Apple Scab, Healthy
- **Ngô**: Common Rust, Healthy

## Cài đặt

Để cài đặt và chạy ứng dụng này trên máy của bạn, làm theo các bước sau:

### Bước 1: Clone repository

```bash
git clone https://github.com/Erwinpro23/Plant-Disease-Detection-apple-and-Corn-
cd Plant-Disease-Detection-apple-and-Corn-
```

### Bước 2: Cài đặt các thư viện yêu cầu

Cài đặt các thư viện cần thiết từ file `requirements.txt`:

```bash
pip install -r requirements.txt
```

Nếu file `requirements.txt` chưa có, bạn có thể cài đặt các thư viện cần thiết thủ công:

```bash
pip install Flask tensorflow pillow opencv-python
```

### Bước 3: Đảm bảo rằng bạn có mô hình

Dự án này yêu cầu mô hình học máy được lưu trong file `best_b6_model.h5`. Bạn cần tải mô hình này từ nguồn đã cho hoặc huấn luyện mô hình của riêng bạn.

### Bước 4: Chạy ứng dụng Flask

```bash
python app.py
```

Ứng dụng sẽ chạy trên `http://localhost:5000/`.

## Cách sử dụng

1. Truy cập ứng dụng web tại `http://localhost:5000/`.
2. Tải lên một hình ảnh của lá cây táo hoặc ngô.
3. Ứng dụng sẽ trả về dự đoán bệnh cùng với độ tin cậy.

### Dự đoán

- **prediction**: Tên bệnh hoặc trạng thái của cây (ví dụ: "Apple__Apple_scab", "Corn__healthy").
- **confidence**: Độ tin cậy của dự đoán (ví dụ: 0.85).
- **all_predictions**: Dự đoán cho tất cả các lớp (bệnh và trạng thái cây).

## Cấu trúc thư mục

```
Plant-Disease-Detection-apple-and-Corn/
│
├── app.py                # File ứng dụng Flask
├── Model.ipynb           # Jupyter Notebook để huấn luyện mô hình
├── templates/            # Thư mục chứa file HTML (index.html)
│   └── index.html        # Template chính của ứng dụng
├── best_b6_model.h5      # Mô hình học máy
└── requirements.txt      # Các thư viện yêu cầu
```

## Lưu ý

- Nếu không có mô hình, ứng dụng sẽ trả về dự đoán ngẫu nhiên.
- Đảm bảo rằng mô hình `best_b6_model.h5` được đặt đúng vị trí trong thư mục gốc của dự án.
