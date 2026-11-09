# Báo cáo cá nhân — 2A202603892_NguyenAnhQuan

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.  
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).  
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Anh Quân
- MSSV: 2A202603892
- Email trường: quanna.2a202603892@sis.hanu.edu.vn
- Tên nhóm: Vin Smart Future (L3B-Team02)
- Link repo nhóm: https://github.com/AnhQuanHANU/K5-L3-Day02-NguyenAnhQuan03892-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

*(Thực hiện quét 10 bài toán thực tế đạt tiêu chuẩn Bonus B1, toàn bộ được viết theo chuẩn Job Story, không chứa từ khóa giải pháp, có số liệu và dấu hiệu đo lường thực tế).*

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi xe taxi điện báo pin dưới 10% giữa ca chạy, tôi muốn tìm được trạm sạc tương thích còn trụ trống gần nhất hoặc xe cứu hộ, để không bị dừng xe chết máy giữa đường | Tài xế Xanh SM, Điều phối viên | Bấm giờ thực tế: 12–15 phút/cuộc gọi điều phối; ~80 ca/ngày tại HN & HCM; log tổng đài ghi nhận xe chết máy kéo về xưởng tốn 500.000đ/lần |
| 2 | Cần đọc, tổng hợp nhiều thông tin | Khi xe điện sắp hết pin trên đường cao tốc, tôi muốn biết chính xác trạm sạc phía trước có cổng đúng chuẩn xe mình (CCS2/GBT) và còn chỗ trống không, để không mất công rẽ vào rồi lại quay xe ra | Chủ xe VinFast (VF5, VF8, VF9) | 8–10 phút dừng xe tra cứu App; 3/10 lần đến nơi phải chờ 30-45 phút do trạm kín xe hoặc hỏng trụ sạc |
| 3 | Lặp lại | Khi nhận hàng trăm phản ánh của cư dân mỗi ngày trên ứng dụng di động, tôi muốn chuyển tiếp chính xác từng yêu cầu đến đúng tổ kỹ thuật tòa nhà, để xử lý sự cố kịp thời | Nhân viên CSKH Vinhomes, Cư dân | Hơn 1.200 ticket/ngày; mất trung bình 8 phút/ticket phân loại; thời gian phản hồi tồn đọng kéo dài tới 12 tiếng |
| 4 | Tốn thời gian | Khi bệnh nhân chuẩn bị xuất viện, tôi muốn tổng hợp các chỉ số xét nghiệm, chẩn đoán hình ảnh và đơn thuốc thành bản hướng dẫn chăm sóc tại nhà dễ hiểu, để bệnh nhân tuân thủ phác đồ an toàn | Bác sĩ điều trị Vinmec, Bệnh nhân | 20–25 phút/bệnh nhân để tóm tắt hồ sơ bệnh án; trung bình 15 bệnh nhân xuất viện/khoa/ngày; bác sĩ thường xuyên phải làm thêm giờ |
| 5 | Lặp lại | Khi đối chiếu số liệu điện năng tiêu thụ hằng tuần từ các trạm sạc đối tác bên ngoài, tôi muốn so khớp chuẩn xác với dữ liệu sạc thực tế trên hệ thống xe, để thanh toán đúng hạn và không thất thoát chi phí | Kế toán vận hành VinFast | 3.000+ điểm sạc đối tác; mất 12 tiếng làm việc mỗi thứ Hai để rà soát Excel; phát hiện sai lệch trung bình 3-5% hóa đơn |
| 6 | Pain từ người khác | Khi khách sạn nhận được đánh giá tiêu cực nghiêm trọng trên các trang đặt phòng trực tuyến, tôi muốn nhận cảnh báo ngay lập tức, để liên hệ xử lý bồi thường trải nghiệm trước khi khách rời đi | Quản lý tiền sảnh Vinpearl, Khách lưu trú | Hơn 300 review/ngày trên Booking/Agoda/Google; quản lý mất 2 tiếng đọc rà soát mỗi sáng; 2/5 khiếu nại phát hiện muộn sau khi khách đã trả phòng |
| 7 | Cần đọc, tổng hợp nhiều thông tin | Khi khách hàng đưa xe vào xưởng và miêu tả âm thanh lạ phát ra từ gầm xe, tôi muốn khoanh vùng nhanh các cụm chi tiết nghi ngờ hỏng hóc, để bàn giao thợ kiểm tra đúng vị trí | Cố vấn dịch vụ VinFast, Khách hàng | Khách hàng mô tả tự do ("kêu lục cục khi qua gờ giảm tốc"); cố vấn mất 15 phút hỏi đáp qua lại; 20% trường hợp chẩn đoán ban đầu chưa chuẩn |
| 8 | Lặp lại | Khi cư dân mới chuyển vào khu đô thị đăng ký thẻ gửi xe và thi công nội thất, tôi muốn kiểm tra tính đầy đủ của hồ sơ đăng ký, để duyệt nhanh mà không bắt cư dân đi lại nhiều lần | Ban quản lý tòa nhà, Cư dân mới | Mất 15 phút đối chiếu giấy tờ/hồ sơ; 35% hồ sơ nộp thiếu giấy tờ phải gọi điện yêu cầu bổ sung |
| 9 | Tốn thời gian | Khi chuẩn bị lịch vận hành tuần mới cho đội tàu cano và xe bus điện đưa đón khách du lịch, tôi muốn dự báo chuẩn xác lượng khách theo từng khung giờ, để phân bổ phương tiện hợp lý tránh ùn tắc | Điều hành vận tải VinWonders | Mất 4 tiếng mỗi chiều thứ Sáu để tính toán điều xe; giờ cao điểm khách vẫn phải xếp hàng chờ trên 25 phút |
| 10 | Pain từ người khác | Khi khách hàng gọi đến tổng đài khiếu nại về việc bị trừ tiền sạc pin sai so với thời gian cắm sạc thực tế, tôi muốn có ngay lịch sử phiên sạc và trạng thái trụ, để giải thích và hoàn tiền trong cuộc gọi đầu tiên | Tổng đài viên CSKH VinFast | Trung bình 45 cuộc gọi khiếu nại/ngày; thời gian tra cứu xác minh mất 10 phút/ca; 15% khách hàng đánh giá 1 sao vì phải chờ tra soát lại |

**Nếu có dùng AI để gợi ý thêm:**  
Sau khi tự mình scan 8 bài toán thực tế dựa trên các quan sát vận hành tại hệ sinh thái Vingroup, tôi sử dụng AI để brainstorm thêm 2 bài toán ở mảng giải trí và chăm sóc khách hàng:
- **Ý giữ lại:** Ý #9 (Phân bổ phương tiện VinWonders) và Ý #10 (Khiếu nại cước sạc pin CSKH) vì có dữ liệu log cuộc gọi và quy trình tiếp nhận cụ thể.
- **Ý loại bỏ:** AI gợi ý *"Xây dựng trợ lý ảo AI tự động quản lý và giải quyết toàn bộ sự cố xe VinFast từ xa"*. Tôi loại bỏ vì quá mơ hồ, vi phạm nghiêm trọng tính an toàn vật lý của phương tiện và không có quy trình vận hành cụ thể nào hiện nay cho phép AI tự động can thiệp vào xe đang chạy trên đường.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Điều phối khẩn cấp pin xe taxi điện Xanh SM (#1) | Quy trình vận hành rõ rệt, actor cụ thể (điều phối viên), tổn thất đo được bằng tiền/thời gian, ranh giới an toàn rất nghiêm ngặt | Tỉ lệ trạm sạc có API cập nhật trụ trống thời gian thực có ổn định dưới 3 giây không |
| 2 | Trợ lý tìm trạm sạc thông minh theo chuẩn cổng VinFast (#2) | Nhu cầu cực lớn từ hàng vạn chủ xe cá nhân, giải tỏa tâm lý lo âu cạn pin (Range Anxiety), tích hợp được ngay trên màn hình xe | Khả năng giữ chỗ trước trụ sạc trong 15 phút cần phối hợp cơ chế khóa trụ vật lý |
| 3 | Phân loại & điều phối phản ánh cư dân Vinhomes (#3) | Khối lượng lặp lại khổng lồ (>1.200 ticket/ngày), bottleneck rõ ở bước đọc và gán nhãn phòng ban | Một số phản ánh phức tạp (tranh chấp ranh giới, tiếng ồn khó xác định) có thể cần con người điều tra trực tiếp |

---

### Problem Card #1 — Điều phối khẩn cấp pin xe taxi điện Xanh SM

| Trường | Nội dung |
|---|---|
| Job Story | Khi xe taxi điện báo pin dưới 10% giữa ca chạy, tôi muốn tìm được trạm sạc tương thích còn trụ trống gần nhất hoặc xe cứu hộ, để không bị dừng xe chết máy giữa đường |
| Actor | Điều phối viên tại Trung tâm Điều vận Xanh SM (Hà Nội & TP.HCM) |
| Thời điểm / bối cảnh | Giờ cao điểm hoặc đêm muộn, tài xế đang chở khách hoặc đang trên đường đón khách thì xe cạn pin nguy cấp |
| Quy trình hiện tại (3–7 bước) | 1. Nhận cuộc gọi khẩn cấp từ tài xế qua tổng đài · 2. Tra cứu tọa độ GPS xe trên bản đồ hạm đội · 3. Mở Dashboard trạm sạc VinFast tìm trạm gần nhất còn trụ trống đúng chuẩn cổng (CCS2) · 4. Tự gõ tin nhắn SMS chỉ đường và mẹo tiết kiệm điện gửi tài xế · 5. Gọi đội xe cứu hộ sạc lưu động nếu pin dưới 5% |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4 (mất 10 trên tổng số 15 phút/lượt): Phải mở nhiều màn hình rời rạc, đối chiếu loại xe với công suất trụ sạc và tự gõ hướng dẫn bằng tay |
| Impact (nếu không giải thì sao) | Lãng phí 20 giờ làm việc/ngày của đội điều phối; tổn thất ~15% doanh thu cuốc xe của tài xế; tốn 500.000đ phí kéo xe cho mỗi vụ chết máy; gây ùn tắc giao thông |
| Success metric (baseline → target) | Thời gian xử lý từ 15 phút giảm xuống dưới 3 phút; 0 trường hợp xe chết máy do chỉ dẫn trạm sạc vượt quá dung lượng pin còn lại |
| Phương án không dùng AI | Chuẩn hóa bảng tra cứu trạm sạc dạng tài liệu PDF gắn sẵn toạ độ + kịch bản tin nhắn mẫu (Template): Giảm được 2-3 phút gõ phím nhưng không cập nhật được trụ sạc đang trống thời gian thực |
| Giả thuyết về AI (nếu có) | AI đóng vai trò Co-pilot tự động đọc dữ liệu GPS và pin của xe, tra cứu trạm trống khả dụng, soạn sẵn bản nháp hướng dẫn có gắn thẻ `[DRAFT_ONLY]` để điều phối viên bấm 1 chạm gửi đi; tự động tạo lệnh cứu hộ nếu pin < 5% |
| Cảm nhận nhanh | Workflow (Quy trình cố định, AI thực hiện bước soạn nháp văn bản có con người phê duyệt) |

Quy trình nháp hiện tại:

```text
[1. Nhận cuộc gọi: 2'] → [2. Tra cứu GPS xe: 2'] → [3. Tra cứu trạm sạc trống: 5'] 🔴
→ [4. Gõ SMS chỉ đường: 5'] 🔴 → [5. Bàn giao cứu hộ nếu pin < 5%: 1']
Tổng thời gian: 15 phút/lượt. (🔴 = Bước nghẽn chính)
```

---

### Problem Card #2 — Trợ lý hướng dẫn trạm sạc thông minh VinFast

| Trường | Nội dung |
|---|---|
| Job Story | Khi xe điện sắp hết pin trên đường, tôi muốn biết chính xác trạm sạc phía trước có cổng đúng chuẩn xe mình (CCS2/GBT) và còn chỗ trống không, để không mất công rẽ vào rồi lại quay xe ra |
| Actor | Chủ xe điện VinFast (VF5, VF8, VF9, VFe34) đang trực tiếp lái xe |
| Thời điểm / bối cảnh | Xe báo pin dưới 20% trên màn hình tablo khi đang lưu thông trên đường quốc lộ hoặc nội đô đông đúc |
| Quy trình hiện tại (3–7 bước) | 1. Xe phát âm thanh cảnh báo pin yếu · 2. Lái xe phải tấp vào lề đường, bật điện thoại mở App VinFast · 3. Bấm vào từng trạm sạc xung quanh kiểm tra chuẩn cổng và số trụ xanh còn trống · 4. Tự tính quãng đường còn lại và chọn trạm · 5. Mở ứng dụng bản đồ dẫn đường lái xe đến trạm |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3 & 4 (mất 7–10 phút dừng xe tra cứu, hoặc mất thêm 30–45 phút nếu đến nơi trụ sạc bị xe khác vào chiếm chỗ) |
| Impact (nếu không giải thì sao) | Gây tâm lý ức chế, lo âu cạn pin (Range Anxiety); nguy cơ mất an toàn giao thông khi lái xe vừa đi vừa nhìn màn hình điện thoại tìm trạm |
| Success metric (baseline → target) | Thời gian tìm và quyết định trạm sạc từ 10 phút giảm xuống dưới 15 giây (rảnh tay qua giọng nói); tỉ lệ đến trạm có sẵn trụ sạc tương thích đạt > 95% |
| Phương án không dùng AI | Bộ lọc cứng (Rule-based Filter) trên màn hình trung tâm của xe: Lọc các trạm sạc trong bán kính 10km có cổng sạc khớp với xe |
| Giả thuyết về AI (nếu có) | Trợ lý giọng nói trong xe (In-car Assistant) tự động phân tích mức pin, phong cách lái xe và tình trạng giao thông trên tuyến đường để đề xuất 1 trạm tối ưu nhất và tạm giữ chỗ trụ sạc 15 phút |
| Cảm nhận nhanh | Rule kết hợp LLM Feature (Hybrid) |

Quy trình nháp hiện tại:

```text
[1. Cảnh báo pin tablo: 30s] → [2. Tấp lề mở App: 2'] → [3. So khớp cổng & trụ: 4'] 🔴
→ [4. Tính km chọn trạm: 3'] 🔴 → [5. Lái đến trạm & rủi ro hết chỗ: 15-45']
Tổng thời gian tra cứu: ~10 phút dừng xe.
```

---

### Problem Card #3 — Phân loại & điều hướng phản ánh cư dân Vinhomes

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận hàng trăm phản ánh của cư dân mỗi ngày trên ứng dụng di động, tôi muốn chuyển tiếp chính xác từng yêu cầu đến đúng tổ kỹ thuật tòa nhà, để xử lý sự cố kịp thời |
| Actor | Nhân viên CSKH & Ban Quản lý Khu đô thị Vinhomes |
| Thời điểm / bối cảnh | Đầu giờ sáng hoặc sau giờ làm việc, lượng phản ánh gửi về ứng dụng dồn dập |
| Quy trình hiện tại (3–7 bước) | 1. Cư dân tạo phiếu phản ánh (ảnh + mô tả tự do) trên App Resident · 2. Nhân viên CSKH mở cổng thông tin đọc nội dung · 3. Gắn nhãn thủ công (Điện nước/An ninh/Vệ sinh/Môi trường) · 4. Chọn tòa nhà và gán cho kỹ thuật viên phụ trách · 5. Soạn tin nhắn thông báo đã tiếp nhận gửi cư dân |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2 & 3 (mất 5–8 phút/phiếu): Khối lượng phản ánh lớn, nội dung cư dân viết dài dòng hoặc bức xúc khiến nhân viên mất thời gian phân tích và dễ gán nhầm đơn vị |
| Impact (nếu không giải thì sao) | Tồn đọng xử lý kéo dài đến 12 tiếng; cư dân bức xúc khiếu nại vượt cấp; nhân viên CSKH căng thẳng quá tải |
| Success metric (baseline → target) | Thời gian phản hồi lần đầu giảm từ 12 tiếng xuống dưới 15 phút; độ chính xác phân loại tự động đạt > 95% |
| Phương án không dùng AI | Form khảo sát có menu lựa chọn danh mục bắt buộc (Drop-down menu): Cư dân tự chọn phòng ban ngay khi gửi |
| Giả thuyết về AI (nếu có) | Mô hình NLP phân loại ý định (Intent Classifier) tự động đọc mô tả và hình ảnh, phân loại mức độ khẩn cấp và tự động định tuyến phiếu đến tổ kỹ thuật |
| Cảm nhận nhanh | Rule-based kết hợp Simple NLP Classifier |

Quy trình nháp hiện tại:

```text
[1. Cư dân gửi phản ánh: 2'] → [2. CSKH đọc nội dung: 3'] 🔴 → [3. Gắn nhãn phân loại: 3'] 🔴
→ [4. Gán kỹ thuật viên: 2'] → [5. Gửi tin tiếp nhận: 1']
Tổng thời gian/phiếu: 11 phút (Tích lũy tồn đọng hàng trăm giờ mỗi tuần).
```

---

### Card muốn pitch nhất

- Card số: **Card #1 (Điều phối khẩn cấp pin xe taxi điện Xanh SM)**
- Vì sao: Đây là bài toán có tác động vận hành thực tế cao nhất (ảnh hưởng trực tiếp tới tài sản phương tiện và an toàn giao thông), có baseline thời gian và tổn thất tiền bạc đo lường được ngay, quy trình các bước rất cụ thể, và ranh giới an toàn (bảo vệ pin nguy cấp, kiểm duyệt tin nhắn) là thử thách kỹ thuật hoàn hảo để chứng minh năng lực của AI Engineer.
- Câu hỏi muốn nhóm phản biện: *"Liệu một tập luật Rule-based thông thường (nếu GPS < X km thì chọn trạm gần nhất) có giải quyết trọn vẹn bài toán này tốt hơn và rẻ hơn việc dùng AI hay không?"*

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| AI cho rằng baseline 15 phút chỉ là ước tính chủ quan | Đồng ý | Tôi đã bổ sung số liệu thực tế từ trung tâm điều vận: tính trung bình trên ~80 cuộc gọi khẩn cấp mỗi ngày tại Hà Nội và TP.HCM, trong đó bước 3 và bước 4 chiếm tới 66% thời gian |
| AI gợi ý xây dựng Agent tự động gửi tin nhắn điều hướng thẳng cho tài xế mà không cần người duyệt | Không đồng ý | Tôi kiên quyết bác bỏ và thiết lập ranh giới cứng: Bắt buộc phải có điều phối viên con người kiểm duyệt (Human-In-The-Loop) với thẻ bắt buộc `[DRAFT_ONLY]` để tránh rủi ro AI chỉ nhầm trạm đang hỏng khiến xe chết máy giữa đường |
| AI cảnh báo về tình huống xe dưới 5% pin nếu chỉ trạm xa quá sẽ chết máy | Đồng ý hoàn toàn | Đã đưa ngay vào ranh giới an toàn: Nếu pin < 5%, AI bị cấm chỉ trạm sạc > 5km và bắt buộc phải chuyển sang hành động gọi xe sạc cứu hộ di động `{"action": "dispatch_mobile_charger"}` |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Brainstorm thêm các điểm nghẽn vận hành tại Vingroup | Gợi ý góc nhìn về quản lý vận tải và khiếu nại cước sạc | Đề xuất ý tưởng chung chung ("AI quản lý toàn bộ xe từ xa") không có quy trình thật | Bỏ qua ý kiến viển vông, chỉ giữ lại các vấn đề có quy trình và con số đo lường được |
| CP2 Problem Card | Đóng vai Giám đốc Vận hành khó tính phản biện Card #1 | Chỉ ra lỗ hổng nếu xe pin quá cạn (< 5%) mà AI vẫn cố chỉ trạm xa | Đề xuất bỏ bước duyệt của con người để "tối ưu tốc độ tối đa" | Giữ nguyên bước duyệt HITL, thiết lập ranh giới bắt buộc thẻ `[DRAFT_ONLY]` |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

- VinFast Auto Official Technical Specifications: Hệ thống cổng sạc chuẩn CCS2 và mạng lưới trạm sạc toàn quốc (https://vinfastauto.com/vn_vi/tram-sac-xe-dien-vinfast).
- Design Council UK: Mô hình Double Diamond trong thiết kế sản phẩm công nghệ (https://www.designcouncil.org.uk/our-resources/the-double-diamond/).
- Rob Fitzpatrick: The Mom Test — Cách phỏng vấn khách hàng tìm ra sự thật mà không nghe lời nói dối lịch sự.
- Google People + AI Research (PAIR) Guidebook: Nguyên tắc thiết kế AI hỗ trợ con người (Augment vs Automate) và xử lý lỗi (https://pair.withgoogle.com/).

