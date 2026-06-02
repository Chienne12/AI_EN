# 🟡 MODULE 2 — MACHINE LEARNING CỐT LÕI (40 buổi · Tuần 6–13)

**Mục tiêu module:** hiểu BẢN CHẤT mô hình học, **tự code thuật toán từ NumPy** (tận dụng bạn thích toán), đánh giá đúng, gói thành pipeline. Kết thúc: **Dự án 2 (ML end-to-end)**.

> 📐 Trục Toán vẫn chạy song song. Nguồn chính: [Andrew Ng – ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction/) + [machinelearningcoban.com](https://machinelearningcoban.com/) (toán tiếng Việt).

---

## TUẦN 6 — Nền tảng ML (Buổi 1–5)

### Buổi 1 — ML là gì & các loại học
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Định nghĩa ML; phân biệt supervised / unsupervised / reinforcement; quy trình 1 dự án ML. |
| ⌨️ **Bài thực hành** | Liệt kê 5 bài toán thực tế, phân loại đúng nhóm học. |
| ✅ **Kết quả phải đạt** | Giải thích được khác biệt 3 loại học + cho ví dụ. |

### Buổi 2 — Train / Validation / Test
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao phải chia dữ liệu; rò rỉ dữ liệu (data leakage); `train_test_split`. |
| ⌨️ **Bài thực hành** | Chia 1 dataset 70/15/15 bằng sklearn. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao không test trên dữ liệu đã train. |

### Buổi 3 — Overfitting, Underfitting, Bias–Variance
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Trực giác overfit/underfit; đánh đổi bias–variance; dấu hiệu nhận biết. |
| ⌨️ **Bài thực hành** | Fit đa thức bậc 1, 4, 15 lên cùng dữ liệu, quan sát overfit. |
| ✅ **Kết quả phải đạt** | Nhìn đồ thị nhận ra model nào overfit/underfit. |

### Buổi 4 — Tiền xử lý cho ML
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Feature scaling (standardize/normalize), encoding biến phân loại; vì sao cần. |
| ⌨️ **Bài thực hành** | StandardScaler + OneHotEncoder trên 1 dataset có cả số & chữ. |
| ✅ **Kết quả phải đạt** | Chuẩn hóa & encode đúng; hiểu vì sao scale ảnh hưởng model. |

### Buổi 5 — Ôn tập tuần + đọc lý thuyết
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hệ thống hóa khái niệm tuần 6; đọc bài tương ứng trên machinelearningcoban. |
| ⌨️ **Bài thực hành** | Viết "cheat sheet" 1 trang về quy trình ML. |
| ✅ **Kết quả phải đạt** | Cheat sheet riêng + commit GitHub. |

---

## TUẦN 7 — Hồi quy tuyến tính (Buổi 6–10)

### Buổi 6 — Hàm giả thuyết & cost function
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Mô hình `y = wx + b`; hàm mất mát MSE; trực giác tối thiểu hóa lỗi. |
| ⌨️ **Bài thực hành** | Tính MSE bằng tay + bằng NumPy cho vài điểm dữ liệu. |
| ✅ **Kết quả phải đạt** | Viết được công thức & code MSE. |

### Buổi 7 — Gradient Descent (toán)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đạo hàm cost theo `w`, `b`; learning rate; cập nhật tham số; vì sao hội tụ. |
| ⌨️ **Bài thực hành** | Tự code gradient descent 1 biến từ NumPy, vẽ đường loss giảm dần. |
| ✅ **Kết quả phải đạt** | Loss giảm qua các vòng lặp; giải thích learning rate quá lớn/nhỏ. |

### Buổi 8 — Tự code Linear Regression
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp giả thuyết + cost + gradient descent thành 1 model hoàn chỉnh. |
| ⌨️ **Bài thực hành** | **Tự code Linear Regression bằng NumPy** (không sklearn), train trên dữ liệu giả. |
| ✅ **Kết quả phải đạt** | Model tự code dự đoán gần đúng; so sánh nghiệm với `LinearRegression` sklearn. |

### Buổi 9 — Hồi quy nhiều biến & vectorization
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Mở rộng nhiều feature; viết dạng ma trận; vectorize gradient descent. |
| ⌨️ **Bài thực hành** | Mở rộng model buổi 8 cho nhiều feature (dạng ma trận). |
| ✅ **Kết quả phải đạt** | Model nhiều biến chạy được; hiểu lợi ích vectorization. |

### Buổi 10 — Đánh giá hồi quy
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | MAE, MSE, RMSE, R²; khi nào dùng cái nào. |
| ⌨️ **Bài thực hành** | Dự đoán giá nhà (dataset thật) + tính 4 metric. |
| ✅ **Kết quả phải đạt** | Đọc & giải thích được R² và RMSE của model. |

---

## TUẦN 8 — Hồi quy Logistic & Phân loại (Buổi 11–15)

### Buổi 11 — Bài toán phân loại & Sigmoid
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Phân loại nhị phân; hàm sigmoid; decision boundary. |
| ⌨️ **Bài thực hành** | Vẽ sigmoid; quan sát ngưỡng 0.5. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao dùng sigmoid cho xác suất. |

### Buổi 12 — Cross-Entropy Loss
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hàm mất mát log loss; vì sao không dùng MSE cho phân loại. |
| ⌨️ **Bài thực hành** | Tính cross-entropy bằng NumPy cho vài ví dụ. |
| ✅ **Kết quả phải đạt** | Viết được công thức & code cross-entropy. |

### Buổi 13 — Tự code Logistic Regression
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp sigmoid + cross-entropy + gradient descent. |
| ⌨️ **Bài thực hành** | **Tự code Logistic Regression bằng NumPy**, train phân loại 2 lớp. |
| ✅ **Kết quả phải đạt** | Model tự code đạt accuracy hợp lý; so với sklearn. |

### Buổi 14 — Phân loại nhiều lớp
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Softmax, one-vs-rest; phân loại >2 lớp. |
| ⌨️ **Bài thực hành** | Phân loại hoa Iris (3 lớp) bằng sklearn. |
| ✅ **Kết quả phải đạt** | Phân loại đúng 3 lớp; hiểu softmax khác sigmoid. |

### Buổi 15 — Regularization (L1/L2)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Overfit trong hồi quy; Ridge (L2), Lasso (L1); tham số `C`/`alpha`. |
| ⌨️ **Bài thực hành** | So sánh model có/không regularization trên dữ liệu nhiễu. |
| ✅ **Kết quả phải đạt** | Giải thích regularization giảm overfit thế nào. |

---

## TUẦN 9 — Đánh giá phân loại (Buổi 16–20)

### Buổi 16 — Confusion Matrix & Accuracy
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | TP/FP/TN/FN; accuracy & hạn chế của nó (dữ liệu lệch). |
| ⌨️ **Bài thực hành** | Vẽ confusion matrix cho 1 model phân loại. |
| ✅ **Kết quả phải đạt** | Đọc đúng 4 ô; chỉ ra khi nào accuracy gây hiểu lầm. |

### Buổi 17 — Precision, Recall, F1
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Công thức & ý nghĩa; đánh đổi precision–recall; chọn metric theo bài toán. |
| ⌨️ **Bài thực hành** | Tính precision/recall/F1 cho bài phát hiện gian lận. |
| ✅ **Kết quả phải đạt** | Chọn đúng metric ưu tiên cho từng tình huống. |

### Buổi 18 — ROC, AUC & Threshold
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đường ROC, chỉ số AUC, điều chỉnh ngưỡng quyết định. |
| ⌨️ **Bài thực hành** | Vẽ ROC, đổi threshold quan sát precision/recall thay đổi. |
| ✅ **Kết quả phải đạt** | Giải thích AUC; biết chỉnh threshold để ưu tiên recall/precision. |

### Buổi 19 — Dữ liệu mất cân bằng
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vấn đề imbalanced data; class weights, oversampling/undersampling (SMOTE intro). |
| ⌨️ **Bài thực hành** | Xử lý dataset lệch lớp + so sánh metric trước/sau. |
| ✅ **Kết quả phải đạt** | Cải thiện recall lớp thiểu số; hiểu vì sao accuracy không đủ. |

### Buổi 20 — Mini-project phân loại
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp kỹ năng tuần 8–9. |
| ⌨️ **Bài thực hành** | Dự đoán churn khách hàng + chọn & giải thích metric đúng. |
| ✅ **Kết quả phải đạt** | Notebook churn có đánh giá đầy đủ, commit GitHub. |

---

## TUẦN 10 — Cây & lân cận (Buổi 21–25)

### Buổi 21 — kNN
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Thuật toán k-Nearest Neighbors; chọn k; ảnh hưởng của scaling. |
| ⌨️ **Bài thực hành** | Tự code kNN đơn giản bằng NumPy + so sklearn. |
| ✅ **Kết quả phải đạt** | kNN tự code chạy đúng; hiểu vì sao cần scale feature. |

### Buổi 22 — Decision Tree
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Entropy/Gini; cách cây chia nhánh; overfit của cây. |
| ⌨️ **Bài thực hành** | Train + trực quan hóa 1 cây quyết định. |
| ✅ **Kết quả phải đạt** | Đọc được cây; giải thích tiêu chí chia. |

### Buổi 23 — Random Forest
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Bagging; vì sao rừng tốt hơn 1 cây; feature importance. |
| ⌨️ **Bài thực hành** | Train Random Forest + xem feature importance. |
| ✅ **Kết quả phải đạt** | RF tốt hơn cây đơn; đọc được feature quan trọng. |

### Buổi 24 — Gradient Boosting
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ý tưởng boosting; XGBoost/LightGBM (công cụ thắng nhiều Kaggle). |
| ⌨️ **Bài thực hành** | Train XGBoost trên dataset tabular. |
| ✅ **Kết quả phải đạt** | Chạy được XGBoost; hiểu khác biệt bagging vs boosting. |

### Buổi 25 — So sánh model
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | So sánh hệ thống nhiều model trên cùng bài toán. |
| ⌨️ **Bài thực hành** | Bảng so sánh logistic / RF / XGBoost (metric + thời gian). |
| ✅ **Kết quả phải đạt** | Chọn model tốt nhất có lý do rõ ràng. |

---

## TUẦN 11 — Feature Engineering (Buổi 26–30)

### Buổi 26 — Scaling & Encoding nâng cao
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | One-hot vs label vs target encoding; khi nào dùng cái nào. |
| ⌨️ **Bài thực hành** | Encode dataset nhiều biến phân loại. |
| ✅ **Kết quả phải đạt** | Chọn encoding phù hợp; tránh tăng chiều quá mức. |

### Buổi 27 — Tạo feature mới
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Feature từ datetime, từ kết hợp biến, binning. |
| ⌨️ **Bài thực hành** | Tạo feature "giờ cao điểm", "nhóm tuổi"... |
| ✅ **Kết quả phải đạt** | ≥3 feature mới có ý nghĩa nghiệp vụ. |

### Buổi 28 — Feature Selection
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chọn feature: tương quan, importance, loại feature thừa. |
| ⌨️ **Bài thực hành** | Loại feature ít giá trị, so accuracy trước/sau. |
| ✅ **Kết quả phải đạt** | Giảm feature mà giữ/ tăng hiệu năng. |

### Buổi 29 — Pipeline & ColumnTransformer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đóng gói tiền xử lý + model thành `Pipeline`; tránh leakage. |
| ⌨️ **Bài thực hành** | Xây pipeline xử lý số + chữ + model trong 1 đối tượng. |
| ✅ **Kết quả phải đạt** | Pipeline `fit/predict` 1 lệnh; tái sử dụng được. |

### Buổi 30 — Cross-Validation
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | k-fold CV; vì sao đáng tin hơn 1 lần split; stratified CV. |
| ⌨️ **Bài thực hành** | Đánh giá model bằng 5-fold CV. |
| ✅ **Kết quả phải đạt** | Báo cáo điểm CV trung bình ± độ lệch. |

---

## TUẦN 12 — Học không giám sát (Buổi 31–35)

### Buổi 31 — k-means
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Thuật toán k-means; tâm cụm; hội tụ. |
| ⌨️ **Bài thực hành** | Tự code k-means đơn giản bằng NumPy. |
| ✅ **Kết quả phải đạt** | k-means tự code phân cụm đúng dữ liệu giả. |

### Buổi 32 — Chọn số cụm
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Elbow method, silhouette score. |
| ⌨️ **Bài thực hành** | Vẽ elbow để chọn k tối ưu. |
| ✅ **Kết quả phải đạt** | Chọn k có cơ sở (không đoán). |

### Buổi 33 — PCA (toán)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Giảm chiều; variance; trực giác eigenvector/eigenvalue. |
| ⌨️ **Bài thực hành** | Tính PCA bằng NumPy (covariance + eig). |
| ✅ **Kết quả phải đạt** | Giải thích PCA giữ lại "phương sai" thế nào. |

### Buổi 34 — PCA thực hành
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Dùng PCA của sklearn; trực quan hóa dữ liệu nhiều chiều về 2D. |
| ⌨️ **Bài thực hành** | Giảm chiều 1 dataset rồi vẽ scatter 2D. |
| ✅ **Kết quả phải đạt** | Vẽ được dữ liệu cao chiều trên 2D có ý nghĩa. |

### Buổi 35 — Project phân cụm
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ứng dụng clustering. |
| ⌨️ **Bài thực hành** | Phân khúc khách hàng (customer segmentation) + đặt tên cụm. |
| ✅ **Kết quả phải đạt** | Notebook phân cụm + diễn giải nghiệp vụ, commit GitHub. |

---

## TUẦN 13 — Tuning & Capstone (Buổi 36–40)

### Buổi 36 — Hyperparameter Tuning
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | GridSearchCV, RandomizedSearchCV; phân biệt tham số vs siêu tham số. |
| ⌨️ **Bài thực hành** | Tune Random Forest/XGBoost bằng GridSearch. |
| ✅ **Kết quả phải đạt** | Tìm được bộ siêu tham số tốt hơn mặc định. |

### Buổi 37 — Đánh giá nâng cao
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Learning curve, validation curve; chẩn đoán bias/variance bằng đồ thị. |
| ⌨️ **Bài thực hành** | Vẽ learning curve, kết luận thiếu dữ liệu hay thiếu model. |
| ✅ **Kết quả phải đạt** | Đọc learning curve → quyết định cải thiện đúng hướng. |

### Buổi 38 — Pipeline end-to-end
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ghép toàn bộ: clean → feature → model → CV → tune trong 1 pipeline. |
| ⌨️ **Bài thực hành** | Xây pipeline hoàn chỉnh tái sử dụng + lưu model (`joblib`). |
| ✅ **Kết quả phải đạt** | Pipeline chạy 1 lệnh từ raw data → dự đoán. |

### Buổi 39 — 🎯 DỰ ÁN 2 (xây dựng)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chọn bài toán thật (dự đoán giá / churn / phân loại) — làm end-to-end. |
| ⌨️ **Bài thực hành** | Clean → feature → train ≥3 model → tune → đánh giá. |
| ✅ **Kết quả phải đạt** | Có model tốt nhất + bảng so sánh + CV. |

### Buổi 40 — 🎯 DỰ ÁN 2 (hoàn thiện)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Viết giải thích **VÌ SAO model tốt/tệ**; hoàn thiện README. |
| ⌨️ **Bài thực hành** | Viết phân tích lỗi + hạn chế + hướng cải thiện; push GitHub. |
| ✅ **Kết quả phải đạt** | Repo DA2 chỉn chu + phần "giải thích" → **bỏ vào portfolio**. |

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 2
- [ ] **Tự code** được Linear & Logistic Regression bằng NumPy
- [ ] Giải thích được gradient descent, overfit, bias–variance
- [ ] Chọn & đọc đúng metric (precision/recall/F1/AUC)
- [ ] Dùng tree-based, kNN, k-means, PCA
- [ ] Xây pipeline + cross-validation + tuning
- [ ] **DA2 (ML end-to-end)** trên GitHub có phần giải thích

➡️ **Tiếp theo:** `module-3-deep-learning.md`


---

## 📚 TÀI NGUYÊN CHI TIẾT THEO BUỔI (Hướng B)

> **📺 học chính** · **🇻🇳 bổ trợ** · **🔧 tra cứu** · **🆘 kẹt thì hỏi đâu**. Bật phụ đề + [Immersive Translate](https://immersivetranslate.com/).
> ⭐ Kênh **[StatQuest (Josh Starmer)](https://www.youtube.com/@statquest)** là "vũ khí" cho người thích hiểu bản chất — mỗi thuật toán có 1 video giải thích cực rõ. Dùng xuyên suốt module này.

### 🧱 Nền tảng ML (Buổi 1–5)
- 📺 [Andrew Ng – ML Specialization, Course 1, Week 1](https://www.coursera.org/learn/machine-learning) · [Kaggle Learn – Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning)
- 📺 StatQuest: "Machine Learning Fundamentals: Bias and Variance", "Cross Validation"
- 🇻🇳 [machinelearningcoban – Overfitting](https://machinelearningcoban.com/2017/03/04/overfitting/)
- 🔧 [Stanford CS229 cheatsheets](https://github.com/afshinea/stanford-cs-229-machine-learning)

### 📈 Hồi quy tuyến tính (Buổi 6–10)
- 📺 Andrew Ng C1 Week 1–2 (cost function, gradient descent) · StatQuest: "Linear Regression", "Gradient Descent Step-by-Step"
- 🇻🇳 [Linear Regression](https://machinelearningcoban.com/2016/12/28/linearregression/) · [Gradient Descent](https://machinelearningcoban.com/2017/01/12/gradientdescent/)
- 🔧 [sklearn – Linear Models](https://scikit-learn.org/stable/modules/linear_model.html) · Sách: [ISLR ch.3](https://www.statlearning.com/)
- ✅ Đối chiếu code tự viết với `sklearn.linear_model.LinearRegression`

### 🎯 Hồi quy Logistic & Phân loại (Buổi 11–15)
- 📺 Andrew Ng C1 Week 3 (logistic regression, regularization) · StatQuest: "Logistic Regression"
- 🇻🇳 [Logistic Regression](https://machinelearningcoban.com/2017/01/27/logisticregression/) · [Softmax Regression](https://machinelearningcoban.com/2017/02/17/softmax/)
- 🔧 [sklearn – LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

### 📊 Đánh giá phân loại (Buổi 16–20)
- 📺 StatQuest: "Confusion Matrix", "Sensitivity and Specificity", "ROC and AUC" · Andrew Ng C2 (metrics for skewed data)
- 🔧 [sklearn – Metrics & scoring](https://scikit-learn.org/stable/modules/model_evaluation.html) · [Google ML Crash Course – Classification](https://developers.google.com/machine-learning/crash-course/classification)
- 🎯 Dataset gợi ý: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

### 🌳 Cây & kNN (Buổi 21–25)
- 📺 StatQuest: "Decision Trees", "Random Forests Part 1-2", "Gradient Boost", "XGBoost" · [Kaggle Learn – Intermediate ML](https://www.kaggle.com/learn/intermediate-machine-learning)
- 🇻🇳 [KNN](https://machinelearningcoban.com/2017/01/08/knn/) · machinelearningcoban "Decision Tree (ID3)"
- 🔧 [XGBoost docs](https://xgboost.readthedocs.io/) · [sklearn – Ensembles](https://scikit-learn.org/stable/modules/ensemble.html)

### 🛠️ Feature Engineering (Buổi 26–30)
- 📺 [Kaggle Learn – Feature Engineering](https://www.kaggle.com/learn/feature-engineering)
- 🔧 [sklearn – Preprocessing](https://scikit-learn.org/stable/modules/preprocessing.html) · [sklearn – Pipeline](https://scikit-learn.org/stable/modules/compose.html)

### 🔍 Học không giám sát (Buổi 31–35)
- 📺 StatQuest: "K-means clustering", "PCA Step-by-Step" · Andrew Ng C3 Week 1 (clustering)
- 🇻🇳 [K-means](https://machinelearningcoban.com/2017/01/01/kmeans/) · [PCA](https://machinelearningcoban.com/2017/06/15/pca/)
- 🔧 [sklearn – Clustering](https://scikit-learn.org/stable/modules/clustering.html)

### ⚙️ Tuning & Capstone (Buổi 36–40)
- 📺 StatQuest: "Cross Validation" · [Kaggle Learn – Intermediate ML (tuning)](https://www.kaggle.com/learn/intermediate-machine-learning)
- 🔧 [sklearn – GridSearchCV](https://scikit-learn.org/stable/modules/grid_search.html)
- 🎯 DA2 dataset: Telco Churn / [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
- 🆘 Lý thuyết khó → [Cross Validated](https://stats.stackexchange.com/); code → Stack Overflow tag [`scikit-learn`]
