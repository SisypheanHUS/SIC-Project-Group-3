# SIC-Project-Group-3
# Toxic-comment-classification
Dự án nhóm cho chương trình SIC tại trường ĐH Khoa học tự nhiên.
Phân loại bình luận thành độc hại hoặc không độc hại và các thuộc tính con về độ độc hại như tấn công danh tính, đe dọa, xúc phạm, v.v.
# Description
Các thành viên bao gồm:

SIC2257 Nguyễn Đức Sĩ   
SIC2255 Đinh Thái Tuấn  
SIC2256 Đỗ Minh Quang  
SIC2266 Nguyễn Thuỳ Trang 

Dự án nhằm xây dựng một mô hình có khả năng phát hiện các loại độc hại khác nhau như mối đe dọa, sự thô tục, lăng mạ và phân biệt chủng tộc. Chúng tôi sẽ sử dụng một tập dữ liệu gồm các bình luận được thu thập bởi Kaggle và huấn luyện bởi nhiều mô hình khác nhau. Mục tiêu của chúng tôi là so sánh và tìm ra mô hình tốt nhất cho dự án này.
- Dữ liệu có thể tìm thấy ở đây [here]([https://www.kaggle.com/fedesoriano/traffic-prediction-dataset](https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge/data?select=sample_submission.csv.zip)).

# Bắt đầu
## Các thư viện cần có 
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Sklearn
- Tensorflow
- NLTK
- Wordcloud

## Machine learning Classifiers used
 **Multinomial Naive Bayes**
 
 
Mô hình Multinomial Naive Bayes là một trong những thuật toán phân loại thuộc họ Naive Bayes, sử dụng Định lý Bayes để phân loại,thường được sử dụng đối với các bài toán phân loại văn bản. Đây là một trong những mô hình đơn giản nhưng hiệu quả, đặc biệt khi áp dụng cho các bài toán với dữ liệu có tính chất phân phối rời rạc. Chúng tôi đạt được độ chính xác là 89.77% khi sử dụng mô hình này.

** SVM ( Support Vector Machine )**

SVM là một thuật toán Supervised Learning được dùng trong các bài toán phân loại, hồi quy, nhận dạng mẫu. SVM hoạt động bằng cách tìm kiếm một siêu phẳng để phân chia tập dữ liệu thành các lớp khác nhau, và siêu phẳng này phải có khoảng cách (hay còn gọi là lề) lớn nhất giữa các điểm dữ liệu thuộc hai lớp. Nếu tập dữ liệu có thể phân chia hoàn toàn (linearly separable), thì SVM sẽ tìm kiếm siêu phẳng tối ưu sao cho khoảng cách giữa các điểm dữ liệu gần siêu phẳng nhất và siêu phẳng là lớn nhất. Chúng tôi đạt được độ chính xác là 85.43% khi sử dụng mô hình này.

**XGBoost Classifier**

Mô hình XGBoosting (hay Extreme Gradient Boosting) là một mô hình của phương pháp Ensemble trong Machine Learning, sử dụng sự kết hợp của các mô hình yếu hơn để tạo nên mô hình tốt hơn. XGBoosting sử dụng biến thể Boosting, biến thể này sẽ xây dựng một lượng lớn các model (thường là cùng loại). Mỗi model sau sẽ học cách sửa những lỗi của model trước (dữ liệu mà model trước dự đoán sai), tạo thành một chuỗi các model mà model sau sẽ tốt hơn model trước bởi trọng số được update qua mỗi model. Và chúng ta sẽ lấy kết quả của model cuối cùng trong chuỗi model này làm kết quả trả về. Chúng tôi đạt được độ chính xác là 91.62% khi sử dụng mô hình này.

**Logistic Regression**

Hồi quy logistic là một mô hình thống kê học máy dùng để dự đoán xác suất xảy ra của một sự kiện nhị phân (có hai kết quả: thành công hoặc thất bại, 0 hoặc 1). Mô hình này được sử dụng rộng rãi trong các bài toán phân loại, nơi mà mục tiêu là dự đoán một nhãn thuộc về một trong hai lớp. Thay vì dự đoán giá trị trực tiếp như trong hồi quy tuyến tính, hồi quy logistic dự đoán xác suất một sự kiện thuộc về một lớp cụ thể. Chúng tôi đạt được độ chính xác là 86.16% khi sử dụng mô hình này.

** LSTM **



## Comparision of Classifiers
Chúng tôi đã so sánh năm mô hình học máy khác nhau (SVM, LSTM, Multinomial Naive Bayes , XG Boost, Logistic Regression). Đối với các mô hình này,các chỉ số như Hamming_loss, Accuracy, Log_loss, ROC, Micro-averaged over all classes,Micro-averaged over all toxicity levels được so sánh.



