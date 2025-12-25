# 📑 DÀN BÀI SLIDE (THEO CHƯƠNG BÁO CÁO)

## **Slide 1 – Trang bìa**

* Tên đề tài
* Môn học / Giảng viên
* Sinh viên thực hiện
* Trường / Khoa

---

## **Slide 2 – Mục lục (Agenda)**

1. Giới thiệu
2. Cơ sở lý thuyết
3. Dữ liệu
4. RQ1
5. RQ2
6. RQ3
7. Thảo luận & kết luận

---

# 🔹 **CHƯƠNG I. GIỚI THIỆU**

## **Slide 3 – Bối cảnh nghiên cứu**

* Sự phát triển của tuyển dụng trực tuyến
* LinkedIn như nguồn dữ liệu thị trường lao động
* Nhu cầu phân tích JD, kỹ năng và lương

## **Slide 4 – Mục tiêu & câu hỏi nghiên cứu**

* Mục tiêu tổng quát
* Ba câu hỏi nghiên cứu:

  * RQ1: Chủ đề nội dung JD
  * RQ2: Skill bundles
  * RQ3: Yếu tố ảnh hưởng lương

---

# 🔹 **CHƯƠNG II. CƠ SỞ LÝ THUYẾT**

## **Slide 5 – Cơ sở lý thuyết & phương pháp nền**

* Data Mining & EDA
* Text Mining (TF-IDF, n-gram)
* Clustering, Pattern Mining
* Regression & Random Forest

*(Slide này lướt nhanh – không đi sâu công thức)*

---

# 🔹 **CHƯƠNG III. DỮ LIỆU & PHƯƠNG PHÁP**

## **Slide 6 – Dữ liệu nghiên cứu**

* Dataset: LinkedIn Job Postings
* Các bảng chính: jobs, companies, skills, industries
* Quy mô & phạm vi dữ liệu

## **Slide 7 – Quy trình xử lý dữ liệu tổng thể**

* Merge dữ liệu
* Làm sạch & tiền xử lý
* Feature engineering
* Phân tích theo từng RQ
  👉 *(đặt sơ đồ pipeline tổng quát ở đây)*

---

# 🔹 **CHƯƠNG IV. KẾT QUẢ THỰC NGHIỆM**

## 🔸 **RQ1 – Phân cụm mô tả công việc**

## **Slide 8 – Phương pháp cho RQ1**

* TF-IDF + K-means
* Chạy trên toàn bộ dữ liệu
* Đánh giá hậu nghiệm bằng ngành nghề

## **Slide 9 – Kết quả phân cụm JD**

* Số cluster
* Ví dụ top keywords theo cluster
* Nhận xét tổng quan

## **Slide 10 – Diễn giải Job Description Themes**

* Gộp cluster → **meta-themes**
* 6–7 nhóm chủ đề chính (IT, Healthcare, Sales, Education, …)

## **Slide 11 – Đánh giá hậu nghiệm theo ngành nghề**

* Heatmap cluster × industry
* Nhận xét cấu trúc nội dung tiềm ẩn

---

## 🔸 **RQ2 – Khai phá skill bundles**

## **Slide 12 – Phương pháp cho RQ2**

* ESCO skills
* Co-occurrence, lift, confidence
* Network graph & community detection

## **Slide 13 – Các mẫu đồng xuất hiện kỹ năng**

* Ví dụ các cặp kỹ năng mạnh
* Ý nghĩa của lift cao

## **Slide 14 – Network graph & cộng đồng kỹ năng**

* Số node, edge, community
* Minh họa network graph

## **Slide 15 – Diễn giải các skill bundles**

* Nhóm kỹ năng kỹ thuật
* Nhóm y tế
* Nhóm kinh doanh – quản lý
* Nhóm chuyên ngành hẹp

---

## 🔸 **RQ3 – Phân tích & dự đoán mức lương**

## **Slide 16 – Phương pháp cho RQ3**

* Target: normalized_salary (log)
* Feature engineering
* Random Forest (explanatory model)

## **Slide 17 – Kết quả mô hình dự đoán**

* RMSE, MAE, R²
* Biểu đồ Actual vs Predicted
* Nhận xét xu hướng dự đoán

## **Slide 18 – Các yếu tố ảnh hưởng đến lương**

* Permutation importance
* Country mean salary
* Seniority, số kỹ năng, quy mô công ty

---

# 🔹 **CHƯƠNG V. THẢO LUẬN & KẾT LUẬN**

## **Slide 19 – Thảo luận**

* Tổng hợp kết quả RQ1–RQ3
* Điểm mạnh của phương pháp
* Hạn chế của dữ liệu & mô hình

## **Slide 20 – Kết luận & hướng nghiên cứu**

* Đóng góp chính của đề tài
* Ý nghĩa thực tiễn
* Hướng phát triển trong tương lai