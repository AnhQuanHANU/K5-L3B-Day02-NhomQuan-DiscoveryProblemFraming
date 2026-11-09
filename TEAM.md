# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: Vin Smart Future (L3B-Team02)
- Candidate problem nhóm chọn (1 câu): Điều phối và xử lý khẩn cấp sự cố pin thực địa cho tài xế taxi điện Xanh SM (GSM) nhằm giảm thời gian điều hướng từ 15 phút xuống dưới 3 phút và triệt tiêu nguy cơ xe chết máy trên đường.
- Quyết định cuối (Go / Not Yet / No-Go): Go, phạm vi nhỏ (Triển khai Workflow có AI hỗ trợ soạn nháp chỉ dẫn + Rule kiểm soát ngưỡng pin < 5% điều xe cứu hộ, bắt buộc điều phối viên duyệt trước khi gửi).

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Anh Quân | 2A202603892 | Nhóm trưởng, phụ trách Problem Statement, vẽ quy trình & ranh giới an toàn AI | AnhQuanHANU |
| 2 | Trần Minh Đức | 2A202603112 | Phụ trách kiểm chứng giả định (phỏng vấn, survey) | DucTM-L3B |
| 3 | Lê Hoàng Nam | 2A202603541 | Phụ trách research giải pháp thị trường & thiết kế bộ eval | NamLH-VinUni |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Nguyễn Anh Quân | Trần Minh Đức | Cluster, cây OST, bảng chấm điểm shortlist |
| CP4 — Kiểm chứng | Trần Minh Đức | Lê Hoàng Nam | Assumption map, 3 interview snapshots, khảo sát nhanh |
| CP4 — Research | Lê Hoàng Nam | Nguyễn Anh Quân | Bảng research giải pháp có link kiểm chứng thực tế |
| CP5 — Quy trình trước/sau | Nguyễn Anh Quân | Trần Minh Đức | Quy trình hiện tại & tương lai + bảng before/after |
| CP5 — Problem Statement v0 | Nguyễn Anh Quân | Lê Hoàng Nam | Problem Statement v0 (6 trường chuẩn) |
| CP6 — Mức can thiệp + Problem Statement v1 | Nguyễn Anh Quân | Trần Minh Đức | Ma trận phân loại, AI Canvas, câu hỏi PAIR, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Anh Quân | Lê Hoàng Nam | Đánh giá 4 rủi ro + Quyết định Go (pilot 2 tuần) & ngưỡng dừng |

## Cá nhân

### NguyenAnhQuan-2A202603892

**Phần việc phụ trách:**
- Trưởng nhóm điều phối toàn bộ tiến độ các checkpoint CP1 đến CP7.
- Xây dựng bản scan 10 bài toán cá nhân (CP1) và hoàn thiện 3 Problem Cards (CP2).
- Trực tiếp pitch và bảo vệ bài toán "Điều phối khẩn cấp pin xe điện Xanh SM" trong buổi hội tụ nhóm (CP3).
- Thiết kế sơ đồ quy trình chi tiết Before/After và bảng so sánh (CP5).
- Soạn thảo bản Problem Statement v0 và nâng cấp lên v1 kèm 4 tiêu chí đánh giá nghiêm ngặt và ranh giới an toàn (CP5, CP6).
- Tổng hợp đánh giá 4 rủi ro, kế hoạch pilot 2 tuần và điều kiện ngưỡng dừng (CP6).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):
- Hoàn thiện 100% nội dung báo cáo cá nhân `report/individual/2A202603892_NguyenAnhQuan.md` đạt tiêu chuẩn Bonus B1 (10 problem scan).
- Đóng góp cây Opportunity Solution Tree (OST), bảng chấm điểm đa tiêu chí và tổng hợp báo cáo nhóm `report/team/group_report.md`.
- Tạo sơ đồ quy trình trực quan `report/assets/04-workflow-diagram.png` và thẻ bài toán `report/assets/vinfast-problem-card.png`.
- Xây dựng bộ Eval mẫu 10 cặp test case trong báo cáo nhóm (đạt tiêu chuẩn Bonus B3).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):
- Mục 2.3 (Cây OST), Mục 4 (Quy trình trước/sau), Mục 5 (Problem Statement v0), Mục 6 & 7 (AI Canvas & Problem Statement v1), Mục 8 (Quyết định) trong `report/team/group_report.md`.
- Hai file sơ đồ hình ảnh tại `report/assets/04-workflow-diagram.png` và `report/assets/vinfast-problem-card.png`.
- File cá nhân đầy đủ tại `report/individual/2A202603892_NguyenAnhQuan.md`.

**Điều mình học được từ phần nhóm:**
- Hiểu sâu sắc sự khác biệt giữa *Opportunity* (nỗi đau có thật của người dùng) và *Solution* (giải pháp kỹ thuật trá hình) thông qua cây OST.
- Nhận thức rõ ràng rằng trong các bài toán điều phối vận hành thực tế, AI phải là trợ lý đồng hành (**Co-pilot**) có con người kiểm duyệt (**Human-in-the-loop**), chứ không được phép chạy tự trị hoàn toàn (**Agent**) vì rủi ro an toàn và trách nhiệm pháp lý.
