# 🟡 MODULE 3 — DEEP LEARNING TỪ GỐC (45 buổi · Tuần 14–22)

**Mục tiêu module:** hiểu & huấn luyện mạng nơ-ron, làm chủ PyTorch, hiểu Transformer từ số 0 (tự xây nanoGPT). Kết thúc: **Dự án 3 (Image classifier + nanoGPT)**.

> Nguồn chính: 🔥 [Karpathy – Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) · [fast.ai](https://course.fast.ai/) · tra cứu [d2l.ai](https://d2l.ai/) ([bản Việt](https://github.com/tiepvupsu/d2l-vn)).
> 💻 GPU RTX 4050: dùng cho MNIST, CIFAR, nanoGPT nhỏ. Mẹo: batch nhỏ + mixed precision khi thiếu VRAM.

---

## TUẦN 14 — Nơ-ron & Forward Pass (Buổi 1–5)

### Buổi 1 — Từ hồi quy logistic đến nơ-ron
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | 1 nơ-ron = logistic regression; trọng số, bias, hàm kích hoạt. |
| ⌨️ **Bài thực hành** | Vẽ sơ đồ 1 nơ-ron; tính output bằng tay. |
| ✅ **Kết quả phải đạt** | Giải thích nơ-ron liên hệ với cái đã học ở Module 2. |

### Buổi 2 — Hàm kích hoạt
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Sigmoid, tanh, ReLU; vì sao cần phi tuyến. |
| ⌨️ **Bài thực hành** | Vẽ 3 hàm kích hoạt bằng NumPy. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao không có activation thì mạng = tuyến tính. |

### Buổi 3 — Mạng nhiều lớp (MLP)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Layer, hidden layer, forward pass; biểu diễn ma trận. |
| ⌨️ **Bài thực hành** | Code forward pass 1 mạng 2 lớp bằng NumPy. |
| ✅ **Kết quả phải đạt** | Tính được output mạng 2 lớp từ input. |

### Buổi 4 — Hàm mất mát & ý tưởng học
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Loss cho mạng; vì sao cần đạo hàm để học. |
| ⌨️ **Bài thực hành** | Tính loss cho mạng forward ở buổi 3. |
| ✅ **Kết quả phải đạt** | Hiểu mục tiêu: tối thiểu hóa loss qua điều chỉnh trọng số. |

### Buổi 5 — Tổng hợp + chuẩn bị backprop
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ôn chain rule (đạo hàm hàm hợp) — nền tảng backprop. |
| ⌨️ **Bài thực hành** | Bài tập chain rule bằng tay (3B1B). |
| ✅ **Kết quả phải đạt** | Tính được đạo hàm hàm hợp đơn giản. |

---

## TUẦN 15 — Backpropagation + micrograd (Buổi 6–10)

### Buổi 6 — Karpathy micrograd (phần 1)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Xem & code theo: đối tượng `Value`, đồ thị tính toán. |
| ⌨️ **Bài thực hành** | Code class `Value` (cộng, nhân) theo Karpathy. |
| ✅ **Kết quả phải đạt** | Tạo được đồ thị tính toán đơn giản. |

### Buổi 7 — micrograd: backward
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Lan truyền ngược gradient qua đồ thị; `.backward()`. |
| ⌨️ **Bài thực hành** | Cài `backward()` cho từng phép toán. |
| ✅ **Kết quả phải đạt** | Gradient tự tính khớp với đạo hàm tay. |

### Buổi 8 — micrograd: nơ-ron & MLP
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Dựng `Neuron`, `Layer`, `MLP` trên micrograd. |
| ⌨️ **Bài thực hành** | Train MLP nhỏ giải bài phân loại 2D. |
| ✅ **Kết quả phải đạt** | **Tự xây xong autograd engine** + MLP học được. |

### Buổi 9 — Hiểu sâu gradient
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vanishing/exploding gradient; vai trò learning rate. |
| ⌨️ **Bài thực hành** | Thử learning rate khác nhau, quan sát loss. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao chọn lr quan trọng. |

### Buổi 10 — Ôn & ghi chú backprop
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hệ thống hóa backprop bằng lời + sơ đồ. |
| ⌨️ **Bài thực hành** | Viết blog ngắn "Backprop bằng tiếng Việt dễ hiểu". |
| ✅ **Kết quả phải đạt** | Giải thích backprop cho người khác hiểu; push GitHub. |

---

## TUẦN 16 — PyTorch + MNIST (Buổi 11–15)

### Buổi 11 — Tensor & Autograd PyTorch
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `torch.tensor`, GPU tensor, `requires_grad`, `.backward()`. |
| ⌨️ **Bài thực hành** | Lặp lại ví dụ micrograd nhưng bằng PyTorch autograd. |
| ✅ **Kết quả phải đạt** | Tính gradient tự động bằng PyTorch trên GPU. |

### Buổi 12 — nn.Module & Optimizer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Định nghĩa model bằng `nn.Module`; `optim.SGD/Adam`; `loss.backward()` + `optimizer.step()`. |
| ⌨️ **Bài thực hành** | Viết 1 MLP bằng `nn.Module`. |
| ✅ **Kết quả phải đạt** | Hiểu vòng lặp huấn luyện chuẩn PyTorch. |

### Buổi 13 — Dataset & DataLoader
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `Dataset`, `DataLoader`, batch, shuffle. |
| ⌨️ **Bài thực hành** | Tải MNIST qua `torchvision`, tạo DataLoader. |
| ✅ **Kết quả phải đạt** | Lặp qua batch dữ liệu đúng. |

### Buổi 14 — Train MNIST (GPU)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vòng lặp train đầy đủ: forward → loss → backward → step; chuyển dữ liệu lên `.cuda()`. |
| ⌨️ **Bài thực hành** | Train MLP phân loại chữ số MNIST trên RTX 4050. |
| ✅ **Kết quả phải đạt** | Accuracy test >95%; train chạy trên GPU. |

### Buổi 15 — Đánh giá & lưu model
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Train/val loss curve; `torch.save`/`load`; chế độ `eval()`. |
| ⌨️ **Bài thực hành** | Vẽ loss curve + lưu/nạp lại model. |
| ✅ **Kết quả phải đạt** | Phát hiện overfit qua loss curve; nạp lại model dự đoán. |

---

## TUẦN 17 — Mô hình ngôn ngữ (makemore) (Buổi 16–20)

### Buổi 16 — Bigram model
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Karpathy makemore: mô hình ký tự bigram; xác suất ký tự kế tiếp. |
| ⌨️ **Bài thực hành** | Code bigram sinh tên. |
| ✅ **Kết quả phải đạt** | Sinh được chuỗi ký tự theo xác suất. |

### Buổi 17 — MLP ngôn ngữ
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Mô hình ngôn ngữ bằng MLP (theo bài Bengio). |
| ⌨️ **Bài thực hành** | Train MLP dự đoán ký tự kế tiếp. |
| ✅ **Kết quả phải đạt** | Loss giảm; sinh tên hợp lý hơn bigram. |

### Buổi 18 — Embedding ký tự
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Khái niệm embedding; biểu diễn token thành vector. |
| ⌨️ **Bài thực hành** | Trực quan hóa embedding ký tự đã học. |
| ✅ **Kết quả phải đạt** | Giải thích embedding là gì & vì sao hữu ích. |

### Buổi 19 — BatchNorm & mẹo huấn luyện
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Khởi tạo trọng số, BatchNorm, ổn định huấn luyện (theo Karpathy). |
| ⌨️ **Bài thực hành** | Thêm BatchNorm, so sánh hội tụ. |
| ✅ **Kết quả phải đạt** | Hiểu vì sao khởi tạo & chuẩn hóa giúp train tốt hơn. |

### Buổi 20 — Ôn tập tuần ngôn ngữ
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tổng hợp makemore; chuẩn bị cho attention. |
| ⌨️ **Bài thực hành** | Refactor code makemore gọn gàng, commit. |
| ✅ **Kết quả phải đạt** | Code sạch + hiểu pipeline mô hình ngôn ngữ. |

---

## TUẦN 18 — CNN (Buổi 21–25)

### Buổi 21 — Convolution là gì
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Phép tích chập, kernel/filter, feature map; vì sao tốt cho ảnh. |
| ⌨️ **Bài thực hành** | Áp dụng filter thủ công lên 1 ảnh (phát hiện cạnh). |
| ✅ **Kết quả phải đạt** | Giải thích convolution trích đặc trưng thế nào. |

### Buổi 22 — Pooling & kiến trúc CNN
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Max/Average pooling; stack conv→pool→fc. |
| ⌨️ **Bài thực hành** | Vẽ kiến trúc 1 CNN nhỏ. |
| ✅ **Kết quả phải đạt** | Mô tả luồng dữ liệu qua CNN. |

### Buổi 23 — CNN trên PyTorch
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `nn.Conv2d`, `nn.MaxPool2d`; xây CNN. |
| ⌨️ **Bài thực hành** | Code 1 CNN cho ảnh. |
| ✅ **Kết quả phải đạt** | CNN forward chạy đúng shape. |

### Buổi 24 — Train CIFAR-10 (GPU)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Train CNN phân loại 10 lớp ảnh màu. |
| ⌨️ **Bài thực hành** | Train trên RTX 4050; theo dõi accuracy. |
| ✅ **Kết quả phải đạt** | Accuracy hợp lý (>70%); train trên GPU ổn định. |

### Buổi 25 — Phân tích lỗi CNN
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Xem ảnh bị nhầm; confusion matrix cho ảnh. |
| ⌨️ **Bài thực hành** | Hiển thị các ảnh model đoán sai. |
| ✅ **Kết quả phải đạt** | Đưa giả thuyết vì sao model nhầm. |

---

## TUẦN 19 — Transfer Learning & chống overfit (Buổi 26–30)

### Buổi 26 — Dropout
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Dropout chống overfit trong DL. |
| ⌨️ **Bài thực hành** | Thêm dropout, so loss curve. |
| ✅ **Kết quả phải đạt** | Giảm khoảng cách train/val loss. |

### Buổi 27 — Data Augmentation
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Lật/xoay/cắt ảnh để tăng dữ liệu. |
| ⌨️ **Bài thực hành** | Áp dụng augmentation cho CIFAR. |
| ✅ **Kết quả phải đạt** | Cải thiện accuracy/giảm overfit. |

### Buổi 28 — Transfer Learning (lý thuyết)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Dùng model pretrained (ResNet); freeze/fine-tune. |
| ⌨️ **Bài thực hành** | Tải ResNet pretrained từ torchvision. |
| ✅ **Kết quả phải đạt** | Hiểu vì sao transfer learning tiết kiệm dữ liệu & thời gian. |

### Buổi 29 — Fine-tune ResNet (GPU)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Fine-tune model pretrained cho bài toán riêng (vd chó/mèo). |
| ⌨️ **Bài thực hành** | Fine-tune ResNet trên dataset nhỏ. |
| ✅ **Kết quả phải đạt** | Accuracy cao hơn train từ đầu; chạy GPU. |

### Buổi 30 — Tổng kết thị giác máy tính
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hệ thống hóa CNN + transfer learning. |
| ⌨️ **Bài thực hành** | Hoàn thiện notebook image classifier (phần a của DA3). |
| ✅ **Kết quả phải đạt** | Image classifier transfer learning + so ≥2 cấu hình. |

---

## TUẦN 20 — Attention & Transformer (Buổi 31–35)

### Buổi 31 — Hạn chế của mô hình tuần tự
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao cần attention; ý tưởng "chú ý" vào token liên quan. |
| ⌨️ **Bài thực hành** | Đọc & tóm tắt trực giác attention. |
| ✅ **Kết quả phải đạt** | Giải thích attention bằng lời. |

### Buổi 32 — Self-Attention (toán)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Query, Key, Value; công thức attention; scaled dot-product. |
| ⌨️ **Bài thực hành** | Tính attention cho 1 ví dụ nhỏ bằng NumPy. |
| ✅ **Kết quả phải đạt** | Tính được ma trận attention từ Q,K,V. |

### Buổi 33 — Multi-Head Attention
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Nhiều "đầu" attention; vì sao đa đầu mạnh hơn. |
| ⌨️ **Bài thực hành** | Code multi-head attention đơn giản. |
| ✅ **Kết quả phải đạt** | Hiểu vai trò nhiều head. |

### Buổi 34 — Kiến trúc Transformer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Positional encoding, residual, layernorm, feed-forward. |
| ⌨️ **Bài thực hành** | Vẽ sơ đồ 1 block Transformer. |
| ✅ **Kết quả phải đạt** | Mô tả luồng dữ liệu qua 1 block. |

### Buổi 35 — Ôn tập Transformer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hệ thống hóa các thành phần trước khi xây nanoGPT. |
| ⌨️ **Bài thực hành** | Ghi chú/sơ đồ tổng hợp; commit. |
| ✅ **Kết quả phải đạt** | Sẵn sàng đọc code nanoGPT không bỡ ngỡ. |

---

## TUẦN 21 — Xây nanoGPT (Buổi 36–40)

### Buổi 36 — nanoGPT: dữ liệu & tokenizer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chuẩn bị dữ liệu văn bản, tokenizer ký tự, batch. |
| ⌨️ **Bài thực hành** | Code phần dữ liệu theo Karpathy. |
| ✅ **Kết quả phải đạt** | Tạo batch (x,y) đúng cho mô hình ngôn ngữ. |

### Buổi 37 — nanoGPT: attention block
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cài self-attention + multi-head trong GPT. |
| ⌨️ **Bài thực hành** | Code block attention. |
| ✅ **Kết quả phải đạt** | Block forward đúng shape. |

### Buổi 38 — nanoGPT: ghép mô hình
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Stack nhiều block + embedding + head dự đoán. |
| ⌨️ **Bài thực hành** | Hoàn thiện class GPT. |
| ✅ **Kết quả phải đạt** | Mô hình forward ra logits đúng. |

### Buổi 39 — nanoGPT: train (GPU)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Train GPT mini trên RTX 4050 (batch nhỏ, mixed precision). |
| ⌨️ **Bài thực hành** | Train tới khi loss giảm rõ. |
| ✅ **Kết quả phải đạt** | Loss giảm; train không tràn VRAM. |

### Buổi 40 — nanoGPT: sinh văn bản
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hàm `generate`; sampling (temperature). |
| ⌨️ **Bài thực hành** | Sinh văn bản từ model đã train. |
| ✅ **Kết quả phải đạt** | **GPT mini tự xây sinh được văn bản** giống dữ liệu train. |

---

## TUẦN 22 — Embedding, Tổng kết & DA3 (Buổi 41–45)

### Buổi 41 — Embedding & không gian vector
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Embedding từ/câu; độ tương đồng cosine (nền cho RAG ở Module 4). |
| ⌨️ **Bài thực hành** | Tính cosine similarity giữa các embedding. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao embedding gần nhau = nghĩa gần nhau. |

### Buổi 42 — Giải thích nanoGPT bằng lời
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Trình bày lại từng phần GPT đã xây. |
| ⌨️ **Bài thực hành** | Viết README giải thích nanoGPT của bạn. |
| ✅ **Kết quả phải đạt** | Giải thích được mọi dòng chính trong code. |

### Buổi 43 — DA3: hoàn thiện Image Classifier
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chốt phần (a) của DA3. |
| ⌨️ **Bài thực hành** | Dọn code, viết README, so sánh cấu hình. |
| ✅ **Kết quả phải đạt** | Repo image classifier chỉn chu. |

### Buổi 44 — DA3: hoàn thiện nanoGPT
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chốt phần (b) của DA3. |
| ⌨️ **Bài thực hành** | Đẩy code nanoGPT + README + ví dụ sinh văn bản. |
| ✅ **Kết quả phải đạt** | Repo nanoGPT chạy lại được + demo. |

### Buổi 45 — Tổng kết Module 3
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Nhìn lại toàn bộ DL; tự đánh giá điểm yếu cần ôn. |
| ⌨️ **Bài thực hành** | Cập nhật portfolio với DA3; viết post LinkedIn. |
| ✅ **Kết quả phải đạt** | **DA3 vào portfolio**; sẵn sàng sang LLM/AI Engineering. |

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 3
- [ ] Tự xây autograd (micrograd) + giải thích backprop
- [ ] Thành thạo vòng lặp huấn luyện PyTorch trên GPU
- [ ] Train được CNN + transfer learning (ResNet)
- [ ] Hiểu & **tự xây nanoGPT**, sinh được văn bản
- [ ] Hiểu embedding & cosine similarity (nền cho RAG)
- [ ] **DA3** trên GitHub (image classifier + nanoGPT)

➡️ **Tiếp theo:** `module-4-llm-ai-eng.md`


---

## 📚 TÀI NGUYÊN CHI TIẾT THEO BUỔI (Hướng B)

> **📺 học chính** · **🇻🇳 bổ trợ** · **🔧 tra cứu** · **🆘 kẹt thì hỏi đâu**. Bật phụ đề + [Immersive Translate](https://immersivetranslate.com/).
> 🔥 Cột sống module: [Karpathy – Zero to Hero](https://karpathy.ai/zero-to-hero.html). Bổ trợ trực giác: [3Blue1Brown – Neural Networks](https://www.3blue1brown.com/topics/neural-networks).

### 🧠 Nơ-ron & Forward (Buổi 1–5)
- 📺 [3B1B – Neural Networks ch.1–2](https://www.3blue1brown.com/topics/neural-networks) · [Andrew Ng – Deep Learning Specialization, Course 1](https://www.coursera.org/specializations/deep-learning)
- 📺 StatQuest: "Neural Networks Part 1: Inside the Black Box"
- 🔧 Ôn chain rule: [3B1B – Calculus ch.4](https://www.3blue1brown.com/topics/calculus)

### 🔁 Backprop + micrograd (Buổi 6–10)
- 📺 🔥 Karpathy: "The spelled-out intro to neural networks and backpropagation: building micrograd" · [3B1B – Backpropagation](https://www.3blue1brown.com/topics/neural-networks)
- 🔧 Repo: [karpathy/micrograd](https://github.com/karpathy/micrograd) (đối chiếu code)
- 🆘 [PyTorch Forums](https://discuss.pytorch.org/)

### 🔥 PyTorch + MNIST (Buổi 11–15)
- 📺 [PyTorch – Learn the Basics](https://pytorch.org/tutorials/beginner/basics/intro.html) · [Deep Learning with PyTorch: A 60 Minute Blitz](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)
- 🇻🇳 [d2l tiếng Việt](https://github.com/tiepvupsu/d2l-vn)
- 🔧 [PyTorch cheat sheet](https://pytorch.org/tutorials/beginner/ptcheat.html)

### 🔤 makemore (Buổi 16–20)
- 📺 🔥 Karpathy makemore: "building makemore" Part 1–4 (bigram → MLP → BatchNorm)
- 🔧 Repo: [karpathy/makemore](https://github.com/karpathy/makemore)

### 🖼️ CNN (Buổi 21–25)
- 📺 Andrew Ng DLS Course 4 (CNN) · [CS231n notes](https://cs231n.github.io/) · [fast.ai](https://course.fast.ai/)
- 📺 StatQuest: "Convolutional Neural Networks (CNNs) Explained"
- 🎯 Dataset: CIFAR-10 (torchvision), [Dogs vs Cats](https://www.kaggle.com/c/dogs-vs-cats)

### 🔁 Transfer Learning (Buổi 26–30)
- 📺 [PyTorch – Transfer Learning Tutorial](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html) · Andrew Ng DLS C4 (tuần transfer learning)
- 🔧 [torchvision models (pretrained)](https://pytorch.org/vision/stable/models.html)

### 🎯 Attention & Transformer (Buổi 31–35)
- 📺 [Jay Alammar – The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) · [3B1B – "But what is a GPT?" & "Attention in transformers"](https://www.3blue1brown.com/topics/neural-networks)
- 📺 Andrew Ng DLS Course 5 (Sequence models, attention)
- 🔧 [The Annotated Transformer (Harvard)](https://nlp.seas.harvard.edu/annotated-transformer/)

### 🤖 nanoGPT (Buổi 36–40)
- 📺 🔥 Karpathy: "Let's build GPT: from scratch, in code, spelled out"
- 🔧 Repo: [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) · [karpathy/ng-video-lecture](https://github.com/karpathy/ng-video-lecture)
- 💻 GPU: batch nhỏ + `torch.cuda.amp` (mixed precision) để vừa 6GB VRAM

### 📐 Embedding & Tổng kết + DA3 (Buổi 41–45)
- 📺 [Jay Alammar – The Illustrated Word2Vec](https://jalammar.github.io/illustrated-word2vec/)
- 🆘 Lý thuyết DL → [r/learnmachinelearning](https://www.reddit.com/r/learnmachinelearning/); code → [PyTorch Forums](https://discuss.pytorch.org/)
