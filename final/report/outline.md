# ĐỀ TÀI: KHAI PHÁ DỮ LIỆU TUYỂN DỤNG LINKEDIN: PHÂN TÍCH CẤU TRÚC MÔ TẢ CÔNG VIỆC, KỸ NĂNG VÀ MỨC LƯƠNG

# I. GIỚI THIỆU

## 1. Tổng quan đề tài
- Bối cảnh thị trường lao động và sự phát triển của tuyển dụng trực tuyến.
- Vai trò của dữ liệu tuyển dụng quy mô lớn trong việc phân tích xu hướng nghề nghiệp và kỹ năng.
- Giới thiệu nền tảng LinkedIn và bộ dữ liệu LinkedIn Job Postings.
- Ý nghĩa của khai phá dữ liệu trong nghiên cứu thị trường lao động.

## 2. Tình hình nghiên cứu
- Tổng quan các nghiên cứu liên quan đến phân tích dữ liệu tuyển dụng trực tuyến.
- Các hướng nghiên cứu về phân cụm mô tả công việc, khai phá kỹ năng và phân tích mức lương.
- Hạn chế của các nghiên cứu trước và khoảng trống nghiên cứu.

## 3. Mục tiêu và câu hỏi nghiên cứu
### 3.1. Mục tiêu nghiên cứu
- Khám phá cấu trúc nội dung của mô tả công việc trong dữ liệu tuyển dụng LinkedIn.
- Khai phá các mẫu đồng xuất hiện kỹ năng và các nhóm kỹ năng đặc trưng.
- Phân tích các yếu tố ảnh hưởng đến mức lương được công bố trong tin tuyển dụng.

### 3.2. Câu hỏi nghiên cứu
- **RQ1:** Các mô tả công việc trên LinkedIn có tự nhiên hình thành những nhóm nội dung (job description themes) khác nhau hay không, khi không sử dụng bất kỳ nhãn nghề nghiệp hoặc kỹ năng có sẵn nào?
- **RQ2:** Các kỹ năng trong mô tả công việc có xu hướng đồng xuất hiện theo những mẫu nào, và những mẫu này phản ánh cấu trúc kỹ năng của thị trường lao động ra sao?
- **RQ3:** Những yếu tố nào trong thông tin tuyển dụng có ảnh hưởng đáng kể đến mức lương được công bố, và mức độ dự đoán lương từ các yếu tố này đến đâu?

## 4. Phương pháp nghiên cứu và hướng tiếp cận
- Hướng tiếp cận khai phá dữ liệu (Data Mining) và phân tích khám phá (Exploratory Data Analysis).
- Áp dụng các phương pháp không giám sát, khai phá mẫu và phân tích dự đoán.
- Quy trình nghiên cứu tổng quát theo CRISP-DM.

## 5. Đối tượng và phạm vi nghiên cứu


# II. CƠ SỞ LÝ THUYẾT

## 1. Các khái niệm cơ bản
- Khai phá dữ liệu (Data Mining).
- Phân tích khám phá dữ liệu (EDA).
- Khai phá văn bản (Text Mining).
- Phân cụm (Clustering), khai phá mẫu (Pattern Mining) và hồi quy (Regression).

## 2. Các thuật toán và phương pháp sử dụng
- Vector hóa văn bản (TF-IDF, n-gram).
- Phân cụm không giám sát (K-means).
- Khai phá luật kết hợp và đồng xuất hiện kỹ năng.
- Phân tích mạng lưới và phát hiện cộng đồng (Community Detection).
- Mô hình hồi quy và Random Forest cho dự đoán mức lương.

## 3. Nghiên cứu liên quan
- Các nghiên cứu phân tích dữ liệu tuyển dụng và thị trường lao động.
- Ứng dụng ontology kỹ năng (ESCO) trong phân tích kỹ năng.
- So sánh và liên hệ với hướng tiếp cận của đề tài.


# III. DỮ LIỆU VÀ PHƯƠNG PHÁP ĐỀ XUẤT

## 1. Giới thiệu bộ dữ liệu
### 1.1 Tổng quan về bộ dữ liệu LinkedIn Job Postings và bối cảnh thu thập dữ liệu.
### 1.2 Cấu trúc tổng thể của bộ dữ liệu và các bảng dữ liệu chính.
### 1.3 Mối quan hệ giữa các bảng dữ liệu và quá trình tích hợp dữ liệu.
### 1.4 Các thuộc tính (cột) chính được khai thác cho từng câu hỏi nghiên cứu (RQ1, RQ2, RQ3).
### 1.5 Phạm vi nghiên cứu và các hạn chế của dữ liệu.

## 2. Xác định vấn đề và tiền xử lý dữ liệu

## 3. Phương pháp đề xuất cho từng câu hỏi nghiên cứu
### 3.1 Phương pháp phân cụm mô tả công việc cho RQ1.
### 3.2 Phương pháp khai phá mẫu kỹ năng và phân tích mạng lưới cho RQ2.
### 3.3 Phương pháp phân tích và dự đoán mức lương cho RQ3.


# IV. THỰC NGHIỆM, KẾT QUẢ VÀ THẢO LUẬN

## 1. Thiết lập thực nghiệm và độ đo đánh giá
### 1.1 Môi trường thực nghiệm và công cụ sử dụng.
### 1.2 Tham số và cấu hình mô hình.
### 1.3 Các độ đo đánh giá (silhouette score, RMSE, R², …).

## 2. Kết quả thực nghiệm cho RQ1
### 2.1 Kết quả phân cụm mô tả công việc.
### 2.2 Phân tích các nhóm nội dung (job description themes).
### 2.3 Trực quan hóa kết quả phân cụm.

## 3. Kết quả thực nghiệm cho RQ2
### 3.1 Các mẫu đồng xuất hiện kỹ năng và nhóm kỹ năng đặc trưng.
### 3.2 Phân tích network graph và các cộng đồng kỹ năng.
### 3.3 Thảo luận ý nghĩa của các skill bundles.

## 4. Kết quả thực nghiệm cho RQ3
### 4.1 Phân tích các yếu tố ảnh hưởng đến mức lương.
### 4.2 Kết quả mô hình dự đoán lương.
### 4.3 Đánh giá và so sánh mô hình.

## 5. Thảo luận
### 5.1 Tổng hợp kết quả của ba câu hỏi nghiên cứu.
### 5.2 Ưu điểm và hạn chế của phương pháp.
### 5.3 Ý nghĩa thực tiễn của nghiên cứu.


# V. KẾT LUẬN

## 1. Tóm tắt các kết quả chính của nghiên cứu.
## 2. Đóng góp của đề tài đối với phân tích dữ liệu tuyển dụng.
## 3. Hạn chế và hướng nghiên cứu trong tương lai.
