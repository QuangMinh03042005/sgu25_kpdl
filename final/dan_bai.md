# Dàn Bài Báo Cáo Khai Phá Dữ Liệu

## CHƯƠNG 1 – GIỚI THIỆU

### 1.1. Bối cảnh

- Thị trường lao động toàn cầu đang thay đổi mạnh mẽ.
- LinkedIn là nền tảng tuyển dụng lớn nhất thế giới, phản ánh nhu cầu nhân lực theo thời gian thực.
- Dữ liệu tuyển dụng là nguồn quan trọng để phân tích xu hướng nghề nghiệp.

### 1.2. Lý do chọn đề tài

- Dataset LinkedIn Job Postings có quy mô lớn và công khai.
- Phù hợp để áp dụng đầy đủ kỹ thuật Data Mining.
- Mang lại insight thực tế về thị trường tuyển dụng.

### 1.3. Mục tiêu nghiên cứu

1. Phân tích và khám phá các nhóm nghề nghiệp chính dựa trên tên công việc và kỹ năng.
2. Tìm ra các kỹ năng có xu hướng xuất hiện cùng nhau trong bài tuyển dụng.
3. Xác định các yếu tố ảnh hưởng đến loại hình công việc (remote/onsite/hybrid).

### 1.4. Câu hỏi nghiên cứu

- Các nhóm nghề nghiệp chủ đạo trên thị trường tuyển dụng được hình thành và phân bố như thế nào dựa trên dữ liệu tuyển dụng từ LinkedIn?
- Những kỹ năng nào có xu hướng xuất hiện đồng thời trong các bài đăng tuyển dụng, và mức độ liên kết giữa các kỹ năng đó ra sao?
- Các yếu tố đặc trưng của công việc (kỹ năng, chức danh, địa điểm, ngành nghề) ảnh hưởng như thế nào đến khả năng một công việc được phân loại là remote hoặc onsite?

### 1.5. Đối tượng & phạm vi nghiên cứu

- Đối tượng: Các bài đăng tuyển dụng trên LinkedIn.
- Phạm vi: ~124.000 bản ghi, nhiều ngành nghề, nhiều quốc gia.

### 1.6. Phương pháp tiếp cận

- Thu thập & tích hợp dữ liệu.
- Tiền xử lý dữ liệu.
- Phân tích mô tả (EDA).
- Clustering → phân nhóm nghề.
- Association Rules → phân tích kỹ năng.
- Classification → dự đoán loại hình làm việc.
- Trực quan hóa kết quả.

---

## CHƯƠNG 2 – CƠ SỞ LÝ THUYẾT

### 2.1. Khai phá dữ liệu (Data Mining)

- Khái niệm.
- Vai trò trong phân tích dữ liệu lớn.
- Các bước CRISP-DM.

### 2.2. Tiền xử lý dữ liệu

- Làm sạch dữ liệu.
- Chuẩn hóa dữ liệu.
- Mã hóa dữ liệu phân loại.
- Xử lý văn bản: tokenization, stopwords, lemmatization.

### 2.3. Vector hóa văn bản

- TF-IDF
- CountVectorizer

### 2.4. Clustering

- K-Means: nguyên lý, lựa chọn k (elbow method).
- Hierarchical Clustering: dendrogram.

### 2.5. Luật kết hợp (Association Rules)

- Transaction data.
- Apriori.
- FP-Growth.
- Support – Confidence – Lift.

### 2.6. Phân lớp (Classification)

- Logistic Regression.
- Random Forest.
- SVM.
- Naive Bayes.

### 2.7. Đánh giá mô hình

- Accuracy.
- Precision – Recall – F1-score.
- Confusion matrix.
- Silhouette score.

---

## CHƯƠNG 3 – DỮ LIỆU & PHƯƠNG PHÁP

### 3.1. Giới thiệu dataset LinkedIn Job Postings

- Nguồn: Kaggle.
- Cấu trúc nhiều file: postings.csv, companies/, jobs/, mappings/.
- Cần join dữ liệu trước khi phân tích.

### 3.2. Tích hợp dữ liệu (Data Integration)

- Join postings.csv với jobs và skills.
- Join postings.csv với companies bằng company_id.
- Tạo bảng dữ liệu cuối gồm: job_title, skills_desc, work_type, location, industry, ...

### 3.3. Tiền xử lý dữ liệu

- Làm sạch giá trị thiếu.
- Chuẩn hóa text.
- Tách kỹ năng từ `skills_desc`.
- Mã hóa dữ liệu phân loại (One-hot, Label encoding).

### 3.4. Phân tích mô tả ban đầu (EDA)

- Phân bố theo quốc gia.
- Top job titles.
- Top kỹ năng.
- Heatmap tương quan.
- Nhận xét tổng quan.

### 3.5. Phương pháp khai phá dữ liệu

#### 3.5.1. Phân cụm nghề nghiệp

- Dùng job_title + skills_desc → TF-IDF.
- Áp dụng K-Means.
- Đánh giá bằng silhouette score.

#### 3.5.2. Khai phá luật kết hợp kỹ năng

- Làm sạch skills_desc.
- Tách kỹ năng → transaction data.
- Áp dụng Apriori/FP-Growth.
- Phân tích support – confidence – lift.

#### 3.5.3. Phân lớp loại hình công việc

- Biến mục tiêu: work_type.
- Feature: job_title, skills_desc, location, industry.
- Mô hình: Logistic Regression, Random Forest, SVM.
- Đánh giá: accuracy, F1.

---

## CHƯƠNG 4 – THỰC NGHIỆM & KẾT QUẢ

### 4.1. Thiết lập thực nghiệm

- Python.
- Pandas, NumPy.
- scikit-learn.
- NLTK/spaCy.
- mlxtend.
- Matplotlib, Seaborn.

### 4.2. Kết quả phân cụm

- Bảng silhouette.
- Biểu đồ PCA scatter plot.
- Giải thích từng cluster.

### 4.3. Kết quả luật kết hợp kỹ năng

- Bảng luật Lift cao nhất.
- Graph mạng kỹ năng (network graph).
- Nhận xét.

### 4.4. Kết quả phân lớp

- Accuracy từng mô hình.
- Confusion matrix.
- Mô hình tốt nhất và vì sao.

### 4.5. Thảo luận

- Hiệu quả mô hình.
- Ý nghĩa thực tiễn.
- Liên hệ với thị trường lao động.

---

## CHƯƠNG 5 – KẾT LUẬN & KIẾN NGHỊ

### 5.1. Kết luận

- Các nhóm nghề chính.
- Các bộ kỹ năng phổ biến.
- Yếu tố ảnh hưởng remote/onsite.

### 5.2. Hạn chế

- Thiếu job description chi tiết.
- Một số kỹ năng không chuẩn hóa hoàn toàn.

### 5.3. Hướng mở rộng

- Dùng mô hình embedding như BERT.
- Phân tích theo từng quốc gia cụ thể.
- Dự đoán mức lương nếu có thêm dữ liệu.
