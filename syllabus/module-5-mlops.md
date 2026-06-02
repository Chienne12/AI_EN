# 🔵 MODULE 5 — MLOPS, DEPLOY & PORTFOLIO (30 buổi · Tuần 33–38)

**Mục tiêu module:** đưa sản phẩm lên chạy thật (API + Docker + cloud), theo dõi thí nghiệm, monitoring, CI. Kết thúc: **Dự án 5 (App online)** + portfolio hoàn chỉnh. Đây là kỹ năng tách "người train model" khỏi **kỹ sư thực thụ**.

> Nguồn chính: [Made With ML — Goku Mohandas](https://github.com/GokuMohandas/Made-With-ML) · [FastAPI docs](https://fastapi.tiangolo.com/) · [roadmap.sh/mlops](https://roadmap.sh/mlops).

---

## TUẦN 33 — REST API với FastAPI (Buổi 1–5)

### Buổi 1 — REST API là gì
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | HTTP, method (GET/POST), request/response, JSON; vì sao model cần API. |
| ⌨️ **Bài thực hành** | Vẽ sơ đồ client → API → model. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao cần API để phục vụ model. |

### Buổi 2 — FastAPI cơ bản
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tạo endpoint, path/query param, chạy `uvicorn`, Swagger docs. |
| ⌨️ **Bài thực hành** | Viết API "hello" + 1 endpoint tính toán. |
| ✅ **Kết quả phải đạt** | Gọi được API qua trình duyệt/Swagger. |

### Buổi 3 — Pydantic & validation
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Định nghĩa schema input/output bằng Pydantic; validate dữ liệu. |
| ⌨️ **Bài thực hành** | Tạo request model có kiểm tra kiểu. |
| ✅ **Kết quả phải đạt** | API trả lỗi rõ khi input sai. |

### Buổi 4 — Phục vụ model ML
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Nạp model đã lưu (joblib/torch), tạo endpoint `/predict`. |
| ⌨️ **Bài thực hành** | Bọc model DA2 thành endpoint dự đoán. |
| ✅ **Kết quả phải đạt** | POST dữ liệu → nhận dự đoán. |

### Buổi 5 — Phục vụ ứng dụng LLM/RAG
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tạo API cho chatbot RAG (DA4); xử lý request bất đồng bộ. |
| ⌨️ **Bài thực hành** | Bọc DA4 thành API `/chat`. |
| ✅ **Kết quả phải đạt** | Gọi chatbot qua API thành công. |

---

## TUẦN 34 — Docker (Buổi 6–10)

### Buổi 6 — Container & vì sao cần
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Container vs máy ảo; "chạy được trên máy tôi" → Docker giải quyết. |
| ⌨️ **Bài thực hành** | Cài Docker, chạy `hello-world`. |
| ✅ **Kết quả phải đạt** | Giải thích lợi ích container hóa. |

### Buổi 7 — Dockerfile
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `FROM`, `COPY`, `RUN`, `CMD`; build image. |
| ⌨️ **Bài thực hành** | Viết Dockerfile cho app FastAPI. |
| ✅ **Kết quả phải đạt** | Build image thành công. |

### Buổi 8 — Chạy container
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `docker run`, port mapping, biến môi trường. |
| ⌨️ **Bài thực hành** | Chạy API trong container, truy cập từ host. |
| ✅ **Kết quả phải đạt** | API chạy trong Docker, gọi được. |

### Buổi 9 — Tối ưu image & .dockerignore
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Giảm kích thước image; layer caching; `.dockerignore`. |
| ⌨️ **Bài thực hành** | Tối ưu Dockerfile, đo lại size. |
| ✅ **Kết quả phải đạt** | Image nhỏ gọn hơn bản đầu. |

### Buổi 10 — Docker Compose (cơ bản)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chạy nhiều service (API + vector DB) bằng compose. |
| ⌨️ **Bài thực hành** | Viết `docker-compose.yml` cho app + Chroma. |
| ✅ **Kết quả phải đạt** | Khởi động nhiều service bằng 1 lệnh. |

---

## TUẦN 35 — Experiment Tracking & Versioning (Buổi 11–15)

### Buổi 11 — Vì sao cần theo dõi thí nghiệm
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vấn đề "model nào tốt, tham số gì"; reproducibility. |
| ⌨️ **Bài thực hành** | Liệt kê thứ cần log (params, metrics, artifact). |
| ✅ **Kết quả phải đạt** | Hiểu vì sao không thể nhớ thủ công. |

### Buổi 12 — MLflow / W&B
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Log params/metrics/model; so sánh runs. |
| ⌨️ **Bài thực hành** | Thêm tracking vào training DA2/DA3. |
| ✅ **Kết quả phải đạt** | Xem được bảng so sánh nhiều run. |

### Buổi 13 — Model Registry
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Quản lý phiên bản model; staging/production. |
| ⌨️ **Bài thực hành** | Đăng ký 1 model, gắn version. |
| ✅ **Kết quả phải đạt** | Nạp lại model theo version. |

### Buổi 14 — Data & code versioning
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao version cả dữ liệu (DVC khái niệm); Git cho code. |
| ⌨️ **Bài thực hành** | Tổ chức repo để tái lập thí nghiệm. |
| ✅ **Kết quả phải đạt** | Người khác chạy lại được thí nghiệm của bạn. |

### Buổi 15 — Cấu hình & reproducibility
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | File config (YAML), seed cố định, requirements khóa version. |
| ⌨️ **Bài thực hành** | Tách config ra khỏi code; cố định seed. |
| ✅ **Kết quả phải đạt** | Chạy lại ra kết quả giống nhau. |

---

## TUẦN 36 — Deploy lên Cloud (Buổi 16–20)

### Buổi 16 — Các lựa chọn deploy free
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | HF Spaces, Render, Railway; ưu/nhược; giới hạn free tier. |
| ⌨️ **Bài thực hành** | Tạo tài khoản, đọc giới hạn từng nền. |
| ✅ **Kết quả phải đạt** | Chọn nền phù hợp cho app của bạn. |

### Buổi 17 — Deploy app lên HF Spaces
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đưa app Streamlit/Gradio lên Hugging Face Spaces. |
| ⌨️ **Bài thực hành** | Deploy DA4 (chatbot RAG) lên Spaces. |
| ✅ **Kết quả phải đạt** | App truy cập được qua link công khai. |

### Buổi 18 — Deploy API (Docker) lên cloud
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Deploy container FastAPI lên Render/Railway. |
| ⌨️ **Bài thực hành** | Deploy API dự đoán DA2. |
| ✅ **Kết quả phải đạt** | API online gọi được từ internet. |

### Buổi 19 — Quản lý secrets & config production
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đặt API key qua secrets nền cloud; tách config môi trường. |
| ⌨️ **Bài thực hành** | Cấu hình secrets cho app đã deploy. |
| ✅ **Kết quả phải đạt** | App online chạy không lộ key. |

### Buổi 20 — Chi phí, độ trễ & giới hạn
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cold start, rate limit, tối ưu chi phí LLM. |
| ⌨️ **Bài thực hành** | Đo độ trễ app online, ghi nhận. |
| ✅ **Kết quả phải đạt** | Hiểu giới hạn thực tế khi chạy production. |

---

## TUẦN 37 — Logging & Monitoring (Buổi 21–25)

### Buổi 21 — Logging
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `logging` module; cấp độ log; log request/lỗi. |
| ⌨️ **Bài thực hành** | Thêm logging vào API. |
| ✅ **Kết quả phải đạt** | Xem được log request & lỗi. |

### Buổi 22 — Monitoring hiệu năng
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Theo dõi latency, throughput, lỗi; vì sao cần dashboard. |
| ⌨️ **Bài thực hành** | Ghi số liệu request theo thời gian. |
| ✅ **Kết quả phải đạt** | Biết app đang chạy nhanh/chậm. |

### Buổi 23 — Model drift & data drift
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao model "xuống cấp" theo thời gian; phát hiện drift. |
| ⌨️ **Bài thực hành** | Mô phỏng drift đơn giản trên dữ liệu. |
| ✅ **Kết quả phải đạt** | Giải thích cần giám sát model sau deploy. |

### Buổi 24 — Đánh giá LLM app khi chạy thật
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Log câu hỏi/câu trả lời; thu phản hồi người dùng. |
| ⌨️ **Bài thực hành** | Thêm log hội thoại + nút feedback. |
| ✅ **Kết quả phải đạt** | Thu được dữ liệu để cải thiện app. |

### Buổi 25 — Testing
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Unit test với pytest; test API & hàm xử lý dữ liệu. |
| ⌨️ **Bài thực hành** | Viết vài test cho API. |
| ✅ **Kết quả phải đạt** | `pytest` chạy pass. |

---

## TUẦN 38 — CI, Portfolio & DA5 (Buổi 26–30)

### Buổi 26 — CI với GitHub Actions
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Workflow tự chạy test khi push; YAML cơ bản. |
| ⌨️ **Bài thực hành** | Tạo workflow chạy `pytest` mỗi push. |
| ✅ **Kết quả phải đạt** | Badge CI xanh trên repo. |

### Buổi 27 — README chuyên nghiệp
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cấu trúc README ăn điểm: mô tả, demo, cách chạy, kết quả. |
| ⌨️ **Bài thực hành** | Viết lại README cho 5 dự án. |
| ✅ **Kết quả phải đạt** | 5 repo có README chỉn chu + ảnh/demo. |

### Buổi 28 — Viết blog kỹ thuật
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Viết 1 bài về dự án "đinh" (DA4) — vấn đề, cách giải, bài học. |
| ⌨️ **Bài thực hành** | Đăng blog (Medium/dev.to/LinkedIn). |
| ✅ **Kết quả phải đạt** | 1 bài blog công khai. |

### Buổi 29 — DA5: hoàn thiện app online
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chốt 1–2 app chạy online (API + Docker + logging). |
| ⌨️ **Bài thực hành** | Kiểm tra app online ổn định, sửa lỗi. |
| ✅ **Kết quả phải đạt** | **DA5** chạy online công khai. |

### Buổi 30 — Trang Portfolio
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tổng hợp 5 dự án vào GitHub profile/trang tĩnh. |
| ⌨️ **Bài thực hành** | Làm GitHub profile README + danh sách dự án có link. |
| ✅ **Kết quả phải đạt** | Trang portfolio hoàn chỉnh, gửi được cho NTD. |

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 5
- [ ] Bọc model thành REST API (FastAPI)
- [ ] Container hóa app bằng Docker
- [ ] Dùng experiment tracking (MLflow/W&B)
- [ ] **Deploy ≥1 app chạy online công khai**
- [ ] Có logging, test, CI (GitHub Actions)
- [ ] **DA5** + trang portfolio + 1 blog kỹ thuật

➡️ **Tiếp theo:** `module-6-job-prep.md`


---

## 📚 TÀI NGUYÊN CHI TIẾT THEO BUỔI (Hướng B)

> **📺 học chính** · **🔧 công cụ/tra cứu** · **🆘 kẹt thì hỏi đâu**. Bật phụ đề + [Immersive Translate](https://immersivetranslate.com/).
> 🏭 Xuyên suốt: [Made With ML – Goku Mohandas](https://madewithml.com/). Khóa free theo dự án: [MLOps Zoomcamp (DataTalksClub)](https://github.com/DataTalksClub/mlops-zoomcamp).

### ⚡ REST API với FastAPI (Buổi 1–5)
- 📺 [FastAPI – Tutorial chính thức](https://fastapi.tiangolo.com/tutorial/) · [freeCodeCamp – FastAPI Course (YouTube)](https://www.youtube.com/results?search_query=freecodecamp+fastapi)
- 🔧 Validation: [Pydantic docs](https://docs.pydantic.dev/)

### 🐳 Docker (Buổi 6–10)
- 📺 [Docker – Get Started](https://docs.docker.com/get-started/) · [Docker Curriculum (hands-on)](https://docker-curriculum.com/)
- 🔧 [Dockerfile reference](https://docs.docker.com/reference/dockerfile/) · [Docker Compose](https://docs.docker.com/compose/)

### 📊 Experiment Tracking (Buổi 11–15)
- 📺 [MLflow docs](https://mlflow.org/docs/latest/index.html) · [Weights & Biases docs](https://docs.wandb.ai/) · [MLOps Zoomcamp – Experiment Tracking module](https://github.com/DataTalksClub/mlops-zoomcamp)
- 🔧 Data versioning: [DVC](https://dvc.org/doc/start)

### ☁️ Deploy lên Cloud (Buổi 16–20)
- 📺 [Hugging Face Spaces docs](https://huggingface.co/docs/hub/spaces) · [Render docs](https://render.com/docs) · [Railway docs](https://docs.railway.com/)
- 🆘 Lỗi deploy → đọc build log của nền tảng + Stack Overflow

### 🔍 Logging & Monitoring (Buổi 21–25)
- 📺 [Python logging – HOWTO](https://docs.python.org/3/howto/logging.html) · Made With ML – Monitoring lesson
- 🔧 Drift: [Evidently AI](https://github.com/evidentlyai/evidently) · Test: [pytest docs](https://docs.pytest.org/)

### 🔧 CI, Portfolio & DA5 (Buổi 26–30)
- 📺 [GitHub Actions – Learn](https://docs.github.com/en/actions/learn-github-actions) · Made With ML – CI/CD
- 🔧 Portfolio: [GitHub profile README guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme) · viết blog trên [Viblo](https://viblo.asia/)/Medium/dev.to
- 🆘 [roadmap.sh/mlops](https://roadmap.sh/mlops) (xem mình còn thiếu gì)
