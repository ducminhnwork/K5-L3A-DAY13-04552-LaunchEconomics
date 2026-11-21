# Báo cáo nhóm

## 1. Thông tin nhóm

- Tên nhóm: 04552
- Lớp: L3A
- Thành viên: xem `TEAM.md`

## 2. Mục tiêu và cách tiếp cận

Nhóm xây dựng hồ sơ launch v0 cho trợ lý hoàn phí LogiX-VN để đánh giá chi phí, mức sử dụng, cơ chế xử lý lỗi và khả năng ra quyết định của pilot. Nhóm phân tích 1.200 yêu cầu và 1.624 lần chạy bằng `src/lab13.py`; các số từ cột `_simulated` được ghi nhãn `simulated`. Hai thành viên gắn nhãn lỗi độc lập trước khi đối chiếu.

## 3. Giải pháp

**A - Mô hình chi phí.** Nhóm cộng token và tool của mọi lần chạy, chi phí xem lại và làm lại, rồi chia cho số việc thành công. Mô hình được kiểm tra bằng ba phép thử, phân tách theo loại yêu cầu và bổ sung chi phí cố định. Chi tiết: [`bang_chi_phi.md`](bang_chi_phi.md).

**B - Độ nhạy.** Nhóm thay đổi giá token, mức xem lại, mức làm lại, lương và giới hạn số lần chạy; đồng thời tính phần việc chuyển cho nhân viên. Kết quả B1-B4: [`bang_chi_phi.md`](bang_chi_phi.md).

**C - Phân loại lỗi.** Hai người gắn nhãn riêng 20 ca theo Google PAIR, sau đó xử lý bất đồng theo nguyên nhân gốc. Mỗi loại lỗi có cách phát hiện đo được, biện pháp và vai trò phụ trách trong [`bang_loi.md`](bang_loi.md).

**D - Thiết kế pilot.** Nhóm tính cỡ mẫu hiệu dụng trước khi chọn cách chia. Kế hoạch có đối chứng, ngẫu nhiên hóa, rollback và ít nhất ba luật dừng đủ NẾU - TRONG - THÌ - KHÔNG THÌ. Chi tiết: [`pilot_plan.yaml`](pilot_plan.yaml).

**E - Chỉ số và quyết định.** Nhóm đặc tả ba nhóm chỉ số, liên kết chúng với event có `trace_id`, rồi tổng hợp rủi ro và bằng chứng bất lợi trước khi đề xuất. Chi tiết: [`chi_so.md`](chi_so.md), [`ho_so_launch_v0.md`](ho_so_launch_v0.md).


## 4. Kết quả

- Chi phí: 4.472 đ/việc thành công; cả hệ thống 5.865 đ/yêu cầu, bằng 0,49 lần nhân viên tự làm [simulated]. Trong phạm vi nội địa và hàng nặng, cộng cố định tại 45.000 yêu cầu/tháng: 4.599 đ/việc thành công [simulated].
- Ba yếu tố nhạy nhất: làm lại gấp đôi tăng 51,8%; xem lại gấp đôi tăng 40,7%; lương tăng 25% làm chi phí tăng 23,1% [simulated]. Xem lại 100% tốn 11.743–12.415 đ/việc, bằng 0,98–1,03 lần nhân viên tự làm [simulated].
- Pilot chỉ gồm `noi_dia` và `hang_nang`, chia 20 nhân viên trợ lý và 20 đối chứng. Chọn mức chênh 6 điểm, cần 859 yêu cầu hiệu dụng/nhóm và ít nhất 299 yêu cầu/người (DE 6,96); nếu tác động thật chỉ 5 điểm thì power khoảng 0,64.
- Chỉ số trong đợt chạy thử: chính 82,83% (994/1.200); bỏ qua gợi ý 27,12% (48/177); mở lại 7 ngày 4,25% (51/1.200). Đây là số quan sát, chưa chứng minh mức cải thiện do trợ lý.
- Hai bộ nhãn đã commit trùng 18/20 ca = 90%, vượt ngưỡng 80%; khác ca 8 và 13. `bang_loi.md` đã có năm ca khắc phục (1, 20, 18, 13, 17), đủ năm loại, mỗi ca có cách phát hiện đo được và một vai trò phụ trách. Bảng đối chiếu và quy tắc đã hoàn tất tại `4519818`: ca 8 thống nhất Hệ thống, ca 13 thống nhất Giới hạn hệ thống.
- Hồ sơ launch đề xuất **Go có điều kiện** cho pilot: ký chấp nhận đánh đổi cỡ mẫu, bật event đo thời gian thật, giảm xem lại theo bậc, loại hai loại yêu cầu ngoài phạm vi và sửa lỗi hệ thống trước 2026-12-14; quyết định pilot vào 2027-01-15. Mục lỗi đã được cập nhật hoàn tất trong hồ sơ launch.
- Kết quả duyệt chéo nhận từ hội đồng: **[CHỜ PHIÊN GATE 2a]**.
- Chấm lại SaoCungDuoc tại commit `b7586bd`: đề xuất **25/30, Go có điều kiện** (lần trước: 10/30, No-go tại `1d25587`). Hồ sơ đã hoàn thiện và bước 0.50 kéo dài 14 ngày; còn cần thống nhất công thức/event cho luật chi phí và mẫu số chi phí cố định. Chi tiết: [`phieu_cham.md`](phieu_cham.md). Điểm chờ nhóm xác nhận, không phải điểm nhóm 04552 nhận được.


## 5. Khó khăn và cách xử lý

- Ba thành viên kiêm nhiệm nhiều vai trò. Nhóm tách file và nhánh để giảm xung đột, đồng thời giữ hai bộ nhãn độc lập.
- Thời gian xem lại và làm lại là giả lập; nhóm ghi nhãn `simulated` và yêu cầu pilot đo thời gian thực.
- Số cụm hạn chế độ nhạy; nhóm tính cỡ mẫu hiệu dụng và ghi rõ đánh đổi trước khi chọn phương án.
- Máy Người 3 chưa cài Python (`python` không nhận diện; `py -0p` báo không có runtime). Đã đối chiếu CSV bằng PowerShell: 978 việc thành công, tổng chi phí 4.373.585 đ [simulated] và ba phân số chỉ số khớp báo cáo; chưa xác nhận chạy code trên máy thứ hai.

## 6. Tổng hợp đóng góp

Nguyễn Đức Minh phụ trách A, B, D, E; Bùi Xuân Thành phụ trách bộ nhãn độc lập và bảng khắc phục C; Đàm Tuấn Linh phụ trách bộ nhãn còn lại, thông tin nhóm, báo cáo nhóm và phiếu hội đồng. Chi tiết file/commit: [`TEAM.md`](../../TEAM.md) và ba báo cáo cá nhân tương ứng.

## 7. Hạn chế và hướng cải thiện

- Dữ liệu giả lập và chưa có đối chứng nên chưa cho phép kết luận nhân quả.
- Pilot phải đo thời gian, khối lượng và chi phí thực tế; duy trì event có `trace_id`, đối soát và kiểm tra mẫu.
- Chỉ xem xét mở rộng sau khi đạt cỡ mẫu, luật dừng và tiêu chí quyết định đã viết trước.

## 8. Tài liệu tham khảo

- Đề bài và hướng dẫn Lab 13 trong thư mục `docs/`.
- Erol và cộng sự, *Cost-of-Pass: An Economic Framework for Evaluating Language Models*.
- Google PAIR, *People + AI Guidebook*, phần Errors and Graceful Failure.
- Tài liệu `statsmodels.stats.power.NormalIndPower`.
