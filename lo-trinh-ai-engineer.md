# 🚀 LỘ TRÌNH AI ENGINEER — SYLLABUS CHI TIẾT (cá nhân hóa)

> Phiên bản 1.0 — thiết kế riêng cho hồ sơ: nền SE (BTEC FPT), Python core ổn, từng học toán đại học, có NumPy/Jupyter, GPU RTX 4050 6GB, học ~2.5h/ngày (đều), thích suy luận & làm toán, mục tiêu kiếm tiền → AI Engineer (LLM/GenAI) → senior → remote.

---

## 0. CHÂN DUNG & QUYẾT ĐỊNH CÁ NHÂN HÓA

| Yếu tố của bạn | Quyết định thiết kế | Lý do |
|---|---|---|
| Thích **suy luận & làm toán** | Nâng "trục Toán" lên thành cột sống thật + ưu tiên **tự code thuật toán từ gốc** (Karpathy) | Đây vừa là sở thích vừa là thứ phân biệt senior với "người gọi API". Biến điểm mạnh thành lợi thế cạnh tranh. |
| Đã có **Python core + nền SE** nhưng **NumPy lâu rồi, quên nhiều** | **Rút gọn** Module 0 + thêm **block NumPy Refresh 2–3 ngày** ở đầu Module 1 | NumPy là công cụ → hồi phục rất nhanh; chỉ cần hâm nóng, không học lại từ 0. |
| **Tiếng Anh đọc OK, nghe yếu** | Tài liệu **chính là tiếng Anh (đọc) + phụ đề**; dùng nguồn Việt (machinelearningcoban, d2l-vn) làm "giàn giáo" lúc lý thuyết khó | Nghề bắt buộc tiếng Anh; nghe yếu đã có phụ đề + AI dịch. Đọc tốt là đủ để tiến. |
| **GPU RTX 4050 6GB** | Train local: CNN, nanoGPT nhỏ, fine-tune QLoRA model 1–3B (4-bit). Việc nặng → Colab/Kaggle free | 6GB đủ cho phần lớn bài học; tránh tốn tiền cloud sớm. |
| **Mục tiêu = kiếm tiền** | Chuyên sâu **LLM/Generative AI + AI Engineering** trên nền ML/DL vững | Theo dữ liệu thị trường: AI Engineer #1 tăng trưởng toàn cầu, khó tuyển nhất ngành IT VN (12,2%), lương cao nhất. ROI cao nhất. |
| **2.5h/ngày, đều, không nhồi** | Lịch ~**17h/tuần**, hoàn thành **~9 tháng**; sẵn sàng apply CTV từ ~tháng 5–6 | Vừa nhanh vừa "ngấm tự nhiên". Khớp khung "5 tháng–1 năm" của bạn. |
| Học liên thông + đang chờ bằng | Lịch có "tuần đệm" linh hoạt | Không vỡ kế hoạch khi bận việc trường. |

### Đánh đổi cần hiểu rõ
Trong ~9 tháng, mục tiêu là **"AI Engineer có chiều sâu ứng dụng"**: hiểu ruột gan model đủ để debug & cải tiến + ship được sản phẩm thật. KHÔNG phải research scientist (cần 2–4 năm + toán nặng). Con đường senior 4 năm của bạn sẽ bồi đắp chiều sâu sau.

---

## 1. NGUYÊN TẮC VẬN HÀNH (đọc 1 lần, áp dụng cả khóa)

1. **Cấu trúc 1 buổi học 2.5h (giữ thói quen & hứng thú):**
   - 🔥 0–10': "khởi động" — đọc lại note hôm qua / 1 flashcard.
   - 📚 10–80': học khái niệm mới (video có phụ đề / đọc).
   - ⌨️ 80–140': **code tay** — gõ lại, sửa, phá, thử. KHÔNG copy-paste.
   - ✍️ 140–150': viết 3 dòng "hôm nay hiểu gì" vào nhật ký học.
2. **Quy tắc chống "tutorial hell":** mỗi module phải đẻ ra 1 dự án trên GitHub mới đi tiếp.
3. **Học công khai (accountability):** mỗi tuần đăng 1 post tiến độ lên LinkedIn + commit GitHub đều → vừa tạo thói quen, vừa là CV sống.
4. **Streak:** đánh dấu ✅ mỗi ngày học. Mất chuỗi thì làm lại, đừng bỏ.
5. **Ôn ngắt quãng:** cuối mỗi tuần dành 30' xem lại note tuần trước.

---

## 2. TRỤC TOÁN CHẠY NỀN (song song Tuần 1–14, ~3h/tuần)

> Bạn thích toán → đây là vũ khí. Học rải đều, mỗi ngày 25–30'.

| Chủ đề | Nguồn (EN chính) | Nguồn Việt (giàn giáo) | Làm gì |
|---|---|---|---|
| Đại số tuyến tính, vector, ma trận | [3Blue1Brown – Essence of Linear Algebra](https://www.3blue1brown.com/topics/linear-algebra) | [machinelearningcoban.com](https://machinelearningcoban.com/) | Tự nhân ma trận bằng NumPy, kiểm chứng tay |
| Giải tích, đạo hàm, gradient | [3Blue1Brown – Essence of Calculus](https://www.3blue1brown.com/topics/calculus) | Khan Academy | Tự code gradient descent |
| Xác suất & thống kê | [Mathematics for ML (Imperial, Coursera audit free)](https://www.coursera.org/specializations/mathematics-machine-learning) | machinelearningcoban | Mô phỏng phân phối bằng NumPy |
| Tối ưu hóa (optimization) | Mathematics for ML | — | Hiểu vì sao SGD/Adam hoạt động |

✅ **Tiêu chí:** đến hết tuần 14, đọc công thức gradient/ma trận không sợ; giải thích được gradient descent bằng lời + code.

---

## 3. SYLLABUS THEO TUẦN

### 🟢 MODULE 0 — Setup & Refresh · Tuần 1 (1 tuần)
**Mục tiêu:** môi trường chuẩn + ôn nhanh Python/OOP/Git.

| Ngày | Nội dung | Thực hành |
|---|---|---|
| 1–2 | conda env, VS Code, Jupyter, cấu trúc project chuẩn | Tạo env `ai`, cài numpy/pandas/jupyter |
| 3–4 | Ôn OOP (class, kế thừa), đọc/ghi file, exception | Viết module nhỏ có class |
| 5–7 | Git/GitHub: commit, branch, push, README, .gitignore | Đẩy 1 CLI nhỏ + README lên GitHub |

📌 *GPU:* cài CUDA-ready PyTorch (`pip install torch --index-url ...cu121`), test `torch.cuda.is_available()` → phải ra `True`.
✅ **Qua môn:** 1 repo GitHub chạy được, README rõ.
🔗 [CS50 Python](https://cs50.harvard.edu/python) (tham khảo phần nâng cao) · [Pro Git (free)](https://git-scm.com/book/vi/v2)

---

### 🟢 MODULE 1 — Python cho dữ liệu + SQL · Tuần 2–5 (4 tuần)
**Mục tiêu:** làm sạch, phân tích, trực quan hóa dữ liệu + SQL.

> 🔁 **NumPy Refresh (2–3 ngày đầu tuần 2):** vì bạn lâu không dùng. Tự test trước (xem mục 8 cuối file). Nếu vấp boolean indexing / `axis` thì luyện lại. Nguồn nhanh: [NumPy – the absolute basics](https://numpy.org/doc/stable/user/absolute_beginners.html) · [rougier/numpy-100 (100 bài tập, GitHub)](https://github.com/rougier/numpy-100).

| Tuần | Nội dung | Thực hành |
|---|---|---|
| 2 | **NumPy Refresh (2–3 ngày)** → rồi nâng cao: vectorization, broadcasting, phép toán ma trận | 30 bài đầu [numpy-100](https://github.com/rougier/numpy-100) + [Kaggle Learn](https://www.kaggle.com/learn) |
| 3 | Pandas: Series/DataFrame, đọc CSV, lọc, groupby, merge | Khám phá dataset Titanic |
| 4 | Data cleaning: thiếu dữ liệu, outlier, kiểu dữ liệu + Matplotlib/Seaborn | Vẽ 5–7 biểu đồ kể chuyện |
| 5 | SQL: SELECT, WHERE, JOIN, GROUP BY, subquery | 20 bài SQL (Kaggle/LeetCode) |

🎯 **DỰ ÁN 1:** EDA hoàn chỉnh 1 dataset thật (chọn dataset bạn thấy "kiếm được tiền" — vd giá BĐS, giá coin, doanh số) → notebook + biểu đồ + 5 nhận xét → GitHub.
✅ **Qua môn:** notebook EDA sạch, có insight.

---

### 🟡 MODULE 2 — Machine Learning cốt lõi · Tuần 6–13 (8 tuần) ⭐
**Mục tiêu:** hiểu BẢN CHẤT model, tự code từ gốc, đánh giá đúng.

| Tuần | Nội dung | Thực hành (tận dụng bạn thích toán) |
|---|---|---|
| 6 | ML là gì; supervised/unsupervised; train/val/test; overfit/underfit | Chia data, quan sát overfit |
| 7 | Hồi quy tuyến tính + hàm mất mát + gradient descent | **Tự code linear regression bằng NumPy** (không dùng sklearn) |
| 8 | Hồi quy logistic + cross-entropy | **Tự code logistic regression từ gốc** |
| 9 | Metrics: accuracy, precision, recall, F1, ROC, confusion matrix | Dự đoán churn, đọc đúng metric |
| 10 | Decision Tree, Random Forest, kNN | So sánh 3 model cùng dữ liệu |
| 11 | Feature engineering + regularization (L1/L2) | Cải thiện model bằng feature |
| 12 | Unsupervised: k-means, PCA | Phân cụm khách hàng + giảm chiều |
| 13 | Cross-validation, tuning (GridSearch) + pipeline sklearn | Gói thành pipeline tái dùng |

🎯 **DỰ ÁN 2:** Bài toán phân loại/dự đoán end-to-end (clean → train → tune → đánh giá) + **giải thích VÌ SAO model tốt/tệ** → GitHub.
✅ **Qua môn:** tự code được linear & logistic regression từ NumPy; giải thích được bias-variance.
🔗 [Andrew Ng – ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction/) (audit free) · [machinelearningcoban.com](https://machinelearningcoban.com/) (toán tiếng Việt) · [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course)

---

### 🟡 MODULE 3 — Deep Learning (từ gốc) · Tuần 14–22 (9 tuần) ⭐⭐
**Mục tiêu:** hiểu & huấn luyện mạng nơ-ron, làm chủ PyTorch, hiểu Transformer từ số 0.

| Tuần | Nội dung | Thực hành (GPU RTX 4050) |
|---|---|---|
| 14 | Nơ-ron, layer, activation, forward pass | Dựng mạng 1 lớp bằng NumPy |
| 15 | Backpropagation (hiểu sâu bằng toán) + optimizer | 🔥 [Karpathy – micrograd](https://github.com/karpathy/nn-zero-to-hero): tự xây autograd |
| 16 | PyTorch: tensor, autograd, nn.Module, training loop | Train MLP trên MNIST (local GPU) |
| 17 | Language model ký tự | 🔥 Karpathy – makemore (bigram → MLP) |
| 18 | CNN: convolution, pooling | Phân loại CIFAR-10 (local GPU) |
| 19 | Chống overfit DL: dropout, augmentation + transfer learning | Fine-tune ResNet (local GPU) |
| 20 | Attention & Transformer (trực giác + toán) | 🔥 Karpathy – **nanoGPT** (tự xây GPT mini) |
| 21 | nanoGPT (tiếp) — train & sinh văn bản | Train GPT mini trên local GPU |
| 22 | Embedding + tổng kết DL | Trực quan hóa embedding |

🎯 **DỰ ÁN 3:** (a) Phân loại ảnh transfer learning + (b) **tái hiện nanoGPT** + giải thích từng phần → GitHub.
✅ **Qua môn:** giải thích được backprop & attention bằng lời + code; train được model trên GPU local.
🔗 [Karpathy – Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) · [fast.ai](https://course.fast.ai/) · [d2l.ai](https://d2l.ai/) ([bản Việt](https://github.com/tiepvupsu/d2l-vn))

---

### 🔵 MODULE 4 — LLM & AI Engineering · Tuần 23–32 (10 tuần) ⭐⭐⭐ TRỌNG TÂM "KIẾM TIỀN"
**Mục tiêu:** xây ứng dụng AI thật bằng LLM — kỹ năng lương cao, khó tuyển ở VN.

> 📖 Đọc song song cả module: **[AI Engineering – Chip Huyen](https://github.com/chiphuyen/aie-book)** (neo khái niệm bền, không lệ thuộc framework).

| Tuần | Nội dung | Thực hành |
|---|---|---|
| 23 | Token, embedding, attention, context window (ôn từ nanoGPT) | Dùng tokenizer, quan sát token |
| 24 | Gọi API LLM (OpenAI/Gemini/open-source) + tham số | App hỏi-đáp đơn giản |
| 25 | Prompt engineering: zero/few-shot, system prompt, structured output | Bộ prompt cho 3 use-case |
| 26 | Hallucination, đánh giá output, AI-as-judge | Thử nghiệm + log so sánh |
| 27 | Embedding & vector DB (FAISS/Chroma), semantic search | Semantic search trên tài liệu |
| 28 | RAG phần 1: kiến trúc retrieval-augmented generation | Pipeline RAG với 1 PDF |
| 29 | RAG phần 2: chunking, re-ranking, đánh giá retrieval | Cải thiện độ chính xác RAG |
| 30 | Fine-tuning: LoRA/QLoRA (4-bit) | 🔥 Fine-tune model 1–3B trên RTX 4050 (4-bit) |
| 31 | Function calling / tools / agents | Agent gọi 1–2 công cụ |
| 32 | LangChain/LlamaIndex + UI (Streamlit/Gradio) + chi phí/độ trễ | Refactor chatbot + thêm UI |

🎯 **DỰ ÁN 4 (lớn nhất, "ăn tiền"):** Chatbot RAG trả lời từ tài liệu của bạn — có UI, có đo chất lượng retrieval, deploy được → GitHub + video demo.
🟢 **Mốc CTV:** từ ~tuần 26–28 (tháng 6) đủ tự tin **apply vị trí Cộng tác viên (CTV)/intern** ở công ty lớn.
✅ **Qua môn:** 1 app RAG hoạt động + giải thích được trade-off (chi phí, độ trễ, độ chính xác).
🔗 [Hugging Face LLM Course](https://huggingface.co/learn/llm-course) · [HF Agents Course](https://github.com/huggingface/agents-course) · [mlabonne/llm-course](https://github.com/mlabonne/llm-course)

---

### 🔵 MODULE 5 — MLOps, Deploy & Portfolio · Tuần 33–38 (6 tuần)
**Mục tiêu:** đưa sản phẩm lên chạy thật + portfolio gây ấn tượng.

| Tuần | Nội dung | Thực hành |
|---|---|---|
| 33 | REST API với FastAPI | Bọc Dự án 2 hoặc 4 thành API |
| 34 | Docker: image, container, Dockerfile | Đóng gói app vào Docker |
| 35 | **Experiment tracking** (MLflow / W&B) + data versioning | Track lại 1 thí nghiệm cũ |
| 36 | Deploy free: HF Spaces / Render / Railway + bảo mật API key | Đưa 1 app lên online |
| 37 | Logging, monitoring, đánh giá khi chạy thật | Thêm logging cho app |
| 38 | CI cơ bản (GitHub Actions) + README chuyên nghiệp + viết blog | Test tự động khi push |

🎯 **DỰ ÁN 5:** 1–2 sản phẩm chạy online công khai + trang portfolio (GitHub profile).
✅ **Qua môn:** ≥1 app chạy online có API + Docker + logging.
🔗 [Made With ML – Goku Mohandas](https://github.com/GokuMohandas/Made-With-ML) · [roadmap.sh/mlops](https://roadmap.sh/mlops) · [HF Spaces](https://huggingface.co/spaces)

---

### 🟣 MODULE 6 — Xin việc tại VN · Tuần 39–42 (4 tuần)
**Mục tiêu:** sẵn sàng apply CTV/intern/fresher/junior AI Engineer.

| Tuần | Nội dung | Thực hành |
|---|---|---|
| 39 | CV tech (nhấn dự án + kết quả đo được) + tối ưu LinkedIn/ITviec/TopDev | CV + hồ sơ ITviec |
| 40 | Luyện lý thuyết ML/DL/LLM (câu hỏi thường gặp) | 30 câu Q&A tự trả lời |
| 41 | Luyện coding + kể chuyện dự án ("tôi đã debug ra sao") | 2 buổi mock interview |
| 42 | Apply thật 10–15 tin | Nộp hồ sơ + theo dõi |

✅ **Tốt nghiệp:** 5 dự án GitHub, ≥1 app online, CV hoàn chỉnh, đã apply thật.

---

## 4. DÒNG THỜI GIAN & CÁC MỐC

| Mốc | Thời điểm (~17h/tuần) | Trạng thái |
|---|---|---|
| Xong nền ML cốt lõi | ~Tháng 3 | Tự code được thuật toán ML |
| Xong Deep Learning | ~Tháng 5 | Hiểu Transformer, có nanoGPT |
| **Bắt đầu apply CTV** | **~Tháng 6** | Có Dự án 1–3 + RAG cơ bản |
| Xong LLM/AI Engineering | ~Tháng 7.5 | Có chatbot RAG hoàn chỉnh |
| Xong MLOps + Portfolio | ~Tháng 9 | App chạy online |
| **Sẵn sàng junior + apply mạnh** | **~Tháng 9–10** | 5 dự án + portfolio |

> Học nhanh hơn (nhờ nền SE) có thể rút còn ~7.5–8 tháng. Bận việc trường thì giãn tới ~12 tháng — vẫn nằm trong khung "5 tháng–1 năm" bạn đặt ra.

---

## 5. SỔ TAY PHẦN CỨNG (RTX 4050 6GB + 16GB RAM)

- ✅ Làm tốt local: MNIST, CIFAR, fine-tune CNN, nanoGPT nhỏ, QLoRA 4-bit cho model 1–3B.
- ⚠️ RAM đang dùng 90% → đóng app nền khi train; cân nhắc **nâng RAM lên 32GB** sau (rẻ, hiệu quả cao).
- 🔧 Mẹo tiết kiệm VRAM 6GB: batch size nhỏ, mixed precision (`fp16`/`bf16`), gradient accumulation, quantization 4-bit (bitsandbytes).
- ☁️ Việc nặng (model lớn, fine-tune dài) → [Google Colab](https://colab.research.google.com/) / [Kaggle Notebooks](https://www.kaggle.com/code) (GPU free) hoặc thuê GPU theo giờ khi thật cần.

---

## 6. NGÂN SÁCH & CÔNG CỤ AI

- Giai đoạn đầu: **100% miễn phí** đủ dùng (mọi nguồn trên đều free/audit).
- Dùng AI làm trợ giảng: hỏi giải thích khái niệm, review code, sinh quiz ôn tập — NHƯNG **tự code tay trước**, AI chỉ để kiểm tra/giải thích.
- Cân nhắc trả phí (sau, nếu cần chứng chỉ để qua vòng lọc HR): Coursera Plus (~$399/năm) hoặc mua cert lẻ.

---

## 7. CHECKLIST DỰ ÁN PORTFOLIO (mục tiêu cuối)
- [ ] DA1 — EDA dataset thật
- [ ] DA2 — ML end-to-end (tự code thuật toán)
- [ ] DA3 — Image classifier + nanoGPT tái hiện
- [ ] DA4 — Chatbot RAG có UI + đánh giá (dự án "đinh")
- [ ] DA5 — App deploy online (API + Docker + logging)
- [ ] Trang portfolio + CV + LinkedIn/ITviec hoàn chỉnh

---

*Nguồn dữ liệu thị trường & thời lượng khóa học được tham chiếu từ: LinkedIn Jobs on the Rise 2026, WEF Future of Jobs 2025, TopCV/ITviec/VnExpress (thị trường VN), Coursera/DeepLearning.AI, fast.ai, Harvard CS50. Nội dung được tổng hợp & diễn giải lại để tuân thủ bản quyền.*


---

## 8. TỰ KIỂM TRA NUMPY (làm 15 phút trước khi vào Module 1)

Mở Jupyter, làm **không tra cứu**. Làm hết được → đi thẳng. Vấp → dành 2–3 ngày refresh (NumPy hồi phục rất nhanh, đừng lo).

```python
import numpy as np
# 1. Tạo ma trận 3x3 chứa các số từ 0 đến 8
# 2. Lấy tất cả số chẵn trong ma trận đó (boolean indexing)
# 3. Nhân 2 ma trận (dot product) — giải thích shape kết quả
# 4. Tính trung bình theo từng cột (chú ý axis)
# 5. Chuẩn hóa 1 vector: (x - mean) / std
```

**Hay quên nhất:** boolean indexing (câu 2) và `axis` (câu 4). Vấp 2 cái này là bình thường — luyện lại là nhớ ngay.

**Nguồn refresh nhanh:**
- [NumPy – the absolute basics for beginners](https://numpy.org/doc/stable/user/absolute_beginners.html)
- [rougier/numpy-100](https://github.com/rougier/numpy-100) — 100 bài tập NumPy kinh điển trên GitHub (làm 30 bài đầu là đủ ấm tay)
