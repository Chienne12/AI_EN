# 🔵 MODULE 4 — LLM & AI ENGINEERING (50 buổi · Tuần 23–32)

**Mục tiêu module:** xây ứng dụng AI thật bằng LLM (prompt, RAG, agents, fine-tuning). Đây là kỹ năng lương cao, khó tuyển ở VN. Kết thúc: **Dự án 4 (Chatbot RAG)** — dự án "đinh".

> 📖 Đọc song song cả module: [AI Engineering — Chip Huyen](https://github.com/chiphuyen/aie-book) (neo khái niệm bền).
> 🟢 **Từ ~Buổi 16 (tuần 26): bắt đầu apply vị trí CTV/intern** ở công ty lớn.
> 💻 GPU RTX 4050: dùng QLoRA 4-bit để fine-tune model 1–3B; việc nặng → Colab/Kaggle.

---

## TUẦN 23 — Nền tảng LLM (Buổi 1–5)

### Buổi 1 — LLM hoạt động thế nào
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ôn lại từ nanoGPT: LLM = dự đoán token kế tiếp ở quy mô lớn; pretraining vs post-training. |
| ⌨️ **Bài thực hành** | Vẽ sơ đồ vòng đời 1 LLM. |
| ✅ **Kết quả phải đạt** | Giải thích LLM sinh văn bản dựa trên xác suất token. |

### Buổi 2 — Token & Tokenizer
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Token là gì; BPE; vì sao tính tiền theo token. |
| ⌨️ **Bài thực hành** | Dùng `tiktoken` đếm token của vài đoạn văn. |
| ✅ **Kết quả phải đạt** | Ước lượng được số token & chi phí 1 prompt. |

### Buổi 3 — Context window & giới hạn
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Context window; ảnh hưởng tới chi phí, độ trễ, khả năng nhớ. |
| ⌨️ **Bài thực hành** | Thử prompt dài/ngắn, quan sát khác biệt. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao không nhét vô hạn dữ liệu vào prompt. |

### Buổi 4 — Bức tranh hệ sinh thái model
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Closed (OpenAI/Gemini/Claude) vs open (Llama/Qwen/Mistral); khi nào dùng cái nào. |
| ⌨️ **Bài thực hành** | Lập bảng so sánh 3 model về chi phí/độ mạnh/riêng tư. |
| ✅ **Kết quả phải đạt** | Chọn được model phù hợp theo bài toán & ngân sách. |

### Buổi 5 — Tầng AI Engineering Stack
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | (theo sách Chip Huyen) 3 tầng stack; AI Eng khác ML Eng thế nào. |
| ⌨️ **Bài thực hành** | Ghi chú chương 1 sách AI Engineering. |
| ✅ **Kết quả phải đạt** | Phân biệt được vai trò AI Engineer. |

---

## TUẦN 24 — Gọi API LLM (Buổi 6–10)

### Buổi 6 — Gọi API đầu tiên
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Lấy API key; gọi API (OpenAI/Gemini); cấu trúc request/response. |
| ⌨️ **Bài thực hành** | Viết script gọi LLM trả lời 1 câu hỏi. |
| ✅ **Kết quả phải đạt** | Nhận được phản hồi từ API thành công. |

### Buổi 7 — Tham số sinh văn bản
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `temperature`, `top_p`, `max_tokens`, `stop`; ảnh hưởng tới output. |
| ⌨️ **Bài thực hành** | Đổi temperature 0 → 1.5, so sánh kết quả. |
| ✅ **Kết quả phải đạt** | Giải thích khi nào dùng temperature thấp/cao. |

### Buổi 8 — Vai trò message (system/user/assistant)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cấu trúc hội thoại nhiều lượt; system prompt định hình hành vi. |
| ⌨️ **Bài thực hành** | Tạo chatbot giữ ngữ cảnh nhiều lượt. |
| ✅ **Kết quả phải đạt** | Chatbot nhớ được hội thoại trước đó. |

### Buổi 9 — Bảo mật API key & chi phí
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | `.env`, biến môi trường; theo dõi token & chi phí. |
| ⌨️ **Bài thực hành** | Đưa key vào `.env`, không hardcode; log token mỗi call. |
| ✅ **Kết quả phải đạt** | Không lộ key trong code; ước tính chi phí. |

### Buổi 10 — Dùng model open-source local
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chạy LLM nhỏ local qua Ollama; ưu/nhược so API. |
| ⌨️ **Bài thực hành** | Cài Ollama, chạy 1 model nhỏ trên RTX 4050. |
| ✅ **Kết quả phải đạt** | Gọi được LLM local; hiểu trade-off riêng tư/chi phí. |

---

## TUẦN 25 — Prompt Engineering (Buổi 11–15)

### Buổi 11 — Zero-shot & Few-shot
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Prompt không ví dụ vs có ví dụ; vì sao few-shot tốt hơn. |
| ⌨️ **Bài thực hành** | Cùng 1 task, viết bản zero-shot & few-shot, so sánh. |
| ✅ **Kết quả phải đạt** | Thấy rõ few-shot cải thiện chất lượng. |

### Buổi 12 — System prompt & vai trò
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Thiết kế system prompt định hình phong cách, ràng buộc. |
| ⌨️ **Bài thực hành** | Viết system prompt cho 1 trợ lý chuyên ngành. |
| ✅ **Kết quả phải đạt** | Output bám đúng vai trò/định dạng yêu cầu. |

### Buổi 13 — Chain-of-thought & reasoning
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Yêu cầu model suy luận từng bước; khi nào hữu ích. |
| ⌨️ **Bài thực hành** | So bài toán logic có/không yêu cầu suy luận từng bước. |
| ✅ **Kết quả phải đạt** | Cải thiện độ chính xác bài cần suy luận. |

### Buổi 14 — Structured Output (JSON)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Bắt model trả JSON đúng schema; vì sao cần cho app. |
| ⌨️ **Bài thực hành** | Trích thông tin thành JSON từ đoạn văn. |
| ✅ **Kết quả phải đạt** | Nhận JSON hợp lệ, parse được trong code. |

### Buổi 15 — Prompt cho nhiều use-case
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tổng hợp kỹ thuật prompt; xây thư viện prompt riêng. |
| ⌨️ **Bài thực hành** | Bộ prompt cho 3 use-case (tóm tắt, phân loại, trích xuất). |
| ✅ **Kết quả phải đạt** | 3 prompt tái dùng + commit GitHub. |

---

## TUẦN 26 — Đánh giá & Hallucination (Buổi 16–20) · 🟢 BẮT ĐẦU APPLY CTV

### Buổi 16 — Hallucination
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao LLM bịa; dấu hiệu; cách hạn chế (grounding, RAG). |
| ⌨️ **Bài thực hành** | Tạo ví dụ model bịa, ghi lại. |
| ✅ **Kết quả phải đạt** | Nhận diện & giải thích hallucination. |

### Buổi 17 — Đánh giá output LLM
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Vì sao khó đánh giá; tiêu chí (đúng, liên quan, an toàn). |
| ⌨️ **Bài thực hành** | Tự chấm 10 output theo rubric. |
| ✅ **Kết quả phải đạt** | Có rubric đánh giá riêng. |

### Buổi 18 — AI as a Judge
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Dùng LLM chấm LLM; ưu/nhược & thiên lệch. |
| ⌨️ **Bài thực hành** | Viết prompt "judge" chấm câu trả lời. |
| ✅ **Kết quả phải đạt** | Pipeline chấm tự động đơn giản. |

### Buổi 19 — Cập nhật CV + apply CTV
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đưa DA1–3 vào CV; tìm tin CTV/intern AI trên ITviec/TopDev. |
| ⌨️ **Bài thực hành** | Hoàn thiện CV, nộp 3–5 tin CTV đầu tiên. |
| ✅ **Kết quả phải đạt** | Đã nộp hồ sơ thật; CV có 3 dự án. |

### Buổi 20 — Mini-project đánh giá
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp prompt + đánh giá. |
| ⌨️ **Bài thực hành** | App tóm tắt văn bản + tự đánh giá chất lượng. |
| ✅ **Kết quả phải đạt** | Notebook có log so sánh, commit. |

---

## TUẦN 27 — Embedding & Vector Search (Buổi 21–25)

### Buổi 21 — Embedding cho tìm kiếm
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ôn embedding; embedding model (vd `text-embedding`/SBERT). |
| ⌨️ **Bài thực hành** | Tạo embedding cho 10 câu. |
| ✅ **Kết quả phải đạt** | Sinh được vector embedding. |

### Buổi 22 — Cosine similarity & semantic search
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đo tương đồng; tìm câu gần nghĩa nhất. |
| ⌨️ **Bài thực hành** | Tự code semantic search bằng NumPy. |
| ✅ **Kết quả phải đạt** | Trả về câu liên quan nhất với truy vấn. |

### Buổi 23 — Vector Database
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | FAISS/Chroma; vì sao cần khi dữ liệu lớn. |
| ⌨️ **Bài thực hành** | Lưu & truy vấn embedding trong Chroma/FAISS. |
| ✅ **Kết quả phải đạt** | Index & search trên vector DB. |

### Buổi 24 — Chunking tài liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cắt tài liệu thành đoạn; chiến lược chunk & overlap. |
| ⌨️ **Bài thực hành** | Chunk 1 file PDF dài. |
| ✅ **Kết quả phải đạt** | Tạo chunk hợp lý cho truy hồi. |

### Buổi 25 — Pipeline ingest tài liệu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đọc PDF → chunk → embedding → lưu vector DB. |
| ⌨️ **Bài thực hành** | Code pipeline ingest hoàn chỉnh. |
| ✅ **Kết quả phải đạt** | Đưa được tài liệu vào vector DB tự động. |

---

## TUẦN 28 — RAG phần 1 (Buổi 26–30)

### Buổi 26 — Kiến trúc RAG
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Retrieval-Augmented Generation: retrieve → augment → generate. |
| ⌨️ **Bài thực hành** | Vẽ sơ đồ pipeline RAG. |
| ✅ **Kết quả phải đạt** | Giải thích RAG giảm hallucination thế nào. |

### Buổi 27 — RAG cơ bản (end-to-end)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ghép retrieval + prompt + LLM. |
| ⌨️ **Bài thực hành** | Hỏi-đáp trên 1 file PDF. |
| ✅ **Kết quả phải đạt** | Trả lời đúng dựa trên nội dung tài liệu. |

### Buổi 28 — Trích dẫn nguồn
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hiển thị đoạn nguồn; tăng độ tin cậy. |
| ⌨️ **Bài thực hành** | Thêm trích dẫn vào câu trả lời. |
| ✅ **Kết quả phải đạt** | Mỗi câu trả lời kèm nguồn. |

### Buổi 29 — Xử lý "không biết"
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cho model trả lời "không có trong tài liệu" thay vì bịa. |
| ⌨️ **Bài thực hành** | Thêm ràng buộc & test câu ngoài phạm vi. |
| ✅ **Kết quả phải đạt** | Model từ chối đúng khi thiếu thông tin. |

### Buổi 30 — Ôn RAG cơ bản
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Hệ thống hóa; refactor code RAG. |
| ⌨️ **Bài thực hành** | Dọn code, commit phiên bản RAG v1. |
| ✅ **Kết quả phải đạt** | RAG v1 chạy ổn định. |

---

## TUẦN 29 — RAG nâng cao (Buổi 31–35)

### Buổi 31 — Đánh giá retrieval
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Metric retrieval (recall@k, precision); vì sao quan trọng. |
| ⌨️ **Bài thực hành** | Tạo bộ câu hỏi-đáp mẫu, đo recall@k. |
| ✅ **Kết quả phải đạt** | Có số đo chất lượng truy hồi. |

### Buổi 32 — Re-ranking
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Sắp xếp lại kết quả bằng reranker; cải thiện độ chính xác. |
| ⌨️ **Bài thực hành** | Thêm reranker, so recall trước/sau. |
| ✅ **Kết quả phải đạt** | Cải thiện chất lượng đoạn truy hồi. |

### Buổi 33 — Hybrid search
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Kết hợp keyword (BM25) + vector. |
| ⌨️ **Bài thực hành** | Thử hybrid search. |
| ✅ **Kết quả phải đạt** | Hiểu khi nào hybrid tốt hơn vector thuần. |

### Buổi 34 — Tối ưu chunking & prompt RAG
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Thử kích thước chunk, overlap, prompt template khác nhau. |
| ⌨️ **Bài thực hành** | A/B vài cấu hình, ghi kết quả. |
| ✅ **Kết quả phải đạt** | Chọn cấu hình tốt nhất có số liệu. |

### Buổi 35 — RAG v2 hoàn chỉnh
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Ráp các cải tiến thành RAG v2. |
| ⌨️ **Bài thực hành** | Hoàn thiện + đo lại chất lượng. |
| ✅ **Kết quả phải đạt** | RAG v2 tốt hơn v1 (có số chứng minh). |

---

## TUẦN 30 — Fine-tuning (Buổi 36–40)

### Buổi 36 — Khi nào fine-tune vs RAG vs prompt
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | (theo Chip Huyen) chọn đúng kỹ thuật theo bài toán. |
| ⌨️ **Bài thực hành** | Lập cây quyết định "prompt/RAG/fine-tune". |
| ✅ **Kết quả phải đạt** | Chọn đúng phương án cho 3 tình huống. |

### Buổi 37 — LoRA & QLoRA (lý thuyết)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Parameter-efficient fine-tuning; QLoRA 4-bit tiết kiệm VRAM. |
| ⌨️ **Bài thực hành** | Ghi chú cơ chế LoRA. |
| ✅ **Kết quả phải đạt** | Giải thích vì sao QLoRA chạy được trên 6GB. |

### Buổi 38 — Chuẩn bị dữ liệu fine-tune
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Định dạng dữ liệu instruction; chất lượng > số lượng. |
| ⌨️ **Bài thực hành** | Tạo dataset nhỏ (vài trăm mẫu) cho 1 tác vụ. |
| ✅ **Kết quả phải đạt** | Dataset đúng định dạng. |

### Buổi 39 — Fine-tune QLoRA (GPU)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Fine-tune model 1–3B bằng QLoRA 4-bit (PEFT). |
| ⌨️ **Bài thực hành** | Chạy fine-tune trên RTX 4050 (hoặc Colab nếu thiếu VRAM). |
| ✅ **Kết quả phải đạt** | Hoàn thành 1 lần fine-tune; loss giảm. |

### Buổi 40 — Đánh giá model fine-tuned
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | So model gốc vs fine-tuned; tránh overfit. |
| ⌨️ **Bài thực hành** | Đánh giá trên tập test giữ riêng. |
| ✅ **Kết quả phải đạt** | Kết luận fine-tune có cải thiện hay không. |

---

## TUẦN 31 — Tools & Agents (Buổi 41–45)

### Buổi 41 — Function calling
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Cho LLM gọi hàm/công cụ; schema tool. |
| ⌨️ **Bài thực hành** | Cho model gọi 1 hàm thời tiết/tính toán. |
| ✅ **Kết quả phải đạt** | Model chọn & gọi đúng tool. |

### Buổi 42 — Khái niệm Agent
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Agent = LLM + lập kế hoạch + công cụ + bộ nhớ; vòng lặp reasoning-action. |
| ⌨️ **Bài thực hành** | Theo [HF Agents Course](https://github.com/huggingface/agents-course) unit 1. |
| ✅ **Kết quả phải đạt** | Giải thích agent ra quyết định thế nào. |

### Buổi 43 — Agent nhiều công cụ
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Agent chọn giữa nhiều tool; xử lý lỗi tool. |
| ⌨️ **Bài thực hành** | Agent gọi 2–3 công cụ (search + calc). |
| ✅ **Kết quả phải đạt** | Agent hoàn thành tác vụ nhiều bước. |

### Buổi 44 — Bộ nhớ & trạng thái
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Memory ngắn/dài hạn cho agent. |
| ⌨️ **Bài thực hành** | Thêm bộ nhớ hội thoại cho agent. |
| ✅ **Kết quả phải đạt** | Agent nhớ ngữ cảnh qua nhiều lượt. |

### Buổi 45 — An toàn & giới hạn agent
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Rủi ro agent; đặt giới hạn, guardrails. |
| ⌨️ **Bài thực hành** | Thêm ràng buộc an toàn cho agent. |
| ✅ **Kết quả phải đạt** | Agent có guardrails cơ bản. |

---

## TUẦN 32 — Framework, UI & DA4 (Buổi 46–50)

### Buổi 46 — LangChain / LlamaIndex
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Framework ghép pipeline nhanh; coi là công cụ (đã hiểu khái niệm gốc). |
| ⌨️ **Bài thực hành** | Refactor RAG v2 sang LangChain/LlamaIndex. |
| ✅ **Kết quả phải đạt** | RAG chạy lại bằng framework, gọn hơn. |

### Buổi 47 — Giao diện (Streamlit/Gradio)
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Tạo UI chat đơn giản. |
| ⌨️ **Bài thực hành** | Bọc chatbot RAG bằng Streamlit. |
| ✅ **Kết quả phải đạt** | Chat qua giao diện web local. |

### Buổi 48 — DA4: xây dựng
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Chatbot RAG trả lời từ tài liệu của bạn (PDF/web). |
| ⌨️ **Bài thực hành** | Ghép ingest + RAG v2 + UI. |
| ✅ **Kết quả phải đạt** | App chạy đầu-cuối local. |

### Buổi 49 — DA4: đánh giá & tối ưu
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | Đo chất lượng retrieval/câu trả lời; tối ưu chi phí & độ trễ. |
| ⌨️ **Bài thực hành** | Thêm bảng đánh giá + ghi chi phí/độ trễ. |
| ✅ **Kết quả phải đạt** | Có số liệu đánh giá rõ ràng. |

### Buổi 50 — DA4: hoàn thiện & demo
| | |
|---|---|
| 🎯 **Mục tiêu & Nội dung** | README chuyên nghiệp + video demo. |
| ⌨️ **Bài thực hành** | Quay demo, viết README, push GitHub. |
| ✅ **Kết quả phải đạt** | **DA4 (dự án đinh)** hoàn chỉnh vào portfolio. |

---

## ✅ TIÊU CHÍ HOÀN THÀNH MODULE 4
- [ ] Gọi API LLM + prompt engineering thành thạo
- [ ] Hiểu & hạn chế hallucination, biết đánh giá output
- [ ] Xây được RAG end-to-end + đánh giá retrieval
- [ ] Fine-tune QLoRA 1 model (local hoặc Colab)
- [ ] Xây được agent dùng công cụ
- [ ] **DA4 (Chatbot RAG)** có UI + đánh giá + demo
- [ ] **Đã apply CTV/intern** thật

➡️ **Tiếp theo:** `module-5-mlops.md`


---

## 📚 TÀI NGUYÊN CHI TIẾT THEO BUỔI (Hướng B)

> **📺 học chính** · **🔧 công cụ/tra cứu** · **🆘 kẹt thì hỏi đâu**. Bật phụ đề + [Immersive Translate](https://immersivetranslate.com/).
> 📖 Đọc xuyên suốt: [AI Engineering – Chip Huyen](https://github.com/chiphuyen/aie-book). Khóa ngắn miễn phí cực hợp: [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/).

### 🧩 Nền tảng LLM (Buổi 1–5)
- 📺 [HF LLM Course – Chapter 1](https://huggingface.co/learn/llm-course) · [3B1B – "But what is a GPT?"](https://www.3blue1brown.com/topics/neural-networks)
- 📖 Chip Huyen ch.1–2 (AI Engineering stack, foundation models)
- 🔧 Đếm token: [tiktoken](https://github.com/openai/tiktoken)

### 🔌 Gọi API LLM (Buổi 6–10)
- 📺 [DeepLearning.AI – Building Systems with the ChatGPT API](https://www.deeplearning.ai/short-courses/) · [OpenAI – Quickstart](https://platform.openai.com/docs/quickstart)
- 🔧 Model local: [Ollama](https://ollama.com/) (chạy LLM nhỏ trên RTX 4050)
- 🆘 Bảo mật key: dùng `.env` + `python-dotenv`

### ✍️ Prompt Engineering (Buổi 11–15)
- 📺 [DeepLearning.AI – ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)
- 🔧 [Prompt Engineering Guide](https://www.promptingguide.ai/) · [OpenAI – Prompt engineering](https://platform.openai.com/docs/guides/prompt-engineering)

### 🧪 Đánh giá & Hallucination (Buổi 16–20) · 🟢 APPLY CTV
- 📖 Chip Huyen ch.3–4 (evaluation methodology, AI as a judge)
- 📺 [DeepLearning.AI – Evaluating and Debugging GenAI](https://www.deeplearning.ai/short-courses/)
- 🟢 Apply CTV: [ITviec](https://itviec.com/) · [TopDev](https://topdev.vn/) (lọc "AI/ML Intern/Fresher/CTV")

### 🔎 Embedding & Vector Search (Buổi 21–25)
- 📺 [Sentence-Transformers (SBERT) docs](https://www.sbert.net/) · HF LLM Course (semantic search)
- 🔧 Vector DB: [Chroma](https://docs.trychroma.com/) · [FAISS](https://github.com/facebookresearch/faiss)

### 📚 RAG phần 1 (Buổi 26–30)
- 📺 [DeepLearning.AI – LangChain: Chat with Your Data](https://www.deeplearning.ai/short-courses/langchain-chat-with-your-data/)
- 🔧 [LlamaIndex docs](https://docs.llamaindex.ai/) · [LangChain – RAG](https://python.langchain.com/docs/tutorials/rag/)

### 🚀 RAG nâng cao (Buổi 31–35)
- 📺 [DeepLearning.AI – Building and Evaluating Advanced RAG](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)
- 🔧 Đánh giá RAG: [Ragas](https://github.com/explodinggradients/ragas)

### 🎛️ Fine-tuning (Buổi 36–40)
- 📺 [DeepLearning.AI – Finetuning LLMs](https://www.deeplearning.ai/short-courses/finetuning-large-language-models/) · [mlabonne/llm-course – Fine-tuning notebooks](https://github.com/mlabonne/llm-course)
- 🔧 [HF PEFT (LoRA/QLoRA)](https://github.com/huggingface/peft) · 🔥 [Unsloth](https://github.com/unslothai/unsloth) (fine-tune tiết kiệm VRAM — hợp RTX 4050 6GB)
- 💻 Thiếu VRAM → fine-tune trên [Kaggle/Colab GPU free]

### 🛠️ Tools & Agents (Buổi 41–45)
- 📺 [HF Agents Course](https://huggingface.co/learn/agents-course) · [DeepLearning.AI – Functions, Tools and Agents with LangChain](https://www.deeplearning.ai/short-courses/)
- 🔧 [LangChain – Agents](https://python.langchain.com/docs/concepts/agents/)

### 🖥️ Framework, UI & DA4 (Buổi 46–50)
- 📺 [LangChain docs](https://python.langchain.com/) · [LlamaIndex docs](https://docs.llamaindex.ai/)
- 🔧 UI: [Streamlit](https://docs.streamlit.io/) · [Gradio](https://www.gradio.app/docs)
- 🆘 [Hugging Face Discord](https://discord.gg/huggingface) · [LangChain Discord]
