# Báo cáo cá nhân — Đàm Tuấn Linh (2A202603624)

## 1. Thông tin thành viên

- Họ tên: Đàm Tuấn Linh
- MSSV: 2A202603624
- Email: 26ai.linhdt3@vinuni.edu.vn
- GitHub: damlinh820
- Vai trong nhóm: Người gắn nhãn 2, kiêm giữ hồ sơ; phụ trách thông tin nhóm, báo cáo nhóm và phiếu hội đồng Gate 2a.

## 2. Phần việc phụ trách

Tôi phụ trách bộ nhãn độc lập của Người 3 cho 20 ca lỗi trong nhiệm vụ C. Tôi đọc đề bài, phân loại từng ca theo nguyên nhân gốc vào một trong năm nhóm: Do người dùng, Hệ thống, Ngữ cảnh, Giới hạn hệ thống và Ngầm.

Ngoài phần gắn nhãn, tôi quản lý các thông tin chung của nhóm, tổng hợp báo cáo nhóm, chuẩn bị phiếu chấm hội đồng Gate 2a và phối hợp hoàn thiện hồ sơ launch v0. Tôi giữ nguyên tính độc lập của bộ nhãn trước khi đối chiếu với bộ nhãn còn lại.

## 3. Đóng góp cụ thể

- Hoàn thành bộ nhãn độc lập cho đủ 20 ca lỗi, kèm lý do theo nguyên nhân gốc trong [`nhan_nv3.md`](nhan_nv3.md).
- Ghi lại cam kết gắn nhãn độc lập: chỉ đọc 20 ca trong đề bài, không xem bộ nhãn của Người 2 và không trao đổi trước khi chốt nhãn.
- Gắn nhãn các ca theo quy tắc nhất quán; ví dụ phân biệt lỗi nhập thiếu thông tin là Do người dùng, lỗi gọi tool sai tham số là Hệ thống, và lỗi đúng thiết kế nhưng gây hiểu nhầm là Ngữ cảnh.
- Cập nhật thông tin nhóm, vai trò và phân công trong [`TEAM.md`](../../TEAM.md).
- Tổng hợp mục tiêu, cách tiếp cận, giải pháp, hạn chế và đóng góp thành viên trong [`group_report.md`](group_report.md).
- Chuẩn bị khung phiếu chấm chéo Gate 2a trong [`phieu_cham.md`](phieu_cham.md), gồm tiêu chí bằng chứng, phạm vi pilot, luật dừng và phần quyết định của hội đồng.
- Đối chiếu hai bộ nhãn đã commit: trùng 18/20 ca = 90%, khác ca 8 và 13; giữ nguyên bộ nhãn độc lập và chuyển phần thống nhất cho Người 2.
- Cập nhật báo cáo khi Người 2 bổ sung bảng khắc phục đủ năm loại; phân biệt rõ phần đã có bằng chứng và phần còn chờ đối chiếu hoặc hỏi–đáp.
- Phối hợp kiểm tra tính nhất quán giữa báo cáo nhóm, các bảng nhiệm vụ và hồ sơ launch; các số liệu lấy từ dữ liệu mô phỏng được giữ nguyên nhãn `simulated` theo quy định.

## 4. Bằng chứng

- Bộ nhãn độc lập và thời gian thực hiện: [`report/team/nhan_nv3.md`](nhan_nv3.md).
- Phân công vai trò và đóng góp của thành viên: [`TEAM.md`](../../TEAM.md).
- Báo cáo nhóm do tôi tổng hợp: [`report/team/group_report.md`](group_report.md).
- Phiếu chấm hội đồng Gate 2a: [`report/team/phieu_cham.md`](phieu_cham.md).
- Các tài liệu nhóm được tham chiếu khi tổng hợp: [`bang_loi.md`](bang_loi.md), [`chi_so.md`](chi_so.md), [`ho_so_launch_v0.md`](ho_so_launch_v0.md) và [`pilot_plan.yaml`](pilot_plan.yaml).
- Commit bộ nhãn và khung hồ sơ: `499c9f3` trên nhánh `nv3-nhan`, đã được merge vào `main` qua commit `51862a3`.
- Commit `f68e315` tổng hợp kết quả A–E và tạo báo cáo cá nhân, đã được merge vào `main` qua commit `49c003d`.
- Kiểm tra chéo CSV bằng PowerShell: 978 việc thành công; chi phí 4.472 đ/việc và 5.865 đ/yêu cầu cả hệ thống [simulated]; ba chỉ số 994/1.200, 48/177 và 51/1.200.
- Chưa chạy được `src/lab13.py` trên máy cá nhân do chưa cài Python; chưa hoàn tất phiếu chấm vì chưa nhận hồ sơ nhóm được chấm.

## 5. Công cụ AI đã dùng

Tôi dùng ChatGPT/Codex để hỗ trợ rà soát cấu trúc báo cáo, đối chiếu các file bằng chứng trong thư mục `report/team` và diễn đạt báo cáo cá nhân theo đúng mẫu. Nội dung đóng góp được kiểm tra lại với [`TEAM.md`](../../TEAM.md), [`nhan_nv3.md`](nhan_nv3.md), [`group_report.md`](group_report.md) và [`phieu_cham.md`](phieu_cham.md). Việc gắn nhãn 20 ca được thực hiện độc lập theo cam kết trong `nhan_nv3.md`; AI không thay thế quyết định nhãn của tôi.

## 6. Tự đánh giá

Tôi đã hoàn thành bộ nhãn độc lập, thông tin thành viên và phần tổng hợp kết quả có đủ bằng chứng; phiếu hội đồng mới ở bước chuẩn bị. Điểm mạnh là giữ nguyên bộ nhãn trước đối chiếu, ghi rõ lý do theo nguyên nhân gốc và tổng hợp được các yêu cầu chính của hồ sơ launch. Bảng khắc phục của Người 2 đã có đủ năm loại. Phần còn chờ là bảng đối chiếu và kết quả thống nhất ca 8/13 do Người 2 phụ trách, hồ sơ nhóm được chấm và phản hồi hội đồng. Tôi sẽ cập nhật khi có bằng chứng thực tế.
