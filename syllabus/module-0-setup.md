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


---

## 📚 TÀI NGUYÊN CHI TIẾT THEO BUỔI (Hướng B)

> Mỗi buổi: **📺 học chính** (xem/đọc cái gì) · **🇻🇳 bổ trợ tiếng Việt** · **🔧 tra cứu/cheat sheet** · **🆘 kẹt thì hỏi đâu**.
> Mẹo nghe yếu tiếng Anh: bật phụ đề YouTube + cài [Immersive Translate](https://immersivetranslate.com/) để dịch song ngữ.

### Buổi 1 — Cài môi trường & Jupyter
- 📺 [Miniconda – hướng dẫn cài](https://docs.conda.io/projects/miniconda/en/latest/) · [VS Code Python tutorial](https://code.visualstudio.com/docs/python/python-tutorial)
- 🇻🇳 Tìm trên [Viblo](https://viblo.asia/) từ khóa "cài đặt Anaconda môi trường ảo Python"
- 🔧 [Conda cheat sheet (PDF)](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)
- 🆘 Lỗi cài đặt → Stack Overflow tag [`conda`] / [`anaconda`]

### Buổi 2 — PyTorch CUDA & test GPU (RTX 4050)
- 📺 [PyTorch – Get Started Locally](https://pytorch.org/get-started/locally/) (chọn CUDA 12.x) · [Cài CUDA cho PyTorch trên Windows (YouTube, bật phụ đề)](https://www.youtube.com/results?search_query=install+pytorch+cuda+gpu+windows)
- 🔧 Kiểm tra: `torch.cuda.is_available()`, `nvidia-smi` (xem GPU & VRAM)
- 🆘 GPU không nhận → [PyTorch Forums](https://discuss.pytorch.org/) (search "cuda not available")

### Buổi 3 — OOP Python
- 📺 [Corey Schafer – OOP Playlist (YouTube, có phụ đề)](https://www.youtube.com/playlist?list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc) · [Real Python – OOP](https://realpython.com/python3-object-oriented-programming/)
- 🇻🇳 Viblo: "Lập trình hướng đối tượng trong Python"
- 🔧 [Python docs – Classes](https://docs.python.org/3/tutorial/classes.html)
- ✅ Đối chiếu: so code class của bạn với ví dụ Real Python
- 🆘 Kẹt khái niệm → hỏi AI: dán code + "giải thích `self`/kế thừa sai chỗ nào"

### Buổi 4 — File I/O, Exception, Module
- 📺 [Real Python – Reading/Writing Files](https://realpython.com/read-write-files-python/) · [Real Python – Exceptions](https://realpython.com/python-exceptions/)
- 🔧 [Python docs – Errors & Exceptions](https://docs.python.org/3/tutorial/errors.html)
- 🆘 Lỗi runtime → copy traceback lên Stack Overflow / hỏi AI

### Buổi 5 — Git & GitHub
- 📺 [freeCodeCamp – Git & GitHub for Beginners (YouTube)](https://www.youtube.com/watch?v=RGOj5yH7evk) (bật phụ đề)
- 🇻🇳 [Pro Git – bản tiếng Việt (free)](https://git-scm.com/book/vi/v2)
- 🔧 [Git cheat sheet (GitHub, PDF)](https://education.github.com/git-cheat-sheet-education.pdf) · [GitHub Skills (thực hành)](https://skills.github.com/)
- 🆘 Lỗi push/conflict → Stack Overflow tag [`git`]

---

### 🆘 QUY TRÌNH "KHI KẸT" (áp dụng cả khóa)
1. **Đọc kỹ thông báo lỗi** (90% câu trả lời nằm ở dòng cuối traceback).
2. **Google nguyên văn lỗi** → thường ra Stack Overflow.
3. **Hỏi AI**: dán code + lỗi + "mình muốn làm X, sai ở đâu, vì sao" — nhưng **tự sửa thử trước**.
4. Vẫn kẹt >30 phút → hỏi cộng đồng (Reddit [r/learnmachinelearning](https://www.reddit.com/r/learnmachinelearning/), nhóm FB "Machine Learning cơ bản").
5. **Ghi lại lỗi + cách fix** vào Obsidian/Notion → lần sau không vấp lại.

### 🧠 Công cụ học xuyên suốt
- **Anki** (flashcard lặp ngắt quãng) — tạo thẻ cho khái niệm hay quên.
- **Obsidian / Notion** — nhật ký "hôm nay hiểu gì" (10' cuối mỗi buổi).
