# Customer Churn Prediction & Model Deployment Pipeline

## Project Overview
Dự án xây dựng mô hình học máy (Machine Learning) để dự báo xác suất khách hàng rời bỏ dịch vụ (Churn). Mục tiêu là xác định sớm các khách hàng có rủi ro cao để bộ phận vận hành có các chiến dịch giữ chân (retention) kịp thời. Dự án bao gồm toàn bộ quy trình từ xử lý dữ liệu, tối ưu hóa mô hình đến đóng gói Pipeline để triển khai thực tế.

## Key Features & Methodology

### 1. End-to-End ML Pipeline
- **Data Preprocessing**: Xử lý dữ liệu thiếu, mã hóa biến phân loại (OHE) và chuẩn hóa dữ liệu.
- **Feature Engineering**: Sử dụng PySpark xử lý log-transform và VectorAssembler để tối ưu hóa đặc trưng đầu vào.
- **Model Selection**: Thử nghiệm và so sánh nhiều thuật toán như **Random Forest, Logistic Regression, XGBoost**.

### 2. Model Optimization & Validation
- **Threshold Tuning**: Thay vì sử dụng ngưỡng mặc định (0.5), dự án thực hiện tìm kiếm **Optimal Threshold** để cân bằng giữa Precision và Recall, tối ưu hóa lợi ích kinh tế cho doanh nghiệp.
- **Evaluation Metrics**: Đánh giá mô hình dựa trên ROC-AUC, F1-Score và Precision-Recall curve.

### 3. Production Readiness (Deployment)
- **Model Serialization**: Sử dụng `joblib` để đóng gói toàn bộ Pipeline (bao gồm cả các bước xử lý dữ liệu và mô hình đã fit) thành file `.pkl`.
- **Inference Ready**: Cung cấp hướng dẫn chi tiết về cách load model và áp dụng ngưỡng threshold đã chọn để thực hiện dự báo trên dữ liệu mới.

## Technical Stack
- **Languages**: Python, PySpark
- **Libraries**: 
    - *Modeling:* `scikit-learn`, `joblib`, `xgboost`, `numpy`, `pandas`
    - *Environment:* Google Colab / Jupyter Notebook

## Business Impact
- Tự động hóa việc phân loại khách hàng rủi ro theo thang điểm xác suất.
- Giúp tối ưu hóa chi phí Marketing bằng cách tập trung nguồn lực vào nhóm khách hàng thực sự có khả năng rời bỏ.

---
