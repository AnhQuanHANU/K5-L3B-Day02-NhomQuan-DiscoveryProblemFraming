# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: NhomQuan
- Thành viên: xem `TEAM.md` (Nguyễn Anh Quân - 2A202603892, Võ Thị Phương Nhung - 2A202603918, Nguyễn Minh Thành - 2A202603884)
- Candidate problem được chọn (1 câu): Khi vừa kết thúc workshop lấy yêu cầu với khách hàng, tôi muốn có biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, để gửi khách xác nhận trong ngày
- Quyết định cuối: Go (với điều kiện áp dụng kiến trúc Workflow có Human-in-the-loop để BA duyệt trước khi gửi)

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Quân | Khi nhận được lời mời phỏng vấn kỹ thuật/tình huống vào ngày mai, tôi muốn tổng hợp các câu hỏi phỏng vấn thường gặp dựa trên chính các yêu cầu trong JD, để luyện tập câu trả lời có trọng tâm mà không bị bỡ ngỡ | Sinh viên năm cuối / Ứng viên mới ra trường | Tốn 2-3h tự đọc JD, search Google từng keyword; câu hỏi generic không sát JD | Mỗi công ty và người phỏng vấn có phong cách hỏi rất khác nhau, câu hỏi sinh từ JD có sát thực tế phỏng vấn không? (Nhung hỏi) |
| 2 | Quân | Khi cần nộp bài tập lớn trong tuần thi, tôi muốn tìm lại nhanh link nộp bài và tiêu chí chấm điểm bị trôi trong kênh chat nhóm/lớp, để nộp đúng hạn và đủ yêu cầu mà không phải tag hỏi lại lớp trưởng | Sinh viên đại học | Tin nhắn trôi hàng trăm tin mỗi ngày trong Zalo/Discord, ghim tin nhắn bị trôi hoặc lẫn lộn | Zalo/Discord đều có tính năng Search và Pin message, tại sao không dùng rule/hashtag đơn giản thay vì cần AI? (Thành hỏi) |
| 3 | Quân | Khi làm bài tập lớn theo nhóm 4-5 người, tôi muốn theo dõi tiến độ công việc và trạng thái nộp bài của từng thành viên theo thời gian thực, để kịp thời nhắc nhở và phân phối lại việc trước hạn chót 3 ngày | Trưởng nhóm sinh viên (Team leader) | Thành viên báo cáo rời rạc qua chat, leader phải gom và tổng hợp thủ công vào bảng tính mất 30-45 phút/lần | Trello hay Notion đã có sẵn bảng Kanban và notification nhắc việc, vấn đề chính là ở ý thức thành viên hay công cụ theo dõi? (Nhung hỏi) |
| 4 | Thành | Khi bắt đầu tuần mới vào sáng thứ Hai, tôi muốn tổng hợp kết quả huấn luyện mô hình và log lỗi của tuần trước vào một chỗ, để báo cáo tiến độ cho tech lead trước 10h (#1) | AI / Data Engineer | Quy trình lặp lại hằng tuần, tốn thời gian đào bới log và metric, có baseline đo thực tế | Phần đánh giá chất lượng nhận định tự động đo thế nào? Có cần chuyên môn kỹ thuật sâu để verify số liệu không? (Quân hỏi) |
| 5 | Thành | Khi tiếp nhận module hệ thống mới hoặc refactor mã nguồn cũ, tôi muốn tìm lại các quyết định thiết kế và lý do kiến trúc trước đây, để chỉnh sửa mà không vi phạm nguyên tắc ban đầu (#2) | Software Engineer / Tech Lead | Pain chung của cả team, tốn thời gian đào bới chat/PR/Confluence cũ | Quyền truy cập và phân loại dữ liệu chat lịch sử phức tạp, liệu có lấy đủ ngữ cảnh bảo mật không? (Nhung hỏi) |
| 6 | Thành | Khi nhận tài liệu đặc tả kiến trúc kỹ thuật hoặc PR lớn hơn 1000 dòng code, tôi muốn có bản tóm tắt các thay đổi cốt lõi và cảnh báo rủi ro tương thích, để review nhanh mà không bỏ sót lỗi logic (#3) | Senior Dev / Tech Lead | Tốn nhiều thời gian đọc hiểu tài liệu và diff phức tạp (45-60 phút/bản) | Chất lượng review phụ thuộc nhiều vào ngữ cảnh dự án và nghiệp vụ ẩn, AI tóm tắt có đảm bảo không bỏ sót side-effect? (Quân hỏi) |
| 7 | Nhung | Khi vừa kết thúc workshop lấy yêu cầu với khách hàng, tôi muốn có biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, để gửi khách xác nhận trong ngày (#2) | Business Analyst (BA) | Quy trình rõ, lặp lại sau mỗi buổi workshop, dễ bấm giờ (mất 60-90 phút nghe lại recording/lọc ghi chép) | Khách hàng có cho ghi âm và đưa nội dung họp vào công cụ AI không? Xử lý bảo mật thông tin bí mật kinh doanh (NDA) ra sao? (Thành hỏi) |
| 8 | Nhung | Khi khách hàng gửi yêu cầu thay đổi (Change Request - CR) giữa sprint, tôi muốn phân tích nhanh phạm vi ảnh hưởng tới các tính năng hiện tại, để ước lượng chi phí và thời gian chính xác (#1) | Project Manager / BA | Ảnh hưởng trực tiếp tới estimate và tiến độ dự án; tài liệu rải rác nhiều nơi | Tài liệu rải rác nhiều nơi (Jira, Figma, code); chất lượng phân tích khó đo và rủi ro estimate sai rất cao? (Quân hỏi) |
| 9 | Nhung | Khi dev đặt câu hỏi làm rõ đặc tả nghiệp vụ, tôi muốn phân loại câu hỏi và tra cứu nhanh các đoạn tài liệu liên quan, để phản hồi trong vòng 30 phút mà không ngắt quãng dòng tư duy (#5) | Business Analyst (BA) | Nhiều người bị ảnh hưởng, đếm được số câu hỏi lặp đi lặp lại hàng ngày | Nguyên nhân có thể nằm ở quy trình review đặc tả từ đầu chưa kỹ, không chỉ ở cách viết hay tra cứu? (Thành hỏi) |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Review thông tin tốn thời gian | #1 (Luyện phỏng vấn theo JD - Quân), #6 (Review tài liệu kỹ thuật dài - Thành), #8 (Phân tích ảnh hưởng CR - Nhung) | Người dùng phải đọc và xử lý khối lượng lớn văn bản kỹ thuật/nghiệp vụ phức tạp; tiêu tốn tải nhận thức (cognitive load) cao để phân tích, đối chiếu và đánh giá |
| B — Phân loại dữ liệu & thông tin rời rạc | #2 (Tìm link nộp bài/deadline - Quân), #5 (Tìm quyết định thiết kế cũ - Thành), #9 (Dev hỏi lại đặc tả - Nhung) | Thông tin bị phân mảnh qua nhiều kênh giao tiếp (chat, email, PR, wiki, doc), thiếu gắn thẻ phân loại, khiến việc định tuyến, lọc và tra cứu lại mất nhiều công sức |
| C — Tổng hợp dữ liệu quy mô lớn & tạo biên bản/báo cáo định kỳ | #3 (Theo dõi tiến độ task nhóm - Quân), #4 (Tổng hợp báo cáo thử nghiệm & tiến độ tuần - Thành), #7 (Biên bản workshop lấy yêu cầu - Nhung) | Dữ liệu đầu vào thô phát sinh định kỳ với khối lượng lớn (audio thảo luận 2-3h, log thử nghiệm mô hình, báo cáo task), cần trích xuất có cấu trúc (quyết định, action items, kết quả) để báo cáo/chốt với stakeholder |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Rút ngắn thời gian phát hành biên bản workshop lấy yêu cầu từ 90 phút xuống dưới 25 phút trong khi giữ tỷ lệ bỏ sót quyết định < 5%
├── Opportunity A: BA mất 60–90 phút nghe lại recording hoặc đọc ghi chép phân mảnh để gom thông tin sau workshop kéo dài 2-3 tiếng
├── Opportunity B: Ranh giới giữa "yêu cầu đã chốt", "câu hỏi mở cần xác nhận thêm", và "action item giao cho ai" dễ bị nhập nhằng trong lúc thảo luận dồn dập
├── Opportunity C: Biên bản không được gửi trong ngày dẫn đến khách hàng quên thỏa thuận miệng, phát sinh tranh cãi và scope creep về sau
└── Opportunity D: Ngại chia sẻ transcript hoặc recording thô cho khách hàng vì chứa nhiều trao đổi ngoài lề và dữ liệu nhạy cảm
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- ~Xây dựng chatbot AI tự động tham gia Google Meet/Teams để ghi âm và tóm tắt cuộc họp~ *(Solution: phụ thuộc bot ngoài, khách hàng từ chối cho bot tham gia vì lý do bảo mật dữ liệu doanh nghiệp và NDA)*
- ~Dùng Whisper transcribe toàn bộ audio ra text rồi ném prompt dài vào ChatGPT để sinh biên bản~ *(Solution: prompt một lượt dễ hallucinate, không phân loại được context nghiệp vụ và bỏ sót quyết định ngầm định)*
- ~Tạo plugin Notion/Confluence tự động xuất biên bản PDF theo template cố định~ *(Solution: chỉ giải quyết việc hiển thị/định dạng, không giải quyết bottleneck trích xuất quyết định từ thảo luận hỗn loạn)*
- ~Bắt khách hàng tự điền form xác nhận yêu cầu sau buổi họp~ *(Solution: đẩy trách nhiệm cho khách hàng, vi phạm vai trò phục vụ của BA và làm giảm trải nghiệm khách hàng)*

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1. Chuẩn bị phỏng vấn kỹ thuật theo JD (Quân) | 4 | 3 | 3 | 2 | 4 | 3 | 5 | 24 |
| 2. Biên bản workshop lấy yêu cầu khách hàng (Nhung) | 5 | 5 | 5 | 5 | 5 | 5 | 4 | **34** |
| 3. Tổng hợp báo cáo thử nghiệm & log lỗi tuần (Thành) | 5 | 4 | 4 | 4 | 3 | 4 | 3 | 27 |

**Candidate được chọn:**
Candidate 2: *"Khi vừa kết thúc workshop lấy yêu cầu với khách hàng, tôi muốn có biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, để gửi khách xác nhận trong ngày"* (Bài toán công việc của Business Analyst - BA).

**Vì sao chọn:**

1. **Actor và quy trình nghiệp vụ cực kỳ chuẩn hóa trong thực tế:** BA trong các công ty phần mềm/dịch vụ CNTT có quy trình làm việc chuẩn sau workshop: Ghi chép/audio → Rà soát → Lọc yêu cầu, quyết định, câu hỏi mở, action items → Soạn biên bản chuẩn → Gửi khách hàng xác nhận. Quy trình này không bị phụ thuộc vào sở thích cá nhân.
2. **Baseline đo lường rõ ràng, định lượng bằng thời gian thực tế:** Mỗi buổi workshop kéo dài 2–3 giờ ngốn trung bình từ 60–90 phút của BA để hoàn thiện biên bản. Mục tiêu rút ngắn xuống dưới 25 phút review là một metric thành công có thể bấm giờ đo lường trực tiếp, không phụ thuộc vào cảm tính.
3. **Giá trị kinh doanh (Business Impact) trực tiếp và trọng yếu:** Biên bản gửi trong ngày giúp "khóa scope" kịp thời, tránh rủi ro "scope creep" (khách hàng thêm việc ngoài hợp đồng) và hiểu nhầm yêu cầu, giúp doanh nghiệp tiết kiệm hàng nghìn USD chi phí làm lại (rework).
4. **Điểm can thiệp AI và ranh giới an toàn (Human-in-the-Loop) rõ ràng:** AI chỉ đóng vai trò trợ lý trích xuất và phân loại cấu trúc thông tin sơ bộ từ bản ghi chép/transcript; BA luôn là người rà soát cuối cùng (human gatekeeper) trước khi gửi cho khách. Hệ thống không tự ý phát hành tài liệu ra bên ngoài, đảm bảo an toàn nghiệp vụ tuyệt đối.
5. **So sánh rõ nét cả 4 mức độ giải pháp:**
   - *No AI:* Dùng template Word/Notion chuẩn để gõ tay trực tiếp.
   - *Rule:* Dùng regex hoặc script lọc theo các cú pháp tag cố định (ví dụ `@decision`, `@action`).
   - *Workflow:* Speech-to-text (hoặc transcript) → LLM trích xuất và phân loại thành 4 mục độc lập → BA kiểm tra, chỉnh sửa → Gửi email (mức phù hợp nhất).
   - *Agent:* Tự động phân tích hội thoại, tự động tạo ticket Jira, tự động gửi email cho khách mà không qua người duyệt (mức rủi ro cao, không khuyến nghị).
6. **Vừa sức và dễ kiểm chứng nhanh trong phạm vi môn học:** Cả nhóm có thể dễ dàng tiếp cận phỏng vấn các anh/chị BA, PM đang đi làm để thu thập interview snapshot thực tế, đồng thời kiểm thử ngay prototype trích xuất trên transcript cuộc họp mẫu.

**Vì sao loại các candidate còn lại:**

- **Loại Candidate 1 (Chuẩn bị phỏng vấn theo JD của Quân):**
  - *Impact khó đo lường khách quan:* Kết quả đỗ hay trượt phỏng vấn phụ thuộc vào rất nhiều biến số phi kỹ thuật (body language, sự ăn ý văn hóa, tâm lý của interviewer, mức độ cạnh tranh của các ứng viên khác). Rất khó chứng minh việc AI sinh câu hỏi có giúp tăng tỷ lệ đậu phỏng vấn hay không.
  - *Quy trình không chuẩn hóa:* Mỗi sinh viên có phong cách ôn tập khác nhau, không có baseline thời gian hay tài liệu chuẩn cố định.
  - *Giá trị thặng dư của giải pháp thấp:* Người dùng hoàn toàn có thể tự copy JD vào ChatGPT bản miễn phí để hỏi vài câu prompt đơn giản mà không cần đến một hệ thống hay workflow chuyên biệt.
- **Loại Candidate 3 (Tổng hợp báo cáo thử nghiệm & log lỗi tuần của Thành):**
  - *Thiên về Rule/Script/Dashboard hơn là bài toán AI:* Việc gom log lỗi và tổng hợp chỉ số huấn luyện (accuracy, loss, latency) đã có các công cụ MLOps chuyên dụng giải quyết rất tốt và chính xác 100% bằng rule-based (như TensorBoard, MLflow, Weights & Biases, Grafana). Dùng AI ở đây là "dùng dao mổ trâu giết gà".
  - *Rủi ro ảo giác (Hallucination) nguy hiểm về số liệu:* AI tóm tắt có xu hướng làm tròn hoặc bịa số liệu metric và log kỹ thuật — điều tối kỵ trong báo cáo kỹ thuật cho Tech Lead.
  - *Khó tiếp cận tệp người dùng rộng:* Đối tượng AI Engineer làm việc với training log hẹp hơn nhiều so với vị trí BA - vai trò có mặt ở mọi dự án phần mềm.

**Xử lý bất đồng (nếu có):**
Ban đầu Quân rất tâm đắc với Candidate 1 vì bài toán sinh viên luyện phỏng vấn rất gần gũi với trải nghiệm cá nhân của mình. Tuy nhiên, sau khi Thành và Nhung chỉ ra điểm yếu chí mạng về việc khó đo lường success metric và khó xây dựng quy trình chuẩn hóa doanh nghiệp, cả nhóm đã cùng chấm điểm khách quan qua ma trận 7 tiêu chí. Kết quả cho thấy bài toán của BA (Candidate 2) vượt trội về tính khả thi, baseline đo được và giá trị kinh doanh. Quân đã hoàn toàn bị thuyết phục và đồng thuận chọn Candidate 2, đồng thời nhận trách nhiệm chính phụ trách vẽ sơ đồ quy trình chi tiết trước/sau ở CP5.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
