# 🧰 TÀI NGUYÊN BỔ TRỢ (luôn mở cạnh bàn học)

> File tổng hợp mọi nguồn dùng chung cho cả lộ trình. Các link cụ thể **theo từng buổi** nằm ở cuối mỗi file trong [`syllabus/`](./syllabus/).
> Hồ sơ người học: thích toán & suy luận · nghe tiếng Anh yếu (đọc OK) · GPU RTX 4050 6GB · mục tiêu LLM/AI Engineering.

---

## 1. 📚 Sách nền (ưu tiên miễn phí)
| Sách | Dùng cho | Link |
|---|---|---|
| Introduction to Statistical Learning (ISLR) | ML có toán vừa phải, kinh điển | [statlearning.com](https://www.statlearning.com/) (PDF free) |
| Mathematics for ML | Toán đúng cho ML | [mml-book.github.io](https://mml-book.github.io/) (PDF free) |
| Deep Learning Book (Goodfellow) | Tra cứu lý thuyết DL | [deeplearningbook.org](https://www.deeplearningbook.org/) (free) |
| Dive into Deep Learning (d2l) | DL code+toán tương tác | [d2l.ai](https://d2l.ai/) · [bản Việt](https://github.com/tiepvupsu/d2l-vn) |
| Hands-On ML (Géron) | Thực hành sklearn + Keras | nên mua (rất đáng) |
| AI Engineering (Chip Huyen) | Xây app foundation models | [aie-book](https://github.com/chiphuyen/aie-book) |
| ML Interviews Book (Chip Huyen) | Ôn phỏng vấn | [huyenchip.com/ml-interviews-book](https://huyenchip.com/ml-interviews-book/) (free) |

## 2. 📺 Kênh YouTube "vàng" (đều có phụ đề)
- **[StatQuest](https://www.youtube.com/@statquest)** — giải thích bản chất ML cực rõ (hợp người thích hiểu sâu).
- **[Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy)** — Zero to Hero (micrograd → nanoGPT).
- **[3Blue1Brown](https://www.youtube.com/@3blue1brown)** — trực giác toán & neural network/transformer.
- **[Corey Schafer](https://www.youtube.com/@coreyms)** — Python/Pandas/Git nền tảng.
- **[fast.ai](https://course.fast.ai/)** — DL thực chiến top-down.

## 3. 📑 Cheat sheets (in ra dán bàn)
- [Stanford CS229 ML cheatsheets](https://github.com/afshinea/stanford-cs-229-machine-learning)
- [NumPy](https://images.datacamp.com/image/upload/v1676302459/Marketing/Blog/Numpy_Cheat_Sheet.pdf) · [Pandas (chính thức)](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf) · [Matplotlib](https://matplotlib.org/cheatsheets/) · [PyTorch](https://pytorch.org/tutorials/beginner/ptcheat.html) · [Git](https://education.github.com/git-cheat-sheet-education.pdf)

## 4. 🇻🇳 Nguồn tiếng Việt (giàn giáo lúc khó)
- [machinelearningcoban.com](https://machinelearningcoban.com/) — toán ML tiếng Việt (Vũ Hữu Tiệp).
- [Viblo](https://viblo.asia/) — blog kỹ thuật VN.
- ProtonX, VietAI — khóa & cộng đồng AI Việt.

## 5. 🆘 Nơi hỏi khi kẹt
- Code lỗi → [Stack Overflow](https://stackoverflow.com/) · PyTorch → [discuss.pytorch.org](https://discuss.pytorch.org/)
- Toán/thống kê → [Cross Validated](https://stats.stackexchange.com/)
- Tổng quát → [r/learnmachinelearning](https://www.reddit.com/r/learnmachinelearning/) · [Hugging Face Discord](https://discord.gg/huggingface)
- VN → nhóm FB "Machine Learning cơ bản", "Vietnam AI & ML"

## 6. 🧪 Sàn luyện tập & kho dataset
- [Kaggle](https://www.kaggle.com/) (dataset + competition + notebook tham khảo) · [UCI ML Repo](https://archive.ics.uci.edu/) · [Hugging Face Datasets](https://huggingface.co/datasets)
- SQL: [LeetCode SQL 50](https://leetcode.com/studyplan/top-sql-50/) · [SQLBolt](https://sqlbolt.com/)

## 7. ⚙️ Công cụ học xuyên suốt
- **[Anki](https://apps.ankiweb.net/)** — flashcard lặp ngắt quãng (chống quên trong 9 tháng).
- **[Obsidian](https://obsidian.md/)** / Notion — nhật ký "hôm nay hiểu gì".
- **[Immersive Translate](https://immersivetranslate.com/)** — dịch song ngữ, giải quyết điểm yếu nghe tiếng Anh.

## 8. 💻 Compute khi GPU 6GB không đủ
- [Google Colab](https://colab.research.google.com/) (free + Pro ~$10/tháng) · [Kaggle Notebooks](https://www.kaggle.com/code) (~30h GPU/tuần free).
- Fine-tune LLM tiết kiệm VRAM: [Unsloth](https://github.com/unslothai/unsloth).

---

## 9. 🆘 QUY TRÌNH "KHI KẸT" (in ra, dán màn hình)
1. Đọc kỹ dòng cuối **traceback** (90% câu trả lời ở đó).
2. **Google nguyên văn lỗi** → thường ra Stack Overflow.
3. **Hỏi AI**: dán code + lỗi + "mình muốn X, sai đâu, vì sao" — *nhưng tự sửa thử trước*.
4. Kẹt >30 phút → hỏi cộng đồng (mục 5).
5. **Ghi lại lỗi + cách fix** vào Obsidian → không vấp lại.

## 10. 🤖 Dùng AI làm "gia sư" đúng cách
- ✅ Nhờ AI: giải thích khái niệm, review code, sinh quiz/flashcard, gợi ý hướng debug.
- ❌ Tránh: copy-paste lời giải khi chưa tự nghĩ → mất khả năng tự code.
- Mẹo: sau khi tự làm xong mới hỏi "code này còn cách nào tốt hơn?".

## 11. 🗓️ Nhịp tuần mẫu (5 buổi học + 2 ngày đệm)
| Thứ | Nội dung |
|---|---|
| 2–6 | 5 buổi học chính (2.5h/buổi) |
| 7 | Ôn tập + Anki + bù buổi lỡ |
| CN | Làm dự án / trục Toán / nghỉ tái tạo năng lượng |

> Giữ **streak** mỗi ngày. Cuối tuần đăng 1 post tiến độ lên LinkedIn → vừa tạo thói quen, vừa là CV sống.
