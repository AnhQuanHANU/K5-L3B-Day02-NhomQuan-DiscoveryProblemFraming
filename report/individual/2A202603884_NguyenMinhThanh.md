# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Minh Thành
- MSSV: 2A202603884
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: NhomQuan
- Link repo nhóm: https://github.com/AnhQuanHANU/K5-L3-Day02-NhomQuan-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại |Khi bắt đầu tuần mới vào sáng thứ Hai, tôi muốn tổng hợp kết quả huấn luyện mô hình và lỗi log của tuần trước vào một chỗ, để báo cáo tiến độ cho tech lead trước 10h |Junior Dev / ML Engineer | Tự bấm giờ 2 tuần gần nhất: mất 75 và 90 phút|
| 2 | Tốn thời gian|Khi cần tìm lại quyết định thiết kế kiến trúc từ các đoạn chat cũ trên Slack/Discord, tôi muốn tìm đúng thread có kết luận, để không phải tranh luận lại từ đầu |Cả team kỹ thuật | Mất 15–20 phút mỗi lần tìm, xảy ra 3–4 lần/tuần|
| 3 | Tốn thời gian|Khi nhận một tài liệu kỹ thuật (RFC/API Spec) dài 20–30 trang cần review, tôi muốn nắm nhanh các điểm thay đổi chính, để kịp góp ý trước hạn |Reviewer / Dev |Khoảng 50 phút/tài liệu, 2 tài liệu/tuần |
| 4 | Cần đọc, tổng hợp nhiều thông tin|Khi kết quả chạy thử nghiệm (experiment) sinh ra hàng loạt file metrics và log rời rạc, tôi muốn tổng hợp chúng thành bảng so sánh trực quan, để biết mô hình nào tối ưu hơn |Data Analyst / ML Dev | Mất khoảng 40 phút cho mỗi vòng experiment|
| 5 | Pain từ người khác| Khi QA gửi bug report thiếu bước tái hiện (reproduce), tôi muốn họ cung cấp đủ log và môi trường, để không mất thời gian hỏi lại|Dev, QA |QA hỏi/nhắn lại 2–3 lần mỗi ticket (đếm trên Jira) |
| 6 | Lặp lại| Khi tạo môi trường phát triển mới cho các thành viên tham gia project, tôi muốn chạy một script tự động cài đặt các dependency, để không phải hướng dẫn thủ công từng bước| Tech Lead, Dev mới| Mất 30–45 phút mỗi lần onboarding thành viên mới|
| 7 | | | | |
| 8 | | | | |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Tổng hợp báo cáo thử nghiệm & tiến độ tuần (#1) |Quy trình lặp lại hằng tuần, tốn thời gian, có baseline đo thực tế | Phần đánh giá chất lượng nhận định tự động đo thế nào?|
| 2 | Tìm lại quyết định thiết kế cũ (#2)|Pain chung của cả team, tốn thời gian |Quyền truy cập và phân loại dữ liệu chat lịch sử phức tạp |
| 3 |Review tài liệu kỹ thuật dài (#3) | Tốn nhiều thời gian đọc hiểu| Chất lượng review phụ thuộc nhiều vào ngữ cảnh dự án|

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi bắt đầu tuần mới vào sáng thứ Hai, tôi muốn tổng hợp kết quả huấn luyện mô hình và log lỗi của tuần trước vào một chỗ, để báo cáo tiến độ cho tech lead trước 10h. |
| Actor | Junior ML Engineer / Software Developer |
| Thời điểm / bối cảnh | Sáng thứ Hai hàng tuần, từ 8h30 đến 10h00 trước giờ họp sync với team leadership. |
| Quy trình hiện tại (3–7 bước) | 1. Export log & metrics từ MLflow/W&B · 2. Lấy số liệu sprint từ Jira/GitLab · 3. Tổng hợp dữ liệu thô vào Google Docs · 4. Viết tóm tắt nhận định (narrative) · 5. Review & chỉnh sửa format · 6. Gửi báo cáo cho Tech Lead |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 — Viết tóm tắt nhận định: mất 30 phút/lần do phải đọc dữ liệu thô và biến thành văn bản tổng hợp. |
| Impact (nếu không giải thì sao) | Mất 80 phút/tuần; 3/8 tuần gần nhất bị gửi trễ báo cáo, gây ảnh hưởng đến kế hoạch họp của lead. |
| Success metric (baseline → target) | Tổng thời gian lập báo cáo giảm từ 80 phút xuống dưới 30 phút, tỷ lệ báo cáo đúng hạn đạt 100%. |
| Phương án không dùng AI | Dùng template Markdown cố định + tạo dashboard tự động kéo số liệu từ Jira/MLflow vào Sheet. |
| Giả thuyết về AI (nếu có) | AI tổng hợp log/metrics đã kéo về để soạn nháp phần nhận định; con người review và chỉnh sửa trước khi gửi. |
| Cảm nhận nhanh | Workflow |

**Quy trình nháp hiện tại:**

```text
HIỆN TẠI — 80 phút/tuần

[1 Export Log/Metrics: 15'] → [2 Lấy số Jira/GitLab: 10'] → [3 Gom vào Docs: 10']
→ [4 Viết nhận định narrative: 30'] ← BOTTLENECK
→ [5 Review & format: 10'] → [6 Gửi email báo cáo: 5']
```

---

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần xem lại nguyên nhân đưa ra quyết định kỹ thuật cũ trên Slack/Discord, tôi muốn tìm đúng thread có kết luận cuối cùng, để không phải tranh luận lại từ đầu. |
| Actor | Software Engineer, System Architect |
| Thời điểm / bối cảnh | Trong quá trình refactor code hoặc khi phát sinh tranh luận kiến trúc giữa các thành viên. |
| Quy trình hiện tại (3–7 bước) | 1. Đánh từ khóa tìm kiếm trên kênh Slack/Discord · 2. Lướt qua hàng loạt kết quả · 3. Đọc lại toàn bộ từng thread liên quan · 4. Tóm tắt lại quyết định cho team |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 — Đọc lại cả thread dài để lọc ra kết luận chính: mất 15–20 phút/lần. |
| Impact (nếu không giải thì sao) | Mất 45–60 phút/tuần cho 1 dev; dễ đưa ra quyết định sai hoặc tốn thời gian họp lại về vấn đề đã chốt. |
| Success metric (baseline → target) | Thời gian tìm ra kết luận giảm từ 15 phút xuống dưới 2 phút/lần. |
| Phương án không dùng AI | Quy định ghi chép ADR (Architecture Decision Record) cố định trên Notion/Confluence và chèn link vào Slack header. |
| Giả thuyết về AI (nếu có) | AI tóm tắt nội dung thread chat được gắn tag/search và trích xuất ra đúng câu kết luận chính kèm link gốc. |
| Cảm nhận nhanh | Workflow hoặc Agent |

**Quy trình nháp hiện tại:**

```text
HIỆN TẠI — 15–20 phút/lần tìm

[1 Search keyword: 2'] → [2 Lướt kết quả: 3'] 
→ [3 Đọc toàn bộ thread dài: 10'] ← BOTTLENECK
→ [4 Tóm tắt lại cho team: 3']
```

---

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận được một tài liệu kỹ thuật (RFC/API Spec) dài 20–30 trang trước buổi review, tôi muốn nắm nhanh các thay đổi kiến trúc chính, để kịp chuẩn bị câu hỏi phản biện. |
| Actor | Senior Dev, Code Reviewer, Technical Lead |
| Thời điểm / bối cảnh | 1–2 ngày trước buổi họp RFC Review định kỳ. |
| Quy trình hiện tại (3–7 bước) | 1. Tải tài liệu spec · 2. Đọc lướt qua cấu trúc · 3. Đọc chi tiết từng phần · 4. Ghi chú các điểm mơ hồ hoặc rủi ro · 5. Viết comment review |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 — Đọc chi tiết toàn bộ tài liệu dài: mất 35 phút/bản. |
| Impact (nếu không giải thì sao) | Mất 50 phút/bản (2 bản/tuần); nguy cơ bỏ sót các rủi ro kiến trúc quan trọng do đọc lướt khi thiếu thời gian. |
| Success metric (baseline → target) | Thời gian nắm ngữ cảnh và chuẩn bị comment giảm từ 50 phút xuống 20 phút/bản. |
| Phương án không dùng AI | Yêu cầu tác giả RFC bắt buộc phải có phần Executive Summary (tóm tắt cho người quản lý) ở 1 trang đầu. |
| Giả thuyết về AI (nếu có) | AI đọc RFC và tạo bản so sánh diff/tóm tắt điểm thay đổi quan trọng theo checklist tiêu chuẩn của team. |
| Cảm nhận nhanh | Workflow |

**Quy trình nháp hiện tại:**

```text
HIỆN TẠI — 50 phút/bản

[1 Tải spec: 2'] → [2 Đọc lướt: 5'] 
→ [3 Đọc chi tiết 20-30 trang: 35'] ← BOTTLENECK
→ [4 Ghi chú rủi ro: 5'] → [5 Viết comment: 3']
```

---

### Card muốn pitch nhất

- **Card số:** 1 (Tổng hợp biên bản workshop lấy yêu cầu với khách hàng)
- **Vì sao:** Bài toán có quy trình thực tế rõ ràng (xảy ra ngay sau mỗi buổi workshop), thời gian tốn kém lớn (~90 phút/buổi), có bằng chứng/baseline đo đạc được ngay và có rủi ro về sai lệch yêu cầu cao nếu không có người kiểm duyệt (cần human-in-the-loop làm boundary).
- **Câu hỏi muốn nhóm phản biện:** 
  1. Nếu chỉ dùng Template biên bản cố định + ghi âm/transcript có sẵn (No AI/Rule) thì đã giảm được bao nhiêu % thời gian tốn kém?
  2. Làm sao để thiết lập tiêu chuẩn kiểm tra (eval/boundary) nhằm đảm bảo AI không "bịa" ra các quyết định hoặc yêu cầu mà khách hàng chưa từng phát biểu trong buổi workshop?

---

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| AI cho rằng baseline 90 phút chỉ dựa trên ước lượng cảm tính chứ chưa có con số theo dõi cụ thể. | Đồng ý | Bổ sung ghi chép đo đạc thực tế từ 2 buổi workshop gần nhất (85 phút và 95 phút, lấy trung bình 90 phút). |
| AI gợi ý xây Agent tự động gửi biên bản trực tiếp qua email cho khách hàng ngay khi workshop kết thúc. | Không đồng ý | Giữ bắt buộc bước BA review, đối chiếu ghi chú và duyệt nội dung (Human-in-the-loop) làm Boundary trước khi gửi email cho khách.|
| Metric ban đầu mới chỉ đo tốc độ tạo biên bản, chưa đo chất lượng và mức độ chính xác của yêu cầu. | Đồng ý | Bổ sung metric chất lượng: Tỷ lệ câu hỏi chỉnh sửa/phản hồi lại từ khách hàng sau khi nhận biên bản không tăng so với trước đây.s |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày Problem Card #1 (Báo cáo tiến độ tuần) | Thuyết phục nhóm lựa chọn bài toán làm candidate chính cho bài nhóm |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt cho bài của Phương Nhung: *"Nếu khách hàng không xem biên bản hoặc phản hồi chậm thì làm sao?"* | Giúp nhóm bổ sung thêm rủi ro về Usability và boundary kiểm soát trong bài nhóm |
| Nhận phản biện | Câu hỏi tôi nhận được từ nhóm: *"Nếu chỉ cần số liệu thì dùng Dashboard Script đã đủ chưa?"* | Tôi đã sửa gì: Thêm phương án No AI/Rule vào báo cáo và làm rõ AI chỉ hỗ trợ phần nhận định (narrative) |
| Gom cluster / cây OST | Cùng nhóm gom 12 candidate thành 4 cluster chính | Xây dựng nhánh Opportunity 2 trong cây OST: "Viết phần nhận định tốn thời gian nhất" |
| Chọn candidate problem | Thảo luận và đánh giá shortlist theo 7 tiêu chí | Chọn đề tài Biên bản/Báo cáo sau workshop với tổng điểm cao nhất (34 điểm) |
| Kiểm chứng / research | Phỏng vấn 1 BA và tìm kiếm giải pháp có sẵn (Atlassian Rovo, Slack AI) | Giúp nhóm chuyển từ tư duy "tự xây app" sang "dùng tool có sẵn + quy trình chuẩn" |
| Quy trình nhóm | Trực tiếp phác thảo và vẽ sơ đồ quy trình Hiện tại & Tương lai bằng Mermaid | Được sử dụng làm sơ đồ chuẩn trong báo cáo nhóm |
| Problem Statement | Phản biện 6 trường trong Problem Statement v0 | Bổ sung thêm Success Metric về chất lượng nhận định (không bị trễ hạn và không bị hỏi lại) |
| Mức can thiệp AI | Phân tích ma trận Độ mơ hồ x Độ phức tạp | Nhóm thống nhất chọn mức **Workflow** thay vì Agent phức tạp |
| Quyết định | Đánh giá 4 rủi ro (Value, Usability, Feasibility, Viability) | Chốt quyết định **Go, phạm vi nhỏ** và xây dựng điều kiện dừng (Exit Criteria) |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm các nỗi đau theo lăng kính tốn thời gian | Nhắc tôi nhớ ra các bài toán như onboarding dev mới hay bug report từ QA | Đề xuất giải pháp quá rộng kiểu "Trợ lý AI quản lý toàn bộ dự án" | Bỏ các gợi ý thiếu quy trình, chỉ giữ lại các bài toán có thể đo đạc |
| CP2 Problem Card | Đóng vai reviewer phản biện Problem Card | Chỉ ra điểm yếu về baseline thời gian chỉ dựa vào trí nhớ | Gợi ý tự động hóa 100% (cho AI tự gửi báo cáo không qua người kiểm) | Đặt ra Boundary bắt buộc: AI chỉ soạn nháp, con người review trước khi gửi |
| CP4 Research | Tìm kiếm các công cụ đã giải bài toán tương tự | Tìm ra Atlassian Rovo, Slack AI và các template n8n | Trích dẫn sai tính năng của gói Slack AI Pro và đưa link tham khảo bị chết | Tự mở từng link kiểm chứng, đọc bảng giá thực tế của Slack và Jira |
| CP5 Quy trình | Chuyển mô tả văn bản thành khối code Mermaid | Chuyển đổi nhanh sơ đồ Mermaid chuẩn cú pháp | AI tự động gộp bước "Viết nhận định" và "Review" thành 1 bước duy nhất | Tách riêng 2 bước vì bottleneck thực sự nằm ở khâu soạn thảo nhận định |
| CP5–6 Problem Statement | Phản biện 6 trường trong Problem Statement v0 | Chỉ ra Success Metric ban đầu chỉ đo tốc độ mà thiếu đo lường chất lượng | Gợi ý đưa công cụ AI vào luôn trong phần mô tả Problem Statement | Loại bỏ tên công cụ AI khỏi Problem Statement để giữ đúng tinh thần problem-first |
| CP6 Mức can thiệp / quyết định | Đóng vai Product Manager chọn mức can thiệp | Gợi ý cách phân tích theo 4 mức (No AI, Rule, Workflow, Agent) | AI cố gắng đẩy bài toán lên mức Agent phức tạp không cần thiết | Chọn mức Workflow vì quy trình có các bước cố định, không cần AI tự quyết định luồng đi |

---

## 6. Reflection (CP7)

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Khi nghe bài trình bày của các bạn khác trong nhóm, tôi nhận ra bài toán không chỉ tồn tại ở góc nhìn kỹ thuật của một Developer mà còn xuất hiện rõ nét ở góc độ nghiệp vụ của Business Analyst (BA) hay Product Owner (PO). Bạn Phương Nhung mang đến bài toán tổng hợp biên bản sau workshop với khách hàng vô cùng thực tế: BA phải mất đến 90 phút để nghe lại file ghi âm và nhặt từng ý thô thành biên bản. Điều này giúp tôi mở rộng tầm nhìn, hiểu rằng dù ở vai trò nào thì nút thắt lớn nhất vẫn luôn nằm ở bước "chuyển đổi dữ liệu thô lộn xộn thành văn bản nhận định có cấu trúc cho người khác đọc".

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Nhóm tôi đã bị dính lỗi "solution-first" ngay từ giai đoạn thảo luận ban đầu. Vừa chốt xong ý tưởng báo cáo, các thành viên đã hào hứng bàn về việc "dùng OpenAI API nào", "xây ứng dụng web ra sao" hay "cho AI tự gửi email tự động". Nhóm nhận ra điều này khi vẽ Cây Opportunity Solution Tree (OST), phát hiện ra nhiều ô ở tầng Opportunity chứa đầy các từ khóa như "Chatbot AI" hay "Dashboard tự động". Nhóm đã lập tức xử lý bằng cách tuân thủ nghiêm ngặt quy tắc OST: gạch bỏ toàn bộ tên công cụ và tính năng ra khỏi tầng Opportunity, ép cả nhóm phải quay lại mô tả chính xác nỗi đau của người dùng là "mất quá nhiều thời gian tổng hợp ghi chú thô".

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi đã đổi ý hoàn toàn ở bước xác định giải pháp công nghệ. Ban đầu, tôi khẳng định chắc chắn nhóm phải tự lập trình một công cụ AI riêng để xử lý báo cáo. Tuy nhiên, khi bị các bạn phản biện về tính khả thi (Feasibility) và sau khi làm research ở CP4, tôi nhận ra Jira đã có tính năng Rovo, Slack có tính năng tóm tắt thread và n8n đã có sẵn các template tự động hóa. Tôi nhận ra việc tự xây ứng dụng là lãng phí và nhiều rủi ro. Tôi đã đổi ý và đề xuất nhóm chuyển hướng sang dùng công cụ có sẵn kết hợp với quy trình chuẩn hóa và prompt tối ưu.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Điều làm tôi bất ngờ nhất khi thực hiện phỏng vấn (dựa theo The Mom Test) là có 1/3 người được hỏi chia sẻ rằng phía Quản lý/CEO của họ... không hề đọc phần chữ nhận định (narrative), mà chỉ xem đúng các con số trên Dashboard! Trước đó, tôi luôn mặc định rằng sếp nào cũng cần đọc nhận định chi tiết. Insight này cho thấy bài toán không áp dụng cho 100% mọi team. Nhờ đó, nhóm tôi đã kịp thời điều chỉnh Problem Statement, thu hẹp nhóm đối tượng người dùng (Actor) thành "Junior PM/BA ở các team mà Leadership thực sự yêu cầu và đọc phần nhận định narrative".

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Điều khó nhất đối với tôi là việc thiết lập **Boundary (Biên giới an toàn)** và **Success Metric (Thước đo thành công)** mà không bị lẫn giải pháp vào đó. Viết một Success Metric đo tốc độ thì dễ (giảm từ 90 phút xuống 20 phút), nhưng để viết thước đo chất lượng đầu ra mà AI tạo ra (tránh bịa số liệu, tránh bỏ sót rủi ro) đòi hỏi phải suy nghĩ rất kỹ về tiêu chuẩn "thế nào là một đầu ra đạt". Việc giữ cho Problem Statement không chứa bất kỳ từ ngữ nào liên quan đến AI hay công cụ cụ thể cũng là một thử thách lớn đòi hỏi sự kiềm chế tư duy giải pháp.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu được làm lại từ đầu, tôi sẽ thúc đẩy nhóm tiến hành phỏng vấn đối tượng người dùng thật ngay từ giai đoạn CP1 thay vì đợi đến CP4. Việc kiểm chứng sớm từ thực tế sẽ giúp nhóm tiết kiệm rất nhiều thời gian tranh luận cảm tính ở CP2 và CP3. Ngoài ra, tôi sẽ phản biện nhóm mạnh hơn ở giả định về quyền riêng tư dữ liệu (Viability/Privacy): khi đưa thông tin ghi âm workshop hoặc dữ liệu dự án vào công cụ AI, rủi ro bảo mật là cực kỳ lớn. Tôi sẽ ép nhóm phải làm rõ điều khoản an toàn dữ liệu trước khi đưa ra quyết định "Go".

**6.7. Hiểu bài:**
Chuỗi tư duy của nhóm bắt đầu từ **Problem**: BA/PM mất 80–90 phút mỗi tuần để biến dữ liệu thô lộn xộn thành nhận định báo cáo chuẩn. Phân tích **Quy trình** cho thấy điểm nghẽn (bottleneck) lớn nhất nằm ở khâu soạn thảo văn bản narrative thủ công. Để giải quyết, nhóm xác định **Metric** rõ ràng: giảm tổng thời gian xuống dưới 30 phút mà tỷ lệ phải viết lại nháp dưới 50%. Nhằm đảm bảo an toàn, **Boundary** được thiết lập nghiêm ngặt: AI tuyệt đối không tự gửi báo cáo và không được tự đưa ra nhận định không có nguồn gốc từ dữ liệu thô. Từ phân tích ma trận độ mơ hồ cao và độ phức tạp trung bình, nhóm chọn **Mức can thiệp AI** là **Workflow** (kết hợp Rule tự động kéo dữ liệu và AI soạn nháp dưới sự duyệt của con người). Cuối cùng, **Quyết định** được đưa ra là "Go ở phạm vi thử nghiệm nhỏ" kèm theo ngưỡng dừng (Exit Criteria) an toàn nếu tỷ lệ nháp sai vượt mức cho phép.

---

## 7. Tài liệu tham khảo

- 