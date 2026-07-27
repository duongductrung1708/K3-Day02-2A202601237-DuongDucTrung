# 01 - Individual Problem Scan

**Bối cảnh:** Tôi là một thực tập sinh AI Engineer, công việc hằng tuần bao gồm: nghiên cứu các state-of-the-art (SOTA) papers, tiền xử lý và gán nhãn dữ liệu (data preprocessing/labeling), viết code huấn luyện và tinh chỉnh (fine-tuning) các mô hình học sâu, đánh giá hiệu năng mô hình (evaluation), và báo cáo tiến độ/kết quả thực nghiệm cho mentor hoặc team lead.

---

## 1. Bảng Scan (10 Problems)

Tôi đã quan sát và ghi nhận các vấn đề sau trong quá trình thực tập, dựa trên 4 lăng kính: Lặp lại, Tốn thời gian, AI có thể làm tốt hơn, và Pain từ người khác.

| #   | Lăng kính          | Problem quan sát được                                                                                                                                  | Ai chịu ảnh hưởng?       | Dấu hiệu thật                                                                                                       |
| --- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| 1   | Tốn thời gian      | Đọc hiểu và tóm tắt ý chính từ các SOTA papers mới để tìm phương pháp áp dụng.                                                                         | AI Intern, AI Researcher | Mất 2-3 tiếng/bài để đọc kỹ và chắt lọc kiến thức; đọc nhiều dễ bị quá tải.                                         |
| 2   | Lặp lại            | Tiền xử lý, làm sạch và chuẩn hóa định dạng dữ liệu thô (ví dụ: text, images) trước khi đưa vào mô hình.                                               | AI Intern, Data Engineer | Script xử lý thường phải viết lại hoặc tinh chỉnh nhỏ cho từng dataset mới; tốn 1-2 ngày/dataset.                   |
| 3   | Tốn thời gian      | Tìm kiếm nguyên nhân và cách sửa lỗi (debugging) khi code huấn luyện mô hình (PyTorch/TensorFlow) văng lỗi khó hiểu hoặc Out of Memory (OOM).          | AI Intern, ML Engineer   | Việc search StackOverflow, GitHub issues tốn hàng giờ; debug có thể kéo dài cả buổi.                                |
| 4   | AI có thể tốt hơn  | Viết tài liệu (documentation) cho code đã viết, docstring cho các hàm/classes.                                                                         | AI Intern, Developer     | Việc này tẻ nhạt, hay bị trì hoãn; code thiếu doc khó cho người sau đọc.                                            |
| 5   | Lặp lại            | Theo dõi (tracking) và so sánh các kết quả thực nghiệm (hyperparameters, metrics) trên Weights & Biases hoặc bảng tính.                                | AI Intern                | Mỗi lần chạy xong phải ghi nhận lại; dễ nhầm lẫn nếu chạy nhiều thí nghiệm song song.                               |
| 6   | Tốn thời gian      | Cấu hình môi trường (environment setup) và viết Dockerfile khi chuyển code từ local lên server GPU.                                                    | AI Intern, DevOps        | Hay gặp lỗi version conflict (CUDA, các thư viện Python); mất nửa ngày để setup xong môi trường chạy được.          |
| 7   | Pain từ người khác | Gán nhãn dữ liệu thủ công (Data labeling) tốn rất nhiều nguồn lực, dữ liệu gán nhãn đôi khi không nhất quán.                                           | Data Labeler, AI Intern  | Mentor thường nhắc nhở về chất lượng nhãn; đội label than phiền công việc nhàm chán, mất hàng tuần cho 1 batch lớn. |
| 8   | Lặp lại            | Viết báo cáo tiến độ (weekly update) và tổng hợp kết quả thí nghiệm để báo cáo trong buổi meeting tuần.                                                | AI Intern                | Mất khoảng 45-60 phút mỗi cuối tuần để gom nhặt lại kết quả, tạo biểu đồ và viết báo cáo.                           |
| 9   | AI có thể tốt hơn  | Tối ưu hóa hyperparameter (Hyperparameter tuning) thường phải thử sai thủ công hoặc dùng các thư viện tự động nhưng tốn rất nhiều thời gian tính toán. | AI Intern                | Phải đợi hàng ngày trời để grid search chạy xong; kết quả đôi khi chỉ cải thiện 1-2%.                               |
| 10  | Tốn thời gian      | Phân tích các trường hợp mô hình dự đoán sai (error analysis) để hiểu điểm yếu của mô hình.                                                            | AI Intern, ML Engineer   | Phải xem từng sample sai, thống kê pattern thủ công; tốn hàng buổi để viết được 1 nhận định chất lượng.             |

---

## 2. Lựa chọn Top 3 Problem Cards

| Rank | Problem                                               | Vì sao chọn                                                                                                                                                                                                            | Điều còn chưa chắc                                                                                              |
| ---- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 1    | Đọc và tóm tắt SOTA papers (Problem 1)                | Đây là việc cốt lõi của R&D, chiếm rất nhiều thời gian (bottleneck rõ). Việc trích xuất phương pháp, datasets, metrics là tác vụ ngôn ngữ mà AI hiện đại (LLM) làm rất tốt. Có thể đo lường impact bằng thời gian đọc. | Chất lượng tóm tắt kỹ thuật chuyên sâu của AI có đủ độ chính xác và không bị "hallucinate" (ảo giác) hay không. |
| 2    | Phân tích các ca dự đoán sai của mô hình (Problem 10) | Workflow rõ ràng, hiện tại làm thủ công rất chậm. Có tiềm năng kết hợp Rule (tính toán metrics) và AI (phân cụm, tìm pattern trong text/ảnh lỗi). Impact trực tiếp đến việc cải thiện model.                           | Khả năng AI hiểu được ngữ cảnh đặc thù của từng bài toán để nhóm các lỗi một cách có ý nghĩa.                   |
| 3    | Viết Weekly Report tổng hợp thực nghiệm (Problem 8)   | Giống bài toán kinh điển, pain point rõ ràng (viết narrative từ số liệu W&B/log). Workflow lặp lại hàng tuần. Dễ so sánh Rule/Workflow/Agent.                                                                          | Impact có thể không quá lớn (chỉ tiết kiệm ~1 tiếng/tuần) so với 2 bài trên, nhưng dễ triển khai pilot.         |

---

### Problem Card #1: Đọc và tóm tắt SOTA papers

**Problem 1 câu:**
AI Intern/Researcher mất quá nhiều thời gian (2-3 tiếng) để đọc sâu một research paper mới chỉ để trích xuất các thông tin cốt lõi (phương pháp, kiến trúc, dataset, kết quả) nhằm quyết định xem paper đó có hữu ích cho dự án hiện tại hay không.

**Actor:**
AI Intern, AI Researcher.

**Thời điểm / bối cảnh:**
Khi bắt đầu một task mới, hoặc khi cập nhật công nghệ hàng tuần (literature review).

**Current workflow (3-7 bước):**

1. Tìm kiếm paper (5').
2. Đọc Abstract và Introduction (15').
3. Lướt qua phần Method/Architecture để tìm điểm mới (30').
4. Xem bảng kết quả (Experiments/Results) (20').
5. Đọc kỹ phần Implementation Details nếu thấy khả thi (45').
6. Viết note tóm tắt lại các ý chính vào Notion (15').

**Bottleneck:**
Bước 3, 4 và 5: Đọc sâu để tìm và đối chiếu các thông tin kỹ thuật (phương pháp mới là gì, dùng dataset nào, metric ra sao) chiếm hầu hết thời gian (hơn 1.5 tiếng) và đòi hỏi tập trung cao độ.

**Impact:**
Một người đọc 3-5 papers/tuần mất khoảng 8-10 tiếng. Giảm tốc độ R&D. Đôi khi đọc xong cả bài mới nhận ra paper không áp dụng được (sunk cost).

**Success metric:**
Giảm thời gian đánh giá và trích xuất thông tin một paper từ 2 tiếng xuống dưới 30 phút. Người đọc vẫn nắm đủ ý chính để quyết định có nên implement hay không.

**Non-AI alternative:**
Chỉ đọc Abstract/Conclusion (rủi ro bỏ sót chi tiết quan trọng), hoặc dùng các trang tóm tắt paper có sẵn (ít tùy biến theo câu hỏi cụ thể của team).

**AI hypothesis:**
AI tự động parse file PDF, trích xuất cấu trúc (Method, Dataset, Metrics), tóm tắt các điểm mới lạ (novelty) và trả lời các câu hỏi kỹ thuật cụ thể do Intern đặt ra. Intern sẽ review bản tóm tắt và quyết định có đọc kỹ bản gốc hay không.

**Quick gut:** [x] Workflow

#### Draft Workflow cho Problem #1

```text
CURRENT STATE — ~125 phút (2 tiếng)
[1 Tìm paper: 5']
→ [2 Đọc Abstract/Intro: 15']
→ [3 Đọc Method: 30']         <-- bottleneck
→ [4 Đọc Results: 20']        <-- bottleneck
→ [5 Đọc Implementation: 40'] <-- bottleneck
→ [6 Viết note tóm tắt: 15']

FUTURE STATE — ~25 phút
[1 Tìm paper: 5']
→ [2 Nạp PDF vào AI tool: 1']
→ [3 AI trích xuất Method, Dataset, Results theo template: 2']       -- Workflow step
→ [4 Intern review tóm tắt và chat để hỏi sâu thêm chi tiết: 15']    <-- human boundary
→ [5 Intern lưu note: 2']

Fallback: AI tóm tắt sai lệch chuyên môn → Intern phát hiện khi chat và tự quay lại đọc bản gốc.
```

---

### Problem Card #2: Phân tích các ca dự đoán sai của mô hình (Error Analysis)

**Problem 1 câu:**
Quá trình phân tích hàng trăm/nghìn mẫu dự đoán sai (error analysis) diễn ra thủ công, tốn nhiều buổi làm việc để ML Engineer có thể gom nhóm và tìm ra pattern (điểm yếu) của mô hình.

**Actor:**
AI Intern, ML Engineer.

**Thời điểm / bối cảnh:**
Sau khi train xong một phiên bản mô hình và chạy trên tập validation/test.

**Current workflow (3-7 bước):**

1. Export danh sách các mẫu dự đoán sai kèm confidence score.
2. Filter các mẫu có lỗi nghiêm trọng hoặc confidence cao nhưng dự đoán sai.
3. Mở từng file (ảnh/text) lên để xem bằng mắt thường.
4. Ghi chú lại nhận định cá nhân cho từng mẫu vào spreadsheet.
5. Gom nhóm các ghi chú để tìm pattern chung (ví dụ: "model hay sai khi ảnh thiếu sáng").
6. Quyết định hướng khắc phục (thêm data, data augmentation, sửa rule).

**Bottleneck:**
Bước 3, 4 và 5: Xem từng mẫu và gom nhóm thủ công tốn rất nhiều thời gian (thường chiếm 70% thời gian phân tích).

**Impact:**
Mất 1-2 ngày cho mỗi vòng lặp error analysis. Quá trình tẻ nhạt làm giảm động lực, dễ dẫn đến việc bỏ qua các pattern tinh vi.

**Success metric:**
Giảm thời gian phát hiện pattern lỗi chính từ 1 ngày xuống dưới 2 tiếng. Báo cáo phân tích tự động chỉ ra được ít nhất 80% các pattern lỗi mà người thật có thể tìm thấy.

**Non-AI alternative:**
Chỉ dùng các rule thống kê đơn giản (ví dụ: sort theo loss) hoặc lấy ngẫu nhiên 50 mẫu để xem (rủi ro không đại diện cho toàn bộ lỗi).

**AI hypothesis:**
Dùng AI (như LLM cho text hoặc VLM cho ảnh) để tự động "xem" các mẫu lỗi, sinh mô tả, và dùng thuật toán clustering để gom nhóm các lỗi có điểm chung. Engineer chỉ cần review các cụm lỗi (clusters) đã được AI tổng hợp.

**Quick gut:** [x] Workflow (Kết hợp Rule + AI)

#### Draft Workflow cho Problem #2

```text
CURRENT STATE — ~8 giờ (1 ngày làm việc)
[1 Export errors: 15']
→ [2 Filter samples: 15']
→ [3 Xem từng mẫu thủ công: 4 tiếng]  <-- bottleneck
→ [4 Ghi chú vào sheet: 2 tiếng]      <-- bottleneck
→ [5 Gom nhóm pattern: 1 tiếng]       <-- bottleneck
→ [6 Quyết định next step: 30']

FUTURE STATE — ~2 giờ
[1 Export errors: 15']
→ [2 Script tự động nạp dữ liệu lỗi vào hệ thống: 5']
→ [3 AI sinh mô tả & gom cụm (Clustering) tự động: 10']              -- Workflow step
→ [4 Engineer review các cụm lỗi (clusters) & tóm tắt của AI: 1 tiếng] <-- human boundary
→ [5 Engineer chốt pattern & next step: 30']

Fallback: Cụm do AI tạo ra vô nghĩa → Engineer chuyển về xem random sample thủ công.
```

---

### Problem Card #3: Viết Weekly Report tổng hợp thực nghiệm

**Problem 1 câu:**
Mỗi cuối tuần, AI Intern mất khoảng 45-60 phút để đi copy số liệu, biểu đồ từ Weights & Biases (W&B) và GitHub commit để chắp vá thành một báo cáo tiến độ hợp lý.

**Actor:**
AI Intern.

**Thời điểm / bối cảnh:**
Thứ Sáu hàng tuần hoặc trước buổi sync meeting.

**Current workflow (3-7 bước):**

1. Mở dashboard W&B.
2. Lọc các run/thí nghiệm có kết quả tốt nhất trong tuần.
3. Chụp màn hình biểu đồ loss/metric.
4. Xem lại lịch sử commit trên GitHub để nhớ đã code những gì.
5. Viết narrative tổng hợp: đã thử gì, kết quả ra sao, next step là gì.
6. Format báo cáo và gửi.

**Bottleneck:**
Bước 4 và 5: Nhớ lại context của cả tuần và viết thành một câu chuyện (narrative) logic tốn nhiều não lực (khoảng 30 phút).

**Impact:**
Tốn khoảng 1 tiếng mỗi tuần, không mang lại nhiều giá trị học thuật. Báo cáo đôi khi viết vội nên khó hiểu cho người ngoài project (mentor).

**Success metric:**
Giảm thời gian làm báo cáo xuống dưới 15 phút.

**Non-AI alternative:**
Dùng template cố định, chỉ điền số liệu (không có narrative).

**AI hypothesis:**
Dùng script kéo data từ W&B API và GitHub API, sau đó LLM tóm tắt các thay đổi và kết quả thành bản draft report. Intern review và chỉnh sửa.

**Quick gut:** [x] Rule / Workflow

#### Draft Workflow cho Problem #3

```text
CURRENT STATE — ~60 phút
[1 Mở W&B lọc kết quả: 10']
→ [2 Chụp ảnh/lấy số: 10']
→ [3 Xem lại git history: 10']
→ [4 Viết narrative: 20']      <-- bottleneck
→ [5 Format & gửi: 10']

FUTURE STATE — ~15 phút
[1 Chạy script kéo data (W&B, Git): 2']  -- Rule
→ [2 AI draft narrative: 3']              -- Workflow step
→ [3 Intern review, sửa lỗi & chèn thêm ý: 8'] <-- human boundary
→ [4 Gửi: 2']
```

---

## 3. Chọn Problem Card để Pitch

**Card muốn pitch nhất:** Problem Card #1: Đọc và tóm tắt SOTA papers

**Vì sao:**

- Đây là "pain point" lớn nhất và tốn nhiều thời gian nhất của một AI Intern/Researcher.
- Công việc này đòi hỏi xử lý ngôn ngữ tự nhiên (NLP) ở mức độ cao (đọc hiểu văn bản học thuật), là điểm mạnh tuyệt đối của các mô hình LLM hiện nay.
- Workflow trước và sau rất rõ ràng, metric dễ đo lường (thời gian đọc và mức độ hiểu).
- Tính khả thi cao: Có thể sử dụng RAG (Retrieval-Augmented Generation) kết hợp với các parser PDF chuyên dụng để xây dựng solution.

**Câu hỏi tôi muốn nhóm challenge:**

- Làm sao để đo lường "chất lượng hiểu" (mức độ nắm bắt ý chính) của Intern khi dùng AI tóm tắt so với việc tự đọc toàn bộ paper?
- Việc dựa dẫm vào AI tóm tắt có làm thui chột khả năng tư duy phản biện và kỹ năng đọc hiểu bài báo khoa học của Intern về lâu dài không?
