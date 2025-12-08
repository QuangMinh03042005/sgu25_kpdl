# ĐỀ TÀI: Khai phá dữ liệu tuyển dụng LinkedIn – Phân cụm nghề nghiệp, khai phá luật kỹ năng và dự đoán mức lương

## CHƯƠNG 1 – GIỚI THIỆU

### 1.1. Bối cảnh
Trình bày sự thay đổi của thị trường lao động, vai trò của dữ liệu tuyển dụng trực tuyến, đặc biệt là LinkedIn. Nhấn mạnh tầm quan trọng của khai phá dữ liệu trong việc hiểu xu hướng nghề nghiệp và kỹ năng.

### 1.2. Lý do chọn đề tài
- Dataset LinkedIn Job Postings có quy mô lớn, đa dạng.
- Phù hợp áp dụng đầy đủ các kỹ thuật khai phá dữ liệu.
- Có tính thực tiễn cao khi phân tích thị trường lao động.
- Có thể kết hợp với ontology ESCO để chuẩn hóa kỹ năng.

### 1.3. Mục tiêu nghiên cứu
1. Phân cụm nhóm nghề nghiệp dựa trên mô tả công việc.
2. Khai phá skill bundles bằng ESCO ontology và network analysis.
3. Dự đoán mức lương dựa trên thông tin mô tả, kinh nghiệm, công ty và các đặc trưng khác.

### 1.4. Câu hỏi nghiên cứu
- **RQ1:** Các nhóm nghề nghiệp được hình thành như thế nào dựa trên mô tả công việc?
- **RQ2:** Những nhóm kỹ năng nào thường xuất hiện cùng nhau? Có tồn tại các skill bundles theo ngành nghề không?
- **RQ3:** Các yếu tố nào ảnh hưởng đến mức lương? Có thể dự đoán lương từ mô tả, kỹ năng, kinh nghiệm và thông tin công ty hay không?

### 1.5. Đối tượng & phạm vi nghiên cứu
- Dữ liệu tuyển dụng dạng tiếng Anh từ LinkedIn.
- Chỉ sử dụng các job có thông tin mô tả.
- Chỉ dùng các job có `med_salary` để dự đoán lương.
- Kỹ năng được trích xuất từ mô tả bằng ESCO ontology thay vì trường `skills_desc`.

### 1.6. Phương pháp tiếp cận
- Tuân theo quy trình CRISP-DM.
- Áp dụng kết hợp supervised learning, unsupervised learning và network mining.

---

## CHƯƠNG 2 – CƠ SỞ LÝ THUYẾT

### 2.1. Tổng quan Data Mining
Khái niệm, vai trò, CRISP-DM, supervised/unsupervised/pattern mining.

### 2.2. Tiền xử lý dữ liệu
Làm sạch văn bản, chuẩn hóa text, xử lý missing values, encode categorical.

### 2.3. Vector hóa văn bản
TF-IDF, embedding ứng dụng trong phân cụm.

### 2.4. Phân cụm (Clustering)
K-means, hierarchical clustering, silhouette score.

### 2.5. Khai phá kỹ năng (Skill Mining)
ESCO ontology, co-occurrence analysis, community detection.

### 2.6. Dự đoán lương
Linear Regression, Random Forest, đánh giá RMSE, phân tích feature importance.

---

## CHƯƠNG 3 – DỮ LIỆU & PHƯƠNG PHÁP

### 3.1. Tổng quan dataset
Giới thiệu các file, đặc thù dữ liệu LinkedIn (missing salary cao, skill_desc không chuẩn hóa).

### 3.2. Tích hợp dữ liệu
Merge job–company–employee_counts, xử lý các cột trùng.

### 3.3. Tiền xử lý
- Loại bỏ các dòng không có `med_salary` cho RQ3.
- Chuẩn hóa văn bản mô tả.
- Trích xuất kỹ năng ESCO.
- Chuẩn hóa các biến phân loại & số.
- Tạo thêm biến (desc_len, views_applies_ratio,…).

### 3.4. EDA
- Heatmap missing values.
- Phân phối salary.
- Boxplot salary theo kinh nghiệm.
- Top title / countries / cities.
- Views vs applies.
- Phân phối độ dài mô tả.

### 3.5. Các phương pháp khai phá

#### 3.5.1. RQ1 – Phân cụm mô tả công việc
TF-IDF → K-means → chọn k bằng silhouette → giải thích từ khóa.

#### 3.5.2. RQ2 – Khai phá kỹ năng bằng ESCO ontology
- Chuẩn hóa kỹ năng.
- Xây dựng ma trận đồng xuất hiện.
- Network graph.
- Community detection.
- Vẽ từng cụm.

#### 3.5.3. RQ3 – Dự đoán mức lương
- Tập dữ liệu filtered.
- One-hot + scaling.
- Linear Regression vs Random Forest.
- RMSE + scatter plot.
- Feature importance.

---

## CHƯƠNG 4 – THỰC NGHIỆM & KẾT QUẢ

### 4.1. EDA
Trình bày các biểu đồ chính và insight.

### 4.2. Kết quả RQ1 – Phân cụm nghề nghiệp
Bảng từ khóa theo cụm, mô tả từng cluster.

### 4.3. Kết quả RQ2 – Skill Bundles
Graph tổng, các hình cụm, phân tích cộng đồng.

### 4.4. Kết quả RQ3 – Dự đoán lương
So sánh mô hình, scatter plot, RMSE, feature importance.

---

## CHƯƠNG 5 – KẾT LUẬN

### 5.1 Tóm tắt phát hiện chính

### 5.2 Hạn chế

### 5.3 Hướng phát triển

---

# PHỤ LỤC
Dataset, code, mô hình.
