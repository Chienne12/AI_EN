# 🟢 MODULE 1 — PYTHON CHO DỮ LIỆU + SQL (20 buổi · Tuần 2–5)

**Mục tiêu module:** đọc – làm sạch – phân tích – trực quan hóa dữ liệu thành thạo + truy vấn SQL. Kết thúc: **Dự án 1 (EDA)** trên GitHub.

> 🔁 Bắt đầu bằng NumPy Refresh (vì lâu không dùng). Làm bài tự test ở mục 8 của `../lo-trinh-ai-engineer.md` trước.

---

## TUẦN 2 — NumPy (Buổi 1–5)

### Buổi 1 — NumPy Refresh + tạo mảng
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Làm bài tự test 5 câu. Ôn: tạo array (`array`, `zeros`, `ones`, `arange`, `linspace`), shape, dtype, indexing/slicing cơ bản. |
| ⌨️ **Bài thực hành** | Làm 15 bài đầu [numpy-100](https://github.com/rougier/numpy-100). |
| ✅ **Kết quả phải đạt** | Tạo & cắt được array 1D/2D; giải thích `shape` và `dtype`. |

### Buổi 2 — Boolean & fancy indexing
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Boolean indexing (lọc theo điều kiện), fancy indexing (lấy theo list chỉ số), gán giá trị theo điều kiện. (2 thứ hay quên nhất!) |
| ⌨️ **Bài thực hành** | Lọc số chẵn/lớn hơn ngưỡng trong mảng; thay mọi số âm thành 0. |
| ✅ **Kết quả phải đạt** | Lọc & gán theo điều kiện không cần vòng lặp. |

### Buổi 3 — Broadcasting & vectorization
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Broadcasting (phép toán giữa mảng khác shape), vectorization (thay vòng lặp bằng phép mảng) — nền tảng tốc độ của ML. |
| ⌨️ **Bài thực hành** | Chuẩn hóa từng cột ma trận `(x-mean)/std` không dùng vòng lặp; so tốc độ vòng lặp vs vectorized. |
| ✅ **Kết quả phải đạt** | Giải thích broadcasting; viết được phép chuẩn hóa vectorized. |

### Buổi 4 — Phép toán ma trận & axis
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `dot`, `matmul`, `@`, transpose, `reshape`; thao tác theo `axis` (`sum`, `mean`, `max` theo hàng/cột). |
| ⌨️ **Bài thực hành** | Nhân 2 ma trận và giải thích shape; tính mean theo từng cột rồi từng hàng. |
| ✅ **Kết quả phải đạt** | Dùng đúng `axis=0/1`; nhân ma trận đúng quy tắc shape. |

### Buổi 5 — Tổng hợp NumPy (mini-project)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp các kỹ năng NumPy lại. |
| ⌨️ **Bài thực hành** | Làm tiếp [numpy-100](https://github.com/rougier/numpy-100) tới bài ~40; viết hàm tính khoảng cách Euclid giữa các điểm chỉ bằng NumPy. |
| ✅ **Kết quả phải đạt** | Tự tin dùng NumPy; commit notebook NumPy lên GitHub. |

---

## TUẦN 3 — Pandas phần 1 (Buổi 6–10)

### Buổi 6 — Series, DataFrame, đọc dữ liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Khái niệm Series/DataFrame; `read_csv`; xem nhanh dữ liệu (`head`, `tail`, `info`, `describe`, `shape`). |
| ⌨️ **Bài thực hành** | Tải dataset [Titanic](https://www.kaggle.com/c/titanic); đọc & in thông tin tổng quan. |
| ✅ **Kết quả phải đạt** | Đọc CSV, mô tả được dữ liệu có bao nhiêu dòng/cột, kiểu gì. |

### Buổi 7 — Chọn & lọc dữ liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `loc` vs `iloc`, chọn cột, lọc theo điều kiện (boolean), kết hợp nhiều điều kiện. |
| ⌨️ **Bài thực hành** | Lấy hành khách nữ sống sót; lấy người trên 30 tuổi hạng 1. |
| ✅ **Kết quả phải đạt** | Phân biệt `loc`/`iloc`; lọc nhiều điều kiện đúng. |

### Buổi 8 — Biến đổi dữ liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Sắp xếp (`sort_values`), thêm/xóa cột, `apply`, `map`, `value_counts`. |
| ⌨️ **Bài thực hành** | Tạo cột `FamilySize`; đếm số người theo hạng vé. |
| ✅ **Kết quả phải đạt** | Tạo cột mới từ cột cũ; dùng `apply` với hàm tự viết. |

### Buổi 9 — Groupby & tổng hợp
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `groupby`, `agg`, tính thống kê theo nhóm; pivot cơ bản. |
| ⌨️ **Bài thực hành** | Tỷ lệ sống sót theo giới tính & hạng vé. |
| ✅ **Kết quả phải đạt** | Trả lời được câu hỏi dạng "trung bình X theo nhóm Y". |

### Buổi 10 — Merge / Join / Concat
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Gộp nhiều bảng: `merge` (inner/left/right/outer), `concat`. |
| ⌨️ **Bài thực hành** | Tự tạo 2 DataFrame nhỏ rồi merge theo khóa chung. |
| ✅ **Kết quả phải đạt** | Chọn đúng loại join cho từng tình huống. |

---

## TUẦN 4 — Làm sạch & Trực quan hóa (Buổi 11–15)

### Buổi 11 — Xử lý dữ liệu thiếu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `isna`, `dropna`, `fillna`; chiến lược điền (mean/median/mode); khi nào xóa vs điền. |
| ⌨️ **Bài thực hành** | Xử lý cột `Age`, `Cabin`, `Embarked` của Titanic. |
| ✅ **Kết quả phải đạt** | Không còn missing vô lý; giải thích lựa chọn điền/xóa. |

### Buổi 12 — Kiểu dữ liệu, trùng lặp, outlier, chuỗi
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `astype`, `drop_duplicates`, phát hiện outlier (IQR), thao tác chuỗi (`str` methods). |
| ⌨️ **Bài thực hành** | Trích tước hiệu (Mr/Mrs/Miss) từ cột `Name`. |
| ✅ **Kết quả phải đạt** | Dữ liệu đúng kiểu, không trùng; tạo được feature từ chuỗi. |

### Buổi 13 — Matplotlib
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Biểu đồ line, bar, scatter, histogram; tiêu đề, nhãn trục, legend. |
| ⌨️ **Bài thực hành** | Vẽ phân phối tuổi (hist); số người theo hạng vé (bar). |
| ✅ **Kết quả phải đạt** | Vẽ 3 loại biểu đồ có nhãn rõ ràng. |

### Buổi 14 — Seaborn
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `histplot`, `boxplot`, `countplot`, `heatmap` tương quan, `pairplot`. |
| ⌨️ **Bài thực hành** | Heatmap tương quan các biến số; boxplot tuổi theo hạng vé. |
| ✅ **Kết quả phải đạt** | Đọc được heatmap tương quan; chọn biểu đồ hợp với loại dữ liệu. |

### Buổi 15 — Kể chuyện bằng dữ liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ghép biểu đồ thành "câu chuyện"; rút nhận xét có ý nghĩa. |
| ⌨️ **Bài thực hành** | Vẽ 5–7 biểu đồ trả lời "Ai có khả năng sống sót cao?" + viết nhận xét. |
| ✅ **Kết quả phải đạt** | 5–7 biểu đồ + 5 nhận xét logic dựa trên dữ liệu. |

🔗 [Kaggle Learn: Pandas, Data Cleaning, Data Visualization](https://www.kaggle.com/learn)

---

## TUẦN 5 — SQL + Dự án 1 (Buổi 16–20)

### Buổi 16 — SQL cơ bản
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cài DB Browser for SQLite; `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, `DISTINCT`. |
| ⌨️ **Bài thực hành** | Truy vấn cơ bản trên 1 bảng mẫu. |
| ✅ **Kết quả phải đạt** | Viết được truy vấn lọc + sắp xếp + giới hạn. |

### Buổi 17 — Tổng hợp & nhóm
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `COUNT/SUM/AVG/MIN/MAX`, `GROUP BY`, `HAVING`. |
| ⌨️ **Bài thực hành** | Doanh thu trung bình theo nhóm; lọc nhóm bằng HAVING. |
| ✅ **Kết quả phải đạt** | Phân biệt `WHERE` và `HAVING`. |

### Buổi 18 — JOIN
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `INNER JOIN`, `LEFT JOIN`; nối nhiều bảng. |
| ⌨️ **Bài thực hành** | Nối bảng khách hàng – đơn hàng, lấy tên KH + tổng đơn. |
| ✅ **Kết quả phải đạt** | Viết JOIN 2 bảng đúng; hiểu khác biệt INNER vs LEFT. |

### Buổi 19 — Subquery & CTE
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Subquery, `WITH` (CTE), truy vấn lồng. |
| ⌨️ **Bài thực hành** | Giải 20 bài [SQL trên LeetCode/Kaggle](https://leetcode.com/studyplan/top-sql-50/). |
| ✅ **Kết quả phải đạt** | Hoàn thành ≥15/20 bài SQL. |

### Buổi 20 — 🎯 DỰ ÁN 1: EDA hoàn chỉnh
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Gộp toàn bộ kỹ năng: chọn 1 dataset thật (gợi ý "kiếm tiền": giá BĐS, doanh số e-commerce, giá coin), làm EDA đầu-cuối. |
| ⌨️ **Bài thực hành** | Notebook: đọc → làm sạch → ≥7 biểu đồ → 5 nhận xét. Viết README, push GitHub. |
| ✅ **Kết quả phải đạt** | Repo DA1 chỉn chu: notebook chạy được + README + insight rõ → **link bỏ vào portfolio**. |

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 1
- [ ] NumPy: thành thạo indexing, broadcasting, ma trận
- [ ] Pandas: đọc, lọc, groupby, merge, làm sạch
- [ ] Trực quan hóa: Matplotlib + Seaborn kể chuyện
- [ ] SQL: SELECT/JOIN/GROUP BY/subquery (≥15/20 bài)
- [ ] **DA1 (EDA)** trên GitHub có README

➡️ **Tiếp theo:** [`module-2-ml-core.md`](./module-2-ml-core.md)
