# 🟢 MODULE 0 — SETUP & REFRESH (5 buổi · Tuần 1)

**Mục tiêu module:** có môi trường làm việc chuẩn (conda + PyTorch chạy GPU), ôn lại Python/OOP, và biết dùng Git/GitHub. Kết thúc: 1 repo chạy được trên GitHub.

> Nhịp: 5 buổi × 2.5h. Trục Toán bắt đầu song song (3B1B – Linear Algebra, 25'/ngày).

---

### Buổi 1 — Cài đặt môi trường & Jupyter
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cài Miniconda/Anaconda, tạo môi trường ảo riêng, cài VS Code + extension Python, chạy được Jupyter Notebook. Hiểu vì sao cần môi trường ảo (tránh xung đột package). |
| ⌨️ **Bài thực hành** | 1) Tạo env: `conda create -n ai python=3.11`. 2) Kích hoạt: `conda activate ai`. 3) Cài: `pip install numpy pandas matplotlib jupyter`. 4) Mở Jupyter, in `"Hello AI"`. |
| ✅ **Kết quả phải đạt** | Chạy được 1 cell Jupyter trong env `ai`; `python --version` ra 3.11; liệt kê được package bằng `pip list`. |

🔗 [Miniconda](https://docs.conda.io/projects/miniconda/) · [VS Code Python](https://code.visualstudio.com/docs/python/python-tutorial)

---

### Buổi 2 — Cài PyTorch CUDA & kiểm tra GPU (RTX 4050)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cài PyTorch bản CUDA để dùng GPU rời. Hiểu khái niệm CUDA, VRAM. Biết kiểm tra GPU có hoạt động không. |
| ⌨️ **Bài thực hành** | 1) Cài: `pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121`. 2) Chạy: `import torch; print(torch.cuda.is_available()); print(torch.cuda.get_device_name(0))`. 3) Tạo tensor trên GPU: `x = torch.randn(3,3).cuda()`. |
| ✅ **Kết quả phải đạt** | `torch.cuda.is_available()` ra `True`; in được tên `NVIDIA GeForce RTX 4050`; tạo được tensor trên `.cuda()` không lỗi. |

🔗 [PyTorch – Get Started](https://pytorch.org/get-started/locally/)

---

### Buổi 3 — Ôn Python OOP
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ôn class, object, `__init__`, thuộc tính/phương thức, kế thừa, `self`. Hiểu khi nào dùng OOP (vì code ML/DL toàn dùng class: `nn.Module`, model, dataset...). |
| ⌨️ **Bài thực hành** | Viết class `BankAccount` (nạp/rút/xem số dư, chặn rút quá số dư) + 1 class con `SavingsAccount` kế thừa, thêm lãi suất. |
| ✅ **Kết quả phải đạt** | Tạo object, gọi method chạy đúng; class con kế thừa và override được 1 method; giải thích được `self` là gì. |

🔗 [Real Python – OOP](https://realpython.com/python3-object-oriented-programming/)

---

### Buổi 4 — File I/O, Exception, Module
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đọc/ghi file (txt, csv cơ bản), xử lý lỗi với `try/except/finally`, tách code thành module và `import`. Hiểu cấu trúc 1 project Python gọn gàng. |
| ⌨️ **Bài thực hành** | Viết chương trình **quản lý chi tiêu (CLI)**: thêm khoản chi, lưu vào file, đọc lại, tính tổng — có bắt lỗi nhập sai. Tách thành 2 file: `main.py` + `utils.py`. |
| ✅ **Kết quả phải đạt** | App chạy được, lưu/đọc file thành công, không crash khi nhập sai (nhờ try/except); import được hàm từ `utils.py`. |

---

### Buổi 5 — Git & GitHub
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Học `git init`, `add`, `commit`, `branch`, `push`; viết `README.md`; tạo `.gitignore`. Hiểu commit là "ảnh chụp" lịch sử code. |
| ⌨️ **Bài thực hành** | Đưa app chi tiêu (buổi 4) lên GitHub: tạo repo, commit, push; viết README mô tả cách chạy; thêm `.gitignore` (bỏ qua `__pycache__`, env). |
| ✅ **Kết quả phải đạt** | Repo công khai trên GitHub có code + README hiển thị đẹp + ít nhất 2 commit; giải thích được khác biệt giữa `add` và `commit`. |

🔗 [Pro Git (tiếng Việt, free)](https://git-scm.com/book/vi/v2) · [GitHub Docs](https://docs.github.com/en/get-started)

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 0
- [ ] Env `ai` chạy được, PyTorch nhận GPU (`cuda.is_available() == True`)
- [ ] Hiểu & dùng được OOP, file I/O, exception
- [ ] 1 repo GitHub: app quản lý chi tiêu + README + ≥2 commit
- [ ] Đã bắt đầu trục Toán (xem ≥2 video 3B1B Linear Algebra)

➡️ **Tiếp theo:** [`module-1-data-sql.md`](./module-1-data-sql.md)
