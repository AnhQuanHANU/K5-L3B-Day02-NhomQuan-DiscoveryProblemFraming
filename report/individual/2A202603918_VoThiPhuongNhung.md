# Báo cáo cá nhân — 2A202603918_VoThiPhuongNhung

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Võ Thị Phương Nhung
- MSSV: 2A202603918
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: NhomQuan
- Link repo nhóm: https://github.com/AnhQuanHANU/K5-L3-Day02-NhomQuan-DiscoveryProblemFraming 

---
Nhân vật: Nhung, Business Analyst (BA) ở một công ty quy mô vừa. Mỗi tuần Nhung tham gia khoảng 2 buổi workshop để lấy yêu cầu từ khách hàng. Sau mỗi buổi, Nhung viết biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, rồi gửi khách xác nhận trong ngày.

Vì sao chọn bài này:

Actor cụ thể: BA phụ trách lấy yêu cầu từ khách hàng.
Quy trình lặp lại: diễn ra sau mỗi buổi workshop, khoảng 2 lần/tuần.
Bottleneck rõ: bước tách yêu cầu, quyết định và câu hỏi mở từ ghi chú lộn xộn.
Có baseline thời gian: khoảng 105 phút/biên bản, đo được bằng cách tự bấm giờ các buổi tiếp theo.
So sánh được 4 mức:
No AI: template biên bản + một người chuyên ghi chép.
Rule: template tự điền sẵn thông tin buổi họp và người tham dự.
Workflow: AI chép lời và soạn nháp biên bản, BA đối chiếu rồi gửi.
Agent: AI tự đối chiếu với yêu cầu cũ và tự gửi cho khách.

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi khách hàng gửi yêu cầu thay đổi (CR), tôi muốn biết nhanh CR ảnh hưởng tới chức năng, màn hình, tài liệu nào, để báo PM effort và rủi ro đúng hạn | BA, PM, Dev lead | 2–3 CR/tuần, 40–60 phút/CR |
| 2 | Tốn thời gian | Khi vừa kết thúc workshop lấy yêu cầu với khách hàng, tôi muốn có biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, để gửi khách xác nhận trong ngày | BA, khách hàng, PM | 2 buổi/tuần, khoảng 105 phút/biên bản |
| 3 | Cần đọc, tổng hợp nhiều thông tin | Khi nhận bộ tài liệu nghiệp vụ của khách (nhiều file, nhiều phiên bản), tôi muốn nắm nhanh quy trình hiện tại (as-is), để chuẩn bị câu hỏi cho workshop | BA | 2–3 tiếng/phân hệ mới |
| 4 | Lặp lại | Khi chuyển yêu cầu đã chốt thành user story, tôi muốn viết đủ acceptance criteria, để dev ước lượng và làm đúng ngay | BA, Dev | 15–20 phút/story, 8–10 story/tuần |
| 5 | Pain từ người khác | Khi dev đọc đặc tả (SRS/FSD) của tôi, họ muốn hiểu đúng ngay lần đầu, để không phải hỏi lại | Dev, BA | 3–5 câu hỏi lại/đặc tả, đếm trong group chat dự án |
| 6 | Pain từ người khác | Khi tester viết test case, họ muốn có kịch bản bám sát yêu cầu, để không sót trường hợp | Tester, BA | 2–3 bug/sprint do hiểu sai yêu cầu, đếm trên công cụ quản lý bug |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi khách hỏi "yêu cầu X đã làm chưa", tôi muốn truy được yêu cầu → tài liệu → ticket → trạng thái, để trả lời ngay | BA, khách hàng, PM | 10–15 phút/lần, 3–4 lần/tuần |
| 8 | Tốn thời gian | Khi một CR đã được duyệt, tôi muốn cập nhật đồng bộ SRS, mockup và ticket, để các tài liệu không lệch nhau | BA, Dev, Tester | 30–45 phút/CR |
| 9 | Lặp lại | Khi đã gửi nhiều câu hỏi cho khách, tôi muốn biết câu nào quá hạn chưa được trả lời, để nhắc khách trước khi dev bị chặn | BA, PM, Dev | 5–10 câu hỏi mở/tuần, kiểm tra 15 phút/ngày |
| 10 | Tốn thời gian | Khi chuẩn bị UAT, tôi muốn có kịch bản và dữ liệu mẫu theo nghiệp vụ, để khách test đúng luồng | BA, khách hàng | 1–2 ngày/đợt UAT |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Bỏ ý "AI tự viết toàn bộ SRS từ đầu" vì quá rộng, không gắn với một bước cụ thể để đo.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Biên bản workshop lấy yêu cầu (#2) | Quy trình rõ, lặp lại sau mỗi buổi workshop, dễ bấm giờ | Khách hàng có cho ghi âm và đưa nội dung họp vào công cụ AI không? |
| 2 | Phân tích ảnh hưởng CR (#1) | Ảnh hưởng trực tiếp tới estimate và tiến độ dự án | Tài liệu rải rác nhiều nơi; chất lượng phân tích khó đo |
| 3 | Dev hỏi lại đặc tả (#5) | Nhiều người bị ảnh hưởng, đếm được số câu hỏi | Nguyên nhân có thể nằm ở quy trình review, không chỉ ở cách viết |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi vừa kết thúc workshop lấy yêu cầu với khách hàng, tôi muốn có biên bản gồm yêu cầu, quyết định, câu hỏi mở và việc cần làm, để gửi khách xác nhận trong ngày |
| Actor | BA phụ trách lấy yêu cầu từ khách hàng hoặc stakeholder nghiệp vụ |
| Thời điểm / bối cảnh | Ngay sau mỗi buổi workshop (2 buổi/tuần), cần gửi trước cuối ngày |
| Quy trình hiện tại (3–7 bước) | 1. Ghi chú trong buổi họp · 2. Nghe lại bản ghi ở những đoạn chưa rõ · 3. Gõ lại ghi chú thành bản sạch · 4. Tách yêu cầu, quyết định, câu hỏi mở, action item · 5. Đối chiếu với yêu cầu cũ để tìm trùng lặp hoặc mâu thuẫn · 6. Format theo template biên bản · 7. Gửi email cho khách xác nhận |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4, tách ý từ ghi chú lộn xộn: khoảng 30 phút, hay sót ý khi khách nói nhanh hoặc nói vòng |
| Impact (nếu không giải thì sao) | Khoảng 105 phút/buổi × 2 buổi/tuần ≈ 210 phút/tuần; số lần khách phản hồi biên bản sai/thiếu ý; dev phải chờ yêu cầu được chốt |
| Success metric (baseline → target) | Thời gian 105 phút → dưới 40 phút; số điểm khách yêu cầu sửa trong biên bản không tăng; ít nhất 90% biên bản gửi trong ngày |
| Phương án không dùng AI | Template biên bản chia sẵn 4 mục, ghi chú thẳng vào template trong buổi họp, phân công một người chuyên ghi chép. Giảm thời gian gõ lại và format, nhưng chưa bớt được việc nghe lại bản ghi và tách ý |
| Giả thuyết về AI (nếu có) | AI chép lời từ bản ghi, rồi soạn nháp biên bản theo template từ bản chép lời và ghi chú. BA đối chiếu, sửa, sau đó mới gửi |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 105 phút

[1 Ghi chú trong họp: không tính] → [2 Nghe lại bản ghi: 25'] → [3 Gõ lại ghi chú: 15']
→ [4 Tách yêu cầu / quyết định / câu hỏi / action: 30'] ← BOTTLENECK
→ [5 Đối chiếu yêu cầu cũ: 20'] → [6 Format: 10'] → [7 Gửi email: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi khách hàng gửi yêu cầu thay đổi (CR), tôi muốn biết nhanh CR ảnh hưởng tới chức năng, màn hình, tài liệu nào, để báo PM effort và rủi ro đúng hạn |
| Actor | BA tiếp nhận và phân tích CR từ khách hàng |
| Thời điểm / bối cảnh | Khi có CR mới (2–3 CR/tuần), cần phản hồi PM trong 1–2 ngày |
| Quy trình hiện tại (3–7 bước) | 1. Đọc CR, hỏi lại khách nếu mơ hồ · 2. Tìm chức năng, màn hình liên quan trong SRS · 3. Tìm ticket và luồng nghiệp vụ liên quan trong Devops· 4. Hỏi dev lead về ảnh hưởng kỹ thuật · 5. Viết bảng phân tích ảnh hưởng (chức năng, tài liệu, rủi ro) · 6. Gửi PM để estimate |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2–3, tìm chức năng và ticket liên quan: khoảng 25 phút, vì tài liệu rải rác, nhiều phiên bản, chưa có liên kết truy vết |
| Impact (nếu không giải thì sao) | Khoảng 50 phút/CR × 2–3 CR/tuần ≈ 100–150 phút/tuần; sót ảnh hưởng thì estimate thiếu, phát sinh effort hoặc bug sau; 10 lần CR bị estimate thiếu do sót ảnh hưởng gần đây |
| Success metric (baseline → target) | Thời gian 50 phút/CR → dưới 20 phút; số ảnh hưởng bị sót (phát hiện sau khi estimate) không tăng |
| Phương án không dùng AI | Duy trì ma trận truy vết yêu cầu (RTM) nối yêu cầu – màn hình – ticket, kèm checklist phân tích ảnh hưởng. Giảm thời gian tìm nếu RTM được cập nhật đều, nhưng tốn công duy trì |
| Giả thuyết về AI (nếu có) | AI đọc CR và bộ tài liệu dự án, đề xuất danh sách chức năng, tài liệu, ticket có thể bị ảnh hưởng kèm nguồn; BA kiểm tra và bổ sung |
| Cảm nhận nhanh | Workflow hoặc Agent |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 50 phút/CR 

[1 Đọc CR: 5'] → [2 Tìm trong SRS: 15'] → [3 Tìm ticket liên quan: 10']   ← BOTTLENECK (bước 2–3)
→ [4 Hỏi dev lead: 5', chưa tính thời gian chờ] → [5 Viết bảng phân tích: 10'] → [6 Gửi PM: 5']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi dev đọc đặc tả (SRS/FSD) của tôi, họ muốn hiểu đúng ngay lần đầu, để không phải hỏi lại |
| Actor | BA viết đặc tả; dev là người chịu ảnh hưởng trực tiếp |
| Thời điểm / bối cảnh | Khi bàn giao đặc tả cho dev, đầu mỗi sprint hoặc mỗi tính năng mới |
| Quy trình hiện tại (3–7 bước) | 1. Viết đặc tả theo template · 2. Tự review · 3. Gửi dev hoặc tổ chức buổi walkthrough · 4. Dev đọc và hỏi lại qua group chat · 5. BA trả lời và sửa đặc tả · 6. Lặp lại bước 4–5 đến khi dev hiểu |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5, vòng hỏi đáp: 3–5 câu hỏi/đặc tả, khoảng 30 phút trả lời và sửa. Không phải bước lâu nhất, nhưng là phần làm lại và chặn dev. Phân loại các câu hỏi gần nhất xem 10 câu do thiếu edge case |
| Impact (nếu không giải thì sao) | Dev chờ câu trả lời nên bắt đầu chậm; hiểu sai dẫn tới bug (2–3 bug/sprint); BA bị ngắt quãng công việc |
| Success metric (baseline → target) | Câu hỏi lại/đặc tả từ 4 → dưới 2; số bug do hiểu sai yêu cầu không tăng |
| Phương án không dùng AI | Checklist review đặc tả (edge case, phân quyền, dữ liệu lỗi, trạng thái) + peer review với BA khác hoặc dev lead trước khi bàn giao |
| Giả thuyết về AI (nếu có) | AI review bản nháp đặc tả theo checklist, chỉ ra chỗ mơ hồ và edge case còn thiếu trước khi gửi dev; BA quyết định sửa gì |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — khoảng 135 phút/đặc tả 

[1 Viết đặc tả: 60'] → [2 Tự review: 15'] → [3 Walkthrough với dev: 30']
→ [4–5 Dev hỏi lại + BA trả lời, sửa: 30'] ← BOTTLENECK (phần làm lại)
→ [6 Lặp lại 4–5 nếu còn câu hỏi]
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: quy trình rõ, lặp lại 2 lần/tuần , tự bấm giờ được ngay từ buổi workshop tiếp theo, so sánh được 4 mức No AI / Rule / Workflow / Agent
- Câu hỏi muốn nhóm phản biện: Nếu dùng template + một người chuyên ghi chép (No AI), bước tách ý có còn là bottleneck không? Khách hàng của các bạn có cho ghi âm và đưa nội dung họp vào công cụ AI không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 105 phút là ước lượng, chưa đo | Đồng ý | Bấm giờ 2–3 buổi workshop gần nhất |
| Bước "nghe lại bản ghi" có thể chỉ tồn tại vì ghi chú chưa tốt; phương án người ghi chép riêng có thể đã đủ | Đồng ý | Đưa vào câu hỏi phỏng vấn ở CP4 để kiểm phương án No AI |
| Chưa rõ khách có cho ghi âm và đưa nội dung họp vào công cụ AI không (rủi ro bảo mật) | Đồng ý | Ghi vào danh sách giả định Viability cần kiểm ở CP4 |
| AI chép lời có thể sai thuật ngữ nghiệp vụ và tên riêng tiếng Việt | Đồng ý | Giữ boundary "BA đối chiếu trước khi gửi"; thêm tiêu chí "không sai thuật ngữ" |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Đưa ra bài toán về việc BA cần hoàn thiện biên bản sau workshop lấy yêu cầu với khách hàng. Trình bày actor, bối cảnh, tần suất, bottleneck và mục tiêu gửi biên bản trong ngày. | Candidate được đưa vào shortlist và cuối cùng được nhóm lựa chọn. Bài toán có actor và quy trình rõ, lặp lại khoảng 2 buổi/tuần, có thể đo thời gian hoàn thành biên bản. |
| Phản biện bài của bạn khác | Đặt câu hỏi cho các candidate của Quân: câu hỏi phỏng vấn sinh từ JD có sát thực tế phỏng vấn không; Trello/Notion đã có Kanban và notification thì vấn đề theo dõi task nằm ở công cụ hay ý thức thành viên? | Giúp nhóm xem xét liệu vấn đề có thực sự cần AI hay có thể giải quyết bằng công cụ/rule sẵn có. |
| Nhận phản biện | Tôi nhận câu hỏi từ Thành về việc khách hàng có cho phép ghi âm và đưa nội dung workshop vào công cụ AI hay không, đặc biệt khi có thông tin mật và NDA. | Tôi nhận thấy bảo mật là giả định quan trọng cần kiểm chứng. Nhóm thống nhất không dùng bot AI tham gia phòng họp; chỉ tiếp nhận transcript hoặc ghi chép do BA chủ động tải lên và phải có cơ chế bảo vệ dữ liệu. |
| Gom cluster / cây OST | Tham gia thảo luận và thống nhất gom các candidate theo pattern chung. Bài toán biên bản workshop được xếp vào Cluster C — Tổng hợp dữ liệu quy mô lớn và tạo biên bản/báo cáo định kỳ. | Cây OST tập trung vào outcome rút ngắn thời gian phát hành biên bản từ 90 phút xuống dưới 25 phút, đồng thời giữ tỷ lệ bỏ sót quyết định dưới 5%. Các opportunity chính gồm thời gian nghe lại recording, khó phân biệt quyết định với ý kiến thảo luận, nguy cơ gửi biên bản trễ và rào cản bảo mật. |
| Chọn candidate problem | Bảo vệ candidate biên bản workshop bằng các tiêu chí: actor rõ, quy trình chuẩn hóa, pain có bằng chứng, impact đo được và có thể so sánh No AI/Rule/Workflow/Agent. | Candidate của tôi đạt 34/35 điểm trong bảng shortlist và được chọn làm bài toán chung. Quyết định cuối của nhóm là Go với điều kiện Workflow có Human-in-the-loop. |
| Kiểm chứng / research | Phụ trách research CP4: tìm hiểu Otter.ai, Fireflies.ai, Atlassian Intelligence và Granola; so sánh phạm vi hỗ trợ, điểm mạnh, khoảng trống và rủi ro đối với quy trình BA. Tôi phối hợp với phần kiểm chứng do Thành phụ trách. | Nhóm nhận ra các công cụ ghi chú họp có thể hỗ trợ chép lời/tóm tắt nhưng chưa giải quyết đầy đủ việc phân loại theo 4 danh mục nghiệp vụ BA, xử lý Vietlish và yêu cầu đối soát nguồn. Bài học là không đưa bot vào phòng họp và cần gắn timestamp cho nội dung trích xuất. |
| Quy trình nhóm | Hỗ trợ Quân hoàn thiện quy trình trước/sau và góp ý việc phân định vai trò Rule, AI và BA. | Quy trình hiện tại có 5 bước, mất khoảng 90 phút; bước nghe lại recording và phân loại chiếm 65 phút. Quy trình tương lai vẫn giữ 5 bước, sử dụng Rule làm sạch, LLM trích xuất 4 danh mục, BA rà soát theo timestamp và tự phê duyệt trước khi gửi; thời gian kỳ vọng còn 22 phút. |
| Problem Statement | Tham gia góp ý để Problem Statement thể hiện rõ actor BA, quy trình sau workshop, bottleneck, impact, metric và boundary. Thành phụ trách chính việc viết v0/v1. | Problem Statement v1 xác định AI can thiệp ở bước trích xuất/phân loại transcript; mọi nội dung phải có timestamp, không được suy diễn ngoài transcript và không được tự gửi email. |
| Mức can thiệp AI | Tham gia đánh giá bốn mức No AI, Rule, Workflow và Agent; cân nhắc độ mơ hồ cao của hội thoại và mức độ rủi ro khi phát hành biên bản. | Nhóm chọn Workflow: Rule tiền xử lý, LLM trích xuất theo ngữ cảnh, BA kiểm tra và phê duyệt. Không chọn Agent vì AI tự gửi thông tin sai có thể gây tranh chấp với khách hàng. |
| Quyết định | Phụ trách CP6 về đánh giá bốn rủi ro và chốt Go/Not Yet/No-Go; phối hợp với Quân và Thành. | Nhóm quyết định Go có điều kiện: bắt buộc có Human-in-the-loop và tuân thủ Zero Data Retention. Pilot đề xuất trên 5 dự án nội bộ trong 2 tuần, với 3 BA và 10 buổi workshop; dừng nếu thời gian trung bình vẫn trên 45 phút hoặc tỷ lệ bỏ sót quyết định quan trọng vượt 10%. |

### Những nội dung nhóm thống nhất sau CP4–CP6

**Quy trình tương lai được chọn**

```text
[1. BA tải transcript / ghi chép thô lên hệ thống: 2 phút]
                         |
                         v
[2. Rule tiền xử lý, làm sạch và chuẩn hóa timestamp: 1 phút]
                         |
                         v
[3. LLM trích xuất và phân loại 4 danh mục: 2 phút]
                         |
                         v
[4. BA rà soát, đối soát timestamp và chỉnh sửa (HITL): 12 phút]
                         |
                         v
[5. Xuất biên bản; BA duyệt và gửi email: 5 phút]
```

Bốn danh mục đầu ra gồm:
1. Yêu cầu tính năng mới hoặc thay đổi (Requirements).
2. Quyết định đã thống nhất (Agreed Decisions).
3. Câu hỏi mở cần xác nhận thêm (Open Questions).
4. Việc cần làm tiếp theo (Action Items), có người phụ trách và deadline nếu transcript nêu rõ.

**Problem Statement v1 của nhóm**

| Trường | Nội dung |
|---|---|
| Actor | Business Analyst (BA) phụ trách phân tích và chốt yêu cầu phần mềm trong các dự án công nghệ |
| Quy trình | Sau workshop 2–3 tiếng: tải transcript thô lên hệ thống → Rule làm sạch và định dạng → AI Workflow trích xuất, phân loại 4 mục kèm timestamp → BA rà soát, đối soát và chỉnh sửa → xuất biên bản chuẩn, BA gửi khách hàng xác nhận trong ngày |
| Bottleneck | BA rà soát và đối soát các quyết định nghi vấn với timestamp gốc, dự kiến khoảng 12 phút thay cho khoảng 65 phút nghe lại và phân loại thủ công |
| Impact | Tiết kiệm thời gian cho BA; mục tiêu nâng tỷ lệ gửi biên bản trong ngày lên 100%, hạn chế bỏ sót thỏa thuận và nguy cơ scope creep |
| Success Metric | Thời gian hoàn thiện biên bản từ 90 phút xuống dưới 25 phút; tỷ lệ quyết định/action item bị bỏ sót dưới 5%; tỷ lệ biên bản gửi trong ngày đạt 100% |
| Boundary | AI không tự phát hành biên bản hoặc gửi email; không suy diễn yêu cầu ngoài transcript; mọi nội dung trích xuất phải có timestamp; không sử dụng dữ liệu hội thoại để tái huấn luyện mô hình public (Zero Data Retention) |
| AI intervention point | Bước 3: LLM đọc hiểu transcript đã làm sạch và trích xuất, phân loại thành 4 danh mục kèm timestamp |
| Mức chọn | Workflow: Rule tiền xử lý + LLM trích xuất ngữ cảnh + BA phê duyệt |
| Rủi ro và người kiểm tra | AI có thể phân loại nhầm ý kiến thảo luận thành quyết định hoặc xử lý sai thuật ngữ Vietlish; BA phụ trách dự án là người rà soát và phê duyệt cuối cùng |

**Tiêu chí đánh giá đầu ra AI**

| Tiêu chí | Mục tiêu đạt | Trường hợp không đạt |
|---|---|---|
| Decision Recall | Trích xuất ít nhất 95% quyết định đã thống nhất và action item được nêu rõ trong transcript | Bỏ sót quyết định quan trọng ảnh hưởng đến phạm vi tính năng hoặc tiến độ |
| Category Precision | Phân biệt chính xác quyết định đã thống nhất với câu hỏi mở/ý kiến đang thảo luận | Đưa ý kiến chưa chốt vào danh mục quyết định hoặc phân loại ngược lại |
| Traceability / Timestamp | 100% mục trích xuất có timestamp chính xác dẫn đến câu thoại gốc | Thiếu timestamp hoặc timestamp lệch quá 30 giây |
| Hallucination-free | Không tự thêm ràng buộc kỹ thuật, deadline hoặc cam kết không xuất hiện trong transcript | Tự tạo deadline hoặc suy diễn nghiệp vụ không có căn cứ |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Tham khảo AI để mở rộng và rà soát các tình huống công việc có thể trở thành Job Story. | Gợi ý thêm các góc nhìn về công việc BA như phân tích CR, chuẩn bị workshop, viết user story và truy vết yêu cầu. | Một số ý tưởng có phạm vi quá rộng, thiên về đề xuất giải pháp hơn là mô tả một vấn đề cụ thể. | Loại ý tưởng “AI tự viết toàn bộ SRS từ đầu”; giữ các Job Story có actor, bối cảnh, tần suất và dấu hiệu đo lường rõ. |
| CP2 Problem Card | Dùng AI để phản biện Problem Card và rà soát bottleneck, baseline, phương án No AI và giả thuyết AI. | AI chỉ ra những điểm cần kiểm chứng như baseline 105 phút mới là ước lượng, phương án người ghi chép riêng có thể giảm thời gian và rủi ro bảo mật khi dùng recording. | AI chưa thể xác nhận số liệu thực tế hoặc biết chính sách bảo mật của từng khách hàng. | Giữ các điểm phản biện thành câu hỏi cần kiểm chứng; bổ sung điều kiện BA phải đối chiếu thuật ngữ và nội dung trước khi gửi. |
| CP4 Research | Hỗ trợ hệ thống hóa tiêu chí so sánh các công cụ ghi chú/tóm tắt cuộc họp và trình bày khoảng trống của từng giải pháp. | Giúp tổ chức việc so sánh theo bước quy trình, điểm mạnh, hạn chế và bài học áp dụng cho bài toán BA. | Không thể mặc định công cụ nào phù hợp với môi trường doanh nghiệp hoặc đáp ứng NDA chỉ dựa trên mô tả tính năng. | Đối chiếu lại theo nhu cầu của nhóm: không dùng bot tham gia phòng họp, cần đầu vào do BA chủ động cung cấp, phân loại đúng 4 danh mục và có timestamp. |
| CP5 Quy trình | Hỗ trợ diễn đạt và rà soát luồng trước/sau, đặc biệt là việc tách vai trò Rule, LLM và con người. | Làm rõ các bước có thể tự động hóa và vị trí cần giữ kiểm duyệt của BA. | Nếu chỉ mô tả “AI tóm tắt cuộc họp”, quy trình sẽ bỏ qua yêu cầu phân biệt ý kiến với quyết định và không có bằng chứng để kiểm tra. | Thống nhất đầu ra có 4 danh mục, mỗi mục có timestamp; BA rà soát ở bước 4 và là người duyệt gửi ở bước 5. |
| CP5–6 Problem Statement | Hỗ trợ rà soát tính nhất quán giữa actor, bottleneck, impact, success metric và boundary. | Giúp phát hiện những phần còn chung chung và đề xuất diễn đạt rõ điểm AI can thiệp trong Workflow. | AI có thể đưa ra mục tiêu hoặc số liệu nghe hợp lý nhưng chưa có bằng chứng kiểm chứng; các con số giữa bản cá nhân ban đầu và bản nhóm cũng khác nhau. | Sử dụng baseline 90 phút và mục tiêu 22 phút theo quy trình nhóm đã thống nhất; phân biệt rõ số liệu mục tiêu với kết quả đã đo. |
| CP6 Mức can thiệp / quyết định | Tham khảo AI để phân tích rủi ro, so sánh No AI/Rule/Workflow/Agent và rà soát các câu hỏi theo Google PAIR. | Hỗ trợ hệ thống hóa Value, Usability, Feasibility, Viability Risk; làm rõ nhu cầu Augment và vai trò Human-in-the-loop. | AI có thể đánh giá thấp rủi ro bảo mật hoặc khẳng định quá mức rằng timestamp giúp phát hiện mọi lỗi. | Giữ quyết định Go có điều kiện; yêu cầu Zero Data Retention, không tự gửi email, không suy diễn ngoài transcript và có phương án quay về template thủ công khi AI lỗi. |

### Nhận định của tôi về việc sử dụng AI

AI hữu ích nhất ở vai trò hỗ trợ cấu trúc hóa thông tin và phản biện các giả định, không thay thế việc kiểm chứng. Những số liệu như thời gian xử lý, tỷ lệ gửi biên bản trễ hoặc mức độ cho phép sử dụng dữ liệu cần dựa trên phỏng vấn, khảo sát và đo lường thực tế. Với bài toán này, AI chỉ nên tạo bản nháp; BA phải kiểm tra nội dung gốc và chịu trách nhiệm phê duyệt trước khi gửi khách hàng.

---

## 6. Reflection (CP7)

> Phần này yêu cầu phản ánh trải nghiệm cá nhân thật và template ghi rõ không dùng AI viết thay. Vì vậy, tôi để các câu hỏi dưới đây để tự hoàn thiện bằng trải nghiệm của mình, không tự tạo câu chuyện hoặc cảm xúc thay cho người viết.

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

*Điều học được từ bài toán luyện phỏng vấn theo JD của Quân là với lượng input đầu vào quá lớn, nhiều lĩnh vực thì việc vận dụng AI khá hữu ích và tiết kiệm thời gian, nhân lực. Qua bài toán theo dõi task nhóm và các bài toán kỹ thuật của Thành, mình nhận thấy khi có AI công việc của 1 lập trình viên sẽ bớt khó khăn và xử lý được nhiều task hơn.*

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

*Nhóm đã gặp vấn đề như vậy sau khi vừa làm việc nhóm, trong quá trình thực hiện sau đó phát hiện ra thì đã quay lại flow và điều chỉnh phù hợp, điểm tốt là tất cả thành viên đều đồng lòng.*

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

*Mình không đổi hoàn toàn ý khi phản biện, trao đổi và bổ sung hoàn thiện đề tài, ý kiến và đóng góp.*

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

*Kết quả kiểm chứng cũng có điểm làm mình bất ngờ. Đó là cách vận hành trước đây của mình còn hơi lăng kính chủ quan*

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

*Cách thống nhất baseline 90 phút, mục tiêu dưới 25 phút, bottleneck, boundary bảo mật và trách nhiệm duyệt của BA.*

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

*Mình muốn kiểm chứng sớm hơn, cách thu thập bằng chứng hoặc điểm muốn phản biện sâu hơn.*

**6.7. Hiểu bài**

*Qua quá trình nghiên cứu, mình nhận thấy vấn đề chính là BA mất nhiều thời gian sau mỗi buổi workshop để nghe lại bản ghi, tổng hợp yêu cầu, quyết định, câu hỏi còn mở và các việc cần thực hiện. Quy trình hiện tại mất khoảng 90 phút, trong đó 65 phút dành cho việc nghe lại và phân loại thông tin. Vì vậy, nhóm đề xuất ứng dụng AI để hỗ trợ trích xuất và phân loại nội dung từ transcript, giúp rút ngắn thời gian xử lý xuống dưới 25 phút, tiết kiệm khoảng 75% thời gian và đảm bảo 100% biên bản được gửi trong ngày. Tuy nhiên, AI chỉ được sử dụng thông tin có trong transcript, không tự suy diễn yêu cầu, thời hạn hay quyết định chưa được xác nhận; đồng thời cần bảo đảm quyền riêng tư dữ liệu. Nhóm lựa chọn mô hình Workflow kết hợp Human-in-the-loop, trong đó AI thực hiện trích xuất và phân loại, còn BA kiểm tra, chỉnh sửa và phê duyệt trước khi gửi khách hàng. Mình cho rằng mức can thiệp này phù hợp vì nội dung workshop có thể mơ hồ hoặc có nhiều cách hiểu, nên con người vẫn cần giữ quyền quyết định cuối cùng. Sau khi đánh giá lợi ích, tính khả thi và các rủi ro, nhóm thống nhất Go có điều kiện, triển khai thử nghiệm Workflow với sự kiểm soát của BA.*

---

## 7. Tài liệu tham khảo

- Rob Fitzpatrick, *The Mom Test — How to talk to customers and learn if your business is a good idea when everyone is lying to you*.
- Teresa Torres, *Continuous Discovery Habits — Discover Products that Create Customer Value and Business Value* (Opportunity Solution Tree methodology).
- Google People + AI Research (PAIR), *PAIR Guidebook — Designing human-centered AI products*: https://pair.withgoogle.com/
- David Bland & Alexander Osterwalder, *Testing Business Ideas* (Assumption Mapping).
- Atlassian Corporation, *Atlassian Intelligence & Teamwork Graph documentation*: https://www.atlassian.com/software/confluence/features/atlassian-intelligence
- Granola AI, *The AI notepad for meetings without bots*: https://www.granola.so
- International Institute of Business Analysis (IIBA), *A Guide to the Business Analysis Body of Knowledge (BABOK Guide v3)*.
