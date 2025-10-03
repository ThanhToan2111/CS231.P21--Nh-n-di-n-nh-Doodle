# Dự án Nhận Diện Hình Doodle  
*(CS231.P21 – Doodle Recognition)*

<p align="center">
  <img src="docs/cover.png" alt="Doodle Example" width="400"/>
</p>

## 1. Tổng quan  
Dự án này thực hiện bài toán **nhận diện hình vẽ nguệch ngoạc (Doodle / sketch)** từ bộ dữ liệu vẽ tay, sử dụng các kỹ thuật học máy / học sâu để phân loại hình vẽ vào các lớp tương ứng.  
Mục tiêu là xây dựng một mô hình có độ chính xác cao, có khả năng xử lý các hình vẽ đơn giản, có thể áp dụng trong ứng dụng vẽ / trò chơi / nhận biết bản vẽ.

---

## 2. Tính năng chính  
- Tiền xử lý dữ liệu: chuẩn hóa, augment dữ liệu (xoay, lật, biến đổi)  
- Xây dựng mô hình deep learning (CNN / mạng nơ-ron tích chập)  
- Huấn luyện và đánh giá mô hình  
- Giao diện demo (notebook / web) để người dùng thử vẽ và nhận diện  
- Trực quan hóa kết quả: ma trận nhầm lẫn, biểu đồ accuracy / loss  

---

---

## 3. Hướng dẫn sử dụng

### 3.1. Cài đặt môi trường  
Bạn có thể dùng `venv` hoặc `conda`:

```bash
# tạo và kích hoạt môi trường (ví dụ với venv)
python3 -m venv venv
source venv/bin/activate    # Linux / macOS
.\venv\Scripts\activate     # Windows

# cài các thư viện cần thiết
pip install -r requirements.txt

# huấn luyện
python src/train.py --config configs/train_config.yaml

# đánh giá mô hình
python src/evaluate.py --model_path models/best_model.pth

