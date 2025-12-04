# ĐỀ TÀI: Khai phá dữ liệu tuyển dụng LinkedIn – Phân cụm nghề nghiệp, khai phá luật kỹ năng và dự đoán mức lương

## CHƯƠNG 1 – GIỚI THIỆU

### 1.1. Bối cảnh
- Thị trường lao động toàn cầu biến đổi mạnh mẽ với sự dịch chuyển kỹ năng.
- LinkedIn cung cấp dữ liệu tuyển dụng quy mô lớn, cập nhật theo thời gian thực.
- Khai phá dữ liệu (Data Mining) cho phép phát hiện mẫu ẩn trong tuyển dụng.

### 1.2. Lý do chọn đề tài
- Dataset LinkedIn Job Postings có cấu trúc tốt, gồm nhiều file liên quan.
- Phù hợp triển khai nhiều kỹ thuật Data Mining: Clustering, Association Rules, Pattern Mining.
- Mang lại insight hữu ích về thị trường nhân lực.

### 1.3. Mục tiêu nghiên cứu
1. Phân cụm các nhóm nghề nghiệp dựa trên mô tả và kỹ năng.
2. Khai phá các bộ kỹ năng thường xuất hiện cùng nhau (skill bundles).
3. Khai phá yếu tố ảnh hưởng đến mức lương và xây dựng mô hình dự đoán lương.

### 1.4. Câu hỏi nghiên cứu
- RQ1: Các nhóm nghề nghiệp được hình thành như thế nào dựa trên mô tả công việc và kỹ năng?
- RQ2: Những kỹ năng nào thường kết hợp với nhau, và tồn tại các “skill bundles” theo nhóm nghề nghiệp?
- RQ3: Các yếu tố nào ảnh hưởng đến lương, và có thể dự đoán mức lương từ mô tả, kỹ năng, kinh nghiệm và thông tin công ty hay không?

### 1.5. Đối tượng & phạm vi nghiên cứu

### 1.6. Phương pháp tiếp cận

---

## CHƯƠNG 2 – CƠ SỞ LÝ THUYẾT

### 2.1. Tổng quan Data Mining
- Khái niệm, vai trò, quy trình CRISP-DM.
- Phân biệt supervised vs unsupervised vs pattern mining.

### 2.2. Tiền xử lý dữ liệu
- Làm sạch dữ liệu.
- Chuẩn hóa text: tokenization, stopwords, lemmatization.
- Biến đổi dữ liệu phân loại.

### 2.3. Vector hóa văn bản
- TF-IDF.
- Word/Skill embedding.

### 2.4. Phân cụm (Clustering)
- K-means.
- Hierarchical clustering.
- Đánh giá bằng silhouette score.

### 2.5. Khai phá luật kết hợp (Association Rules)
- Apriori.
- FP-Growth.
- Support – Confidence – Lift.

### 2.6. Khai phá mẫu lương (Pattern Mining + Regression)
- Discretization salary bins.
- Luật liên quan skill → salary.
- Regression models để bổ sung dự đoán.

---

## CHƯƠNG 3 – DỮ LIỆU & PHƯƠNG PHÁP

### 3.1. Giới thiệu dataset
- job_postings.csv: lương, kỹ năng, mô tả, kinh nghiệm, location.
- companies.csv: quy mô, địa chỉ, follower_count.
- benefits, employee_counts, job_details.

### 3.2. Tích hợp dữ liệu
- Join theo job_id và company_id.
- Tạo bảng cuối phục vụ khai phá.

### 3.3. Tiền xử lý
- Xử lý missing.
- Chuẩn hóa text và kỹ năng.
- Encode categorical features.

### 3.4. EDA
- Phân bố nghề nghiệp, lương, kỹ năng.
- Heatmap tương quan.
- Biểu đồ tần suất kỹ năng.

### 3.5. Phương pháp khai phá

#### 3.5.1. RQ1 – Phân cụm nghề nghiệp
- TF-IDF mô tả + kỹ năng.
- K-means / H-Clustering.
- PCA/t-SNE visualization.
- Phân tích đặc trưng từng cluster.

#### 3.5.2. RQ2 – Khai phá kỹ năng
- Tách kỹ năng thành transaction list.
- Apriori / FP-Growth → frequent skillsets.
- Network analysis → centrality, community detection.

#### 3.5.3. RQ3 – Khai phá lương & dự đoán
- Discretization salary (low/medium/high).
- Association between skill bundles & salary bins.
- Regression: RF/XGBoost.
- SHAP feature importance.

---

## CHƯƠNG 4 – THỰC NGHIỆM & KẾT QUẢ

### 4.1. Thiết lập môi trường
- Python, Pandas, Sklearn, MLxtend, NetworkX.

### 4.2. Kết quả phân cụm
- Silhouette score.
- Visualization.
- Giải thích cluster.

### 4.3. Kết quả luật kết hợp
- Bảng luật mạnh nhất.
- Biểu đồ mạng kỹ năng.
- Nhận xét skill bundles.

### 4.4. Kết quả khai phá lương & dự đoán
- Patterns liên quan skill → salary.
- Performance của mô hình dự đoán lương.
- SHAP phân tích yếu tố ảnh hưởng.

---

## CHƯƠNG 5 – KẾT LUẬN

### 5.1. Kết luận chính
- Các nhóm nghề nghiệp rõ ràng theo skill & description.
- Skill bundles theo ngành nghề.
- Các yếu tố ảnh hưởng mạnh đến lương.

### 5.2. Hạn chế
- Mô tả không chuẩn hóa.
- Một số thiếu dữ liệu lương.

### 5.3. Hướng phát triển
- Dùng embedding nâng cao (BERT).
- Phân tích từng quốc gia.
