# 02 — Group Problem Statement
# Group Report — Day 02

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|---:|---|---|---|
| 1 | Nguyễn Văn Linh | 2A202601971 | Scan/pitch candidates, gom cluster, lập luận Rule-first cho daily update. |
| 2 | Dương Đức Trung | 2A202601237 | Quick Interview, log baseline và kiểm tra metric. |
| 3 | Lê Quốc An | 2A202601811 | Research giải pháp, workflow before/after, risk và fallback. |
| 4 | Nguyễn Duy Hoàng | 2A202601147 | Problem Statement v0/v1, Rule/Workflow/Agent, decision, pilot và rollback. |


> Nhóm tổng hợp **12 Problem Cards**. Báo cáo phân biệt bằng chứng từ cards với Quick Interview và log hai chu kỳ báo cáo. Validation xác nhận pain, nhưng input chưa được chuẩn hóa nhất quán; quyết định hiện tại là **Not Yet**: chạy Rule trước, rồi mới cân nhắc Workflow AI.

## Phase 3 — Group convergence

### 3.1. Danh sách 12 candidates

| # | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cluster |
|---|---|---|---|---|
| 1 | Daily progress update và phát hiện blocker dự án 4 người | Nhóm dự án | Update thiếu cấu trúc, hỏi lại blocker/dependency | Báo cáo & điều phối |
| 2 | Tìm bối cảnh khi nhận task/handoff | Thành viên nhận task | Nối Discord, Git và tài liệu rời rạc | Tìm tri thức & quyết định |
| 3 | Biến yêu cầu lab thành checklist nộp Git | Học viên | Tự tổng hợp yêu cầu từ nhiều nguồn | Tuân thủ/nộp bài |
| 4 | Đối chiếu yêu cầu lab trước khi nộp | Học viên | Tự suy ra field/artifact còn thiếu | Tuân thủ/nộp bài |
| 5 | Tìm lại Q&A/quyết định cũ trong Discord | Học viên, thành viên nhóm | Search và đọc nhiều thread thiếu context | Tìm tri thức & quyết định |
| 6 | Ôn kiến thức từ nhiều nguồn sau buổi học | Học viên | Tự tổng hợp slide, worksheet, Discord, note | Học tập & research |
| 7 | Đọc và tóm tắt SOTA papers | AI Intern/Researcher | Đọc Method/Results/Implementation sâu | Học tập & research |
| 8 | Error analysis các ca mô hình dự đoán sai | AI Intern/ML Engineer | Xem mẫu, ghi chú, gom pattern thủ công | ML/R&D chuyên sâu |
| 9 | Weekly report tổng hợp thực nghiệm | AI Intern | Viết narrative từ W&B và Git history | Báo cáo & điều phối |
| 10 | Báo cáo tiến độ tuần cho giảng viên/mentor | Sinh viên/nhóm trưởng | Viết nhận xét/insight từ nhiều nguồn | Báo cáo & điều phối |
| 11 | Tìm quyết định và góp ý cũ đa kênh | Sinh viên/nhóm trưởng | Search nhiều kênh và đọc context | Tìm tri thức & quyết định |
| 12 | Viết meeting notes sau buổi họp | Người ghi notes/nhóm trưởng | Chuyển ghi chú thô thành action item rõ ràng | Báo cáo & điều phối |

### 3.2. Gom cluster

| Cluster | Candidates included | Pattern chung | Nhận xét |
|---|---|---|---|
| A. Báo cáo & điều phối | 1, 9, 10, 12 | Gom update, số liệu, chat hoặc notes thành thông tin người khác có thể hành động. | Có 4/12 cards, workflow lặp lại và có thể đo thời gian/chất lượng handoff. |
| B. Tìm tri thức & quyết định | 2, 5, 11 | Cần tìm lại context/decision trong Discord, Git hoặc nhiều kênh. | Pain rộng nhưng data access và scope search đa nguồn cần kiểm soát. |
| C. Tuân thủ/nộp bài | 3, 4 | Đối chiếu yêu cầu với artifact trước khi nộp. | Rõ và nhỏ; Rule/checklist có thể đã đủ cho phần lớn case. |
| D. Học tập & research | 6, 7 | Tổng hợp/tóm tắt tài liệu nhiều nguồn. | Metric chất lượng học/đọc khó hơn metric thời gian. |
| E. ML/R&D chuyên sâu | 8 | Phân tích pattern lỗi mô hình. | Impact lớn nhưng domain/data/pilot vượt scope một buổi lab của nhóm hiện tại. |

### 3.3. Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| Báo cáo tiến độ tuần cho giảng viên/mentor | Actor, workflow, bottleneck và baseline đã có log rõ; được củng cố bởi các cards daily update, weekly experiment report và meeting notes trong cùng cluster. | Board/update chưa được chuẩn hóa nhất quán; baseline vận hành 72–80 phút khi board tương đối sạch, raw log là 97 và 72 phút. |
| Daily progress update dự án 4 người | Xảy ra hằng ngày, gắn deadline dự án và có thể đo chất lượng update/dependency. | Template/board có thể giải 70–80% pain; chưa chắc cần AI. |
| Error analysis mô hình | Impact và bottleneck rõ; có Rule + AI hợp lý. | Dữ liệu/chuyên môn chuyên sâu, khó pilot và khó để cả nhóm kiểm chứng trong lab. |

### 3.4. Score để đồng thuận

> Điểm 1–5 là đánh giá từ nội dung 12 cards, không thay thế validation với người dùng ngoài nhóm.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Báo cáo tiến độ tuần | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Daily progress update | 5 | 5 | 4 | 5 | 5 | 4 | 5 | 33 |
| Error analysis | 4 | 5 | 4 | 5 | 3 | 5 | 3 | 29 |

**Candidate nhóm chọn để đào sâu:** **Tổng hợp báo cáo tiến độ tuần cho nhóm dự án gửi giảng viên/mentor**.

**Vì sao chọn:** Đây là một workflow tuyến tính, có một owner rõ (sinh viên/nhóm trưởng), một người nhận rõ (giảng viên/mentor), baseline đã được log (72–80 phút khi board tương đối sạch; raw log 97 và 72 phút) và bottleneck xác định được (biến dữ liệu rời rạc thành narrative/insight). Nó cũng tận dụng được daily updates như input có cấu trúc, weekly experiment report và meeting notes như các pattern cùng cluster.

**Vì sao không chọn các candidate còn lại:**

- Daily update: cần thử Rule/template và board trước; nếu đủ thì đó là lời giải tốt hơn Workflow AI.
- Error analysis: scope R&D và yêu cầu dữ liệu/chuyên môn riêng quá lớn cho pilot chung của nhóm.
- Search decision/FAQ: actor rộng, data access/permission và nguồn chuẩn chưa rõ; dễ trượt thành “search agent” quá lớn.
- Checklist nộp lab: phù hợp Rule/script hơn, nhưng không giải tốt phần narrative/context.

**Cách xử lý chênh lệch khi chọn candidate:** Hai candidate đứng đầu chỉ chênh 1 điểm (34 và 33). Nhóm không coi score là quyết định tự động; nhóm ưu tiên báo cáo tiến độ tuần vì có Quick Interview và log hai chu kỳ làm baseline cụ thể. Daily progress update vẫn được giữ làm Rule/input cho candidate đã chọn, thay vì bị loại hoàn toàn.

---

## Phase 4 — Quick validation và research

### 4.1. Bằng chứng hiện có và quick validation

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác / giới hạn | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Tổng hợp Problem Cards | 4 thành viên | 3 cards trực tiếp về báo cáo/update và 1 card meeting notes đều cho thấy pain “gom nguồn → viết/tóm tắt để người khác hành động”. | Đây là tự báo cáo từ cards, chưa phải interview độc lập; một bối cảnh là AI R&D, không hoàn toàn giống báo cáo sinh viên. | Thu hẹp actor xuống sinh viên/nhóm trưởng làm báo cáo dự án cho giảng viên/mentor. |
| Card được chọn | 1 workflow có baseline | Báo cáo tuần gồm Classroom/Notion, tiến độ nhóm và chat; bottleneck narrative 20–25 phút trong tổng 72–80 phút khi board tương đối sạch. | Mới có hai chu kỳ; Tuần A bị nhiễu Discord. | Dùng làm baseline Rule và tiếp tục đo sau khi chuẩn hóa input. |
| Quick interview | 3 sinh viên/nhóm trưởng | Pain được xác nhận ở 3/3 người; rõ nhất khi input chưa chuẩn. Khi board sạch, thời gian giảm nhưng narrative vẫn nghẽn. | Mẫu nhỏ; phần lớn là người có trách nhiệm tổng hợp nên chưa đại diện mọi sinh viên. | Giữ scope nhóm trưởng/sinh viên làm weekly report; không khái quát thành mọi người học. |
| Log workflow hiện tại | 2 chu kỳ báo cáo | Tuần A 97 phút, Tuần B 72 phút; baseline vận hành khi board tương đối sạch là 72–80 phút; narrative 20–25 phút; mentor hỏi lại 2–3 câu/tuần. | Mới có hai chu kỳ; Tuần A bị nhiễu Discord nhiều hơn. | Dùng làm baseline Rule, rồi so sánh trước khi quyết định pilot Workflow AI. |

### Quick interview (3 người, ẩn danh)

**Câu hỏi chung:** Lần gần nhất làm weekly report? Đang dùng workflow nào? Bước nào đau nhất? Mất bao lâu? Nếu tốt hơn muốn đổi gì?

| Người | Vai trò | Lần gần nhất | Nguồn đang dùng | Bước đau nhất | Thời gian tự ước lượng | Mentor/GV hỏi lại gì? | Mong muốn nếu cải thiện |
|---|---|---|---|---|---:|---|---|
| I1 | Nhóm trưởng dự án 4 người | Cuối tuần trước, trước buổi mentor | Notion task + Discord + Git commit message | Viết phần “rủi ro + kế hoạch tuần sau” từ chat rời | 70–80 phút | “Blocker nào còn mở?”; “Ai phụ trách item X?” | Có draft từ update sẵn, mình chỉ sửa và gửi. |
| I2 | Thành viên từng thay nhóm trưởng viết report | 2 tuần trước | Google Sheet tiến độ + screenshot PR | Gom update của từng bạn vì format khác nhau | 45–60 phút | “Tuần này xong được gì so với plan?” | Bắt buộc một mẫu update ngắn mỗi ngày. |
| I3 | Nhóm trưởng nhóm khác cùng lớp | Tuần này | Notion database đã có status/owner | Ít đau ở lấy số; vẫn mất thời gian viết narrative đủ ngắn cho mentor | 35–45 phút nếu Notion sạch; từng hơn 60 phút khi update thiếu | Ít hỏi số liệu hơn, vẫn hỏi “Bài học tuần này?” | Template report + gợi ý narrative, không tự gửi. |

**Kết luận interview:**

- Pain được xác nhận ở ít nhất 2/3 người, đặc biệt khi input chưa chuẩn.
- Khi board/update có cấu trúc như trường hợp I3, tổng thời gian giảm rõ; Rule có giá trị lớn.
- Narrative/insight/risk/next step vẫn là bước ngôn ngữ khó thay bằng checklist đơn thuần.
- Chưa có tín hiệu đủ mạnh để nhảy Agent hoặc Go AI khi chưa chuẩn hóa update.

### Log hai chu kỳ báo cáo (bấm giờ thật)

**Owner log:** Nhóm trưởng, người viết report tuần.
**Phạm vi:** Chỉ đo thời gian chuẩn bị + viết + gửi; không tính thời gian họp mentor.

| Bước | Tuần A (phút) | Tuần B (phút) | Trung bình | Ghi chú |
|---|---:|---:|---:|---|
| 1. Lấy task/mốc từ Classroom/Notion/board | 12 | 8 | 10 | Tuần B board đã cập nhật sẵn hơn. |
| 2. Kiểm tra tiến độ cá nhân + nhóm | 11 | 9 | 10 | Phụ thuộc update của thành viên. |
| 3. Đọc daily updates/chat/notes | 18 | 12 | 15 | Tuần A Discord nhiễu, nhiều tin không liên quan. |
| 4. Xem Git history/artifact | 10 | 9 | 9,5 | Chủ yếu link PR/commit. |
| 5. Tổng hợp vào Docs | 12 | 8 | 10 | Copy/paste thủ công. |
| 6. Viết narrative: highlight, risk, next step | 26 | 20 | **23** | **Bottleneck cả hai tuần.** |
| 7. Self-review, format, gửi | 8 | 6 | 7 | |
| **Tổng** | **97** | **72** | **84,5** | Khi board tương đối sạch, baseline vận hành dùng là **72–80 phút**. |

| Chỉ số chất lượng | Tuần A | Tuần B | Nhận xét |
|---|---:|---:|---|
| Số nguồn chính dùng | 4: Notion, Discord, Git, Sheet | 3: Notion, Git, notes họp | Ít nguồn hơn giúp nhanh hơn. |
| Claim/số liệu không truy được nguồn lúc self-review | 3 chỗ | 1 chỗ | Dễ lẫn “cảm nhận” với fact. |
| Câu mentor hỏi lại ở buổi sau | 3 | 2 | Chủ yếu risk mở và owner của next step. |
| Tỷ lệ thời gian ở bước narrative | 27% | 28% | Ổn định khoảng 1/4–1/3 tổng thời gian. |

**Baseline nhóm chốt cho metric:** Tổng thời gian hiện tại **72–80 phút/tuần** trong điều kiện board tương đối sạch; narrative **20–25 phút/tuần**; mentor hỏi lại **2–3 câu/tuần**, tập trung vào risk và next step.

**Insight sau validation:** Pain không nằm ở việc lấy một con số đơn lẻ. Pain là chuyển task, update, chat và Git history rời rạc thành báo cáo tuần có narrative, risk và next step đủ rõ để mentor hoặc cả nhóm hành động. Interview và log cùng cho thấy Rule chuẩn hóa update giảm phần gom dữ liệu; Workflow AI draft chỉ nên cân nhắc sau khi Rule chạy ổn định.

### 4.2. Research các pattern/giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| GitHub Projects | [GitHub Docs — About Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) | Theo dõi issues/PR, custom fields, trạng thái và status update; có thể dùng chart/insight từ dữ liệu project. | Là nền Rule/process tốt để chuẩn hóa task, owner, status trước khi viết report. | Không tự viết narrative từ context chat/lesson learned; chỉ tốt khi nhóm cập nhật dữ liệu đều. | Dùng project board/template làm nguồn có cấu trúc trước, không đưa dữ liệu rời rạc thẳng vào AI. |
| Slack AI summaries/recaps | [Slack Help — Guide to AI features](https://slack.com/help/articles/25076892548883-Guide-to-AI-features-in-Slack) | Tóm tắt channel, conversation và thread; có thể mở chi tiết để xem nguồn. | Pattern “summary có nguồn” phù hợp với việc gom update từ chat. | Availability/permission phụ thuộc workspace; summary không thay thế việc kiểm fact hay chọn insight. | Nếu AI draft report, từng claim quan trọng phải có link/nguồn để nhóm trưởng kiểm lại. |
| Notion AI Meeting Notes | [Notion — AI Meeting Notes](https://www.notion.com/en-US/product/ai-meeting-notes) | Chuyển meeting transcript/notes thành summary và action item. | Minh họa rõ AI draft + người review; nhấn mạnh consent và quyền truy cập. | Cần consent, không tự đảm bảo owner/deadline/insight chính xác. | Không auto-send report. Người chủ report review dữ liệu, narrative, owner và deadline trước khi gửi. |

**Research takeaway:** Không cần build Agent. Một process/Rule để chuẩn hóa task/status là nền bắt buộc. Nếu sau khi chuẩn hóa, bước viết narrative từ nhiều nguồn vẫn tốn đáng kể, Workflow tạo draft có trích nguồn là mức phù hợp; human review là boundary.

---

## Phase 5 — Workflow và Problem Statement

### 5.1. Current workflow

```text
CURRENT STATE — baseline vận hành 72–80 phút/tuần khi board tương đối sạch
(raw log hai tuần: 97 phút và 72 phút)

[1. Lấy task/mốc tuần từ Classroom, Notion hoặc project board: 10']
→ [2. Kiểm tra tiến độ cá nhân và nhóm: 10']
→ [3. Đọc daily updates/chat/meeting notes: 15']
→ [4. Mở Git history hoặc artifact liên quan: 10']
→ [5. Tổng hợp vào Docs: 10']
→ [6. Viết narrative: việc đã làm, insight, risk, next step: 20–25']  <-- bottleneck
→ [7. Self-review, format và gửi: 5–10']
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Sinh viên/nhóm trưởng | Mục tiêu, task, deadline | Danh sách việc trong tuần | Hằng tuần | Nguồn ưu tiên là board/Classroom chuẩn. |
| 2 | Sinh viên/nhóm trưởng | Update của 4 thành viên | Trạng thái từng task | Hằng tuần | Chất lượng phụ thuộc template update. |
| 3 | Sinh viên/nhóm trưởng | Discord/chat/meeting notes | Bối cảnh, blocker, decision | Hằng tuần | Có risk bỏ sót/nhầm context. |
| 4 | Sinh viên/nhóm trưởng | Git history/artifact | Thay đổi đã thực hiện | Hằng tuần | Chỉ dùng link/commit được phép chia sẻ. |
| 5 | Sinh viên/nhóm trưởng | Các dữ liệu đã chọn | Draft report có cấu trúc | Hằng tuần | Thường là copy/paste thủ công. |
| 6 | Sinh viên/nhóm trưởng | Draft + raw data | Narrative/insight/risk/next step | Hằng tuần | **Bottleneck chính.** |
| 7 | Sinh viên/nhóm trưởng | Report hoàn chỉnh | Report gửi mentor/nhóm | Hằng tuần | Owner chịu trách nhiệm nội dung cuối. |

### 5.2. Future workflow candidate — chỉ sau khi Rule chưa đủ

```text
FUTURE STATE CANDIDATE — chỉ pilot nếu Rule chạy 2 tuần mà narrative vẫn nghẽn

[1. Mỗi thành viên update theo mẫu task/status/blocker/next step/link] -- Rule
→ [2. Nhóm trưởng chọn nguồn được phép: board, update, Git, notes]     -- Human boundary
→ [3. Rule/script gom dữ liệu có cấu trúc vào report template]
→ [4. AI draft narrative: highlight, risk, lesson learned, next step;
    mỗi claim gắn nguồn]                                                -- Workflow step
→ [5. Nhóm trưởng kiểm nguồn, số liệu, narrative và chỉnh sửa]         -- Human boundary
→ [6. Gửi mentor/nhóm]                                                  -- Human send

Fallback:
Draft thiếu nguồn, bịa số liệu, hoặc sai bối cảnh
→ bỏ draft; dùng template + dữ liệu nguồn để tự viết report thủ công.
```

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Tổng thời gian chuẩn bị + viết report | 72–80 phút/tuần khi board tương đối sạch; raw log: 97 và 72 phút | Dưới 25 phút/tuần sau Workflow pilot | Bấm giờ từng bước sau 2 tuần Rule và sau pilot. |
| Thời gian viết narrative | 20–25 phút/tuần | Dưới 10 phút review/edit | Bấm giờ phần draft + edit, không tính auto-run. |
| Chất lượng nguồn | 3 claim không truy được nguồn ở Tuần A; 1 ở Tuần B | 0 claim chính không truy được nguồn | Review report trước gửi. |
| Câu hỏi/yêu cầu bổ sung từ mentor | 2–3 câu/tuần | Không tăng; mục tiêu dưới hoặc bằng 2/report | Đếm trong feedback đến buổi mentor sau. |
| Bước thủ công | 7/7 | 3/6: chọn nguồn, review/edit, gửi | Không tự động hóa approval. |

### 5.3. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên/nhóm trưởng tổng hợp báo cáo tiến độ tuần của dự án cho giảng viên/mentor và các thành viên nhóm. |
| **Workflow** | Lấy task → kiểm tra tiến độ → đọc chat/notes → xem Git/artifact → tổng hợp → viết narrative → review/gửi. |
| **Bottleneck** | Viết narrative từ dữ liệu rời rạc (việc đã làm, insight, risk, bài học và next step) mất khoảng 20–25 phút/tuần trong baseline và dễ nghẽn ý. |
| **Impact** | Baseline vận hành là 72–80 phút/tuần khi board tương đối sạch; log vẫn có 1–3 claim không truy được nguồn và mentor hỏi lại 2–3 câu/tuần. |
| **Success Metric** | Sau khi Rule chạy ổn định, nếu pilot Workflow thì giảm tổng thời gian từ baseline 72–80 phút xuống dưới 25 phút; không còn claim chính không truy được nguồn; không tăng câu hỏi/yêu cầu bổ sung và mục tiêu dưới hoặc bằng 2/report. |
| **Boundary** | Không tự gửi report, không tự bịa số liệu/insight, không tự đổi priority hoặc commit thay nhóm; chỉ dùng nguồn nhóm cho phép. |

---

## Phase 6 — Rule / Workflow / Agent và quyết định

### 6.0. Ma trận độ phù hợp

```text
Độ mơ hồ: cao — narrative/insight có nhiều cách viết chấp nhận được,
nhưng phải trung thực với nguồn.

Độ phức tạp: trung bình — nhiều nguồn (board, daily update, Git, notes)
nhưng đường đi 6–7 bước rõ, không cần AI tự chọn mục tiêu.

Kết luận: Rule cho dữ liệu có cấu trúc + Workflow để draft narrative;
không cần Agent.
```

### 6.1. So sánh Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Template daily update, GitHub Project/board có status-owner-deadline, template weekly report và checklist nguồn. | Đủ nếu sau 2 tuần, copy/paste và narrative không còn là bottleneck lớn. | Phụ thuộc kỷ luật cập nhật; vẫn phải tổng hợp/viết narrative thủ công. | Bắt buộc làm nền, phải thử trước. |
| **Workflow** | Gom các nguồn đã chọn → map vào template → AI tạo draft narrative có source links → nhóm trưởng review → gửi. | Chỉ phù hợp nếu Rule đã chạy 2 tuần nhưng narrative/tổng hợp vẫn mất thời gian đáng kể. | Hallucination, bỏ sót, lẫn context/tuần, lộ dữ liệu. | Chưa chọn; candidate cho pilot có điều kiện. |
| **Agent** | Tự tìm nguồn, chọn số liệu, viết, gửi report hoặc giao lại task. | Chỉ hợp lý nếu cần tự lập kế hoạch nhiều nhánh/tool mà Workflow không thể mô tả. | Permission/scope lớn; có thể gửi sai hoặc tự đổi ưu tiên. | Không chọn. |

**Mức chọn hiện tại:** `Rule` — mẫu daily update, board có task/status/owner/deadline và weekly-report template.

**Mức có thể chọn sau Rule:** `Workflow`, chỉ khi log hai tuần cho thấy narrative vẫn mất từ 10–15 phút trở lên hoặc tổng workflow không đạt target. Human review vẫn bắt buộc.

**Vì sao chọn mức đơn giản hơn trước:** Interview I3 và log Tuần B cho thấy board/update sạch đã giảm đáng kể phần gom dữ liệu. Vì vậy Rule là lựa chọn hiện tại; nhóm chỉ nâng lên Workflow nếu hai tuần Rule không xử lý đủ bottleneck narrative/insight.

**Vì sao không chọn Agent:** Các bước, owner và điểm gửi đã cố định. AI không cần tự chọn công cụ, đổi kế hoạch hay hành động độc lập.

### 6.2. Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên/nhóm trưởng của dự án học tập, chịu trách nhiệm gửi weekly progress report cho mentor/giảng viên và nhóm. |
| **Workflow** | Thành viên update theo template → nhóm trưởng chọn board/chat/Git/notes có quyền → gom vào report → draft narrative → review → gửi. |
| **Bottleneck** | Sau khi đã có dữ liệu nguồn, nhóm trưởng phải biến nhiều update rời rạc thành narrative đáng tin gồm highlight, risk, lesson learned và next step. |
| **Impact** | Baseline vận hành 72–80 phút/tuần khi board tương đối sạch; report có 1–3 claim không truy được nguồn và mentor hỏi lại 2–3 câu/tuần về risk/next step. |
| **Success Metric** | Sau 2 tuần Rule, nếu narrative vẫn nghẽn thì pilot Workflow: tổng thời gian dưới 25 phút/tuần; narrative review/edit dưới 10 phút; 0 claim chính không truy được nguồn; không tăng câu hỏi/yêu cầu bổ sung. |
| **Boundary** | AI chỉ tạo draft từ nguồn do nhóm trưởng chọn; không bịa số liệu, không tự gửi, không tự gán owner/deadline hay đổi priority; nhóm trưởng approve cuối. |
| **AI intervention point** | Sau bước Rule/script gom dữ liệu vào template và trước review/edit của nhóm trưởng. |
| **Mức chọn** | Rule hiện tại; Workflow chỉ được pilot sau khi Rule/template đã chạy 2 tuần và chứng minh chưa đủ. |
| **Rủi ro & người thật kiểm tra** | Rủi ro: hallucination, sai tuần/sai số, thiếu blocker, lộ thông tin. Nhóm trưởng kiểm link nguồn/số liệu/narrative; thành viên xác nhận action item trước gửi. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Actor, người nhận, input, output và bottleneck được xác định. |
| Baseline và success metric đã đo được chưa? | Yes | Raw log: 97 và 72 phút; baseline vận hành 72–80 phút, narrative 20–25 phút, mentor hỏi lại 2–3 câu/tuần. |
| Có data/input đủ dùng chưa? | Not Yet | Board/update hiện chưa được chuẩn hóa nhất quán; đây là điều kiện Rule cần giải quyết trước. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes, có điều kiện | Không auto-send; claim có nguồn; nhóm trưởng review và fallback thủ công. |
| Có người review/owner vận hành không? | Yes | Sinh viên/nhóm trưởng là owner report/pilot. |
| Có cách non-AI đơn giản hơn không? | Yes | Interview I3 và log Tuần B cho thấy Rule/board sạch có tác dụng rõ; phải thử trước. |

**Decision: Not Yet.**

**Lý do:** Interview và log xác nhận pain, metric và bottleneck narrative. Tuy nhiên, chúng cũng chỉ ra Rule—mẫu daily update, board có status/owner và template report—có thể giảm đáng kể phần gom dữ liệu. Nhóm chưa có bằng chứng rằng Rule không đủ, nên chưa Go AI. Agent không phù hợp vì workflow đã tuyến tính và không cần tự hành động.

**Điều cần làm trước khi Go Workflow:**

1. Chạy Rule trong 2 tuần: daily update bắt buộc theo mẫu, board có task/status/owner/deadline và weekly report template.
2. Log lại tổng thời gian, narrative, claim không có nguồn và câu hỏi mentor ở hai tuần Rule.
3. Nếu narrative vẫn mất từ 10–15 phút trở lên hoặc tổng workflow vẫn không đạt target, Go pilot Workflow ở scope nhỏ.
4. Nhóm trưởng duyệt danh sách nguồn được phép và review toàn bộ output trước khi gửi.

**Pilot nhỏ nhất sau khi Rule chưa đủ:**

- Dùng 2 tuần dữ liệu đã được nhóm cho phép: project board, 4 daily updates, Git links/commit và meeting notes.
- Nhóm trưởng chọn input, paste/gom vào template chuẩn; AI chỉ tạo draft narrative với cấu trúc cố định và source links.
- Nhóm trưởng đo thời gian review/edit, kiểm claim và gửi report thủ công.
- So sánh với hai tuần baseline: tổng thời gian, số câu hỏi mentor, số claim phải sửa và source coverage.

**Exit / rollback:**

- Nếu Rule/template tự nó giảm 70–80% effort, dừng ở Rule.
- Nếu nhóm trưởng phải viết lại hơn 70% draft trong 2 tuần liên tiếp, quay lại template thủ công.
- Nếu AI bịa số liệu, không gắn được nguồn, hoặc để lộ dữ liệu, dừng pilot và không dùng AI output trong report chính thức.