# Bảng lỗi và cách khắc phục · Nhiệm vụ C

20 ca lỗi nằm trong `docs/Ngay13_Lab13_De_bai_hoc_vien.docx`. Năm loại theo Google PAIR: **Do người dùng · Hệ thống · Ngữ cảnh · Giới hạn hệ thống · Ngầm**. Gắn nhãn theo nguyên nhân gốc, không theo chỗ cần sửa.

## Hai bộ nhãn độc lập

Bộ nhãn A: Bùi Xuân Thành (2A202603521), file `nhan_nv2.md`, gắn 15:01–15:09. Bộ nhãn B: Đàm Tuấn Linh (2A202603624), file `nhan_nv3.md`, chốt 15:00. Hai người gắn riêng, không trao đổi, commit trước khi so.

| Ca | Nhãn A (Thành) | Nhãn B (Linh) | Trùng? | Nhãn thống nhất |
| --: | --- | --- | :-: | --- |
| 1 | Do người dùng | Do người dùng | Có | Do người dùng |
| 2 | Hệ thống | Hệ thống | Có | Hệ thống |
| 3 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 4 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 5 | Ngầm | Ngầm | Có | Ngầm |
| 6 | Do người dùng | Do người dùng | Có | Do người dùng |
| 7 | Hệ thống | Hệ thống | Có | Hệ thống |
| 8 | Hệ thống | Ngầm | **Không** | Hệ thống |
| 9 | Do người dùng | Do người dùng | Có | Do người dùng |
| 10 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 11 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 12 | Ngầm | Ngầm | Có | Ngầm |
| 13 | Giới hạn hệ thống | Hệ thống | **Không** | Giới hạn hệ thống |
| 14 | Do người dùng | Do người dùng | Có | Do người dùng |
| 15 | Hệ thống | Hệ thống | Có | Hệ thống |
| 16 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 17 | Ngầm | Ngầm | Có | Ngầm |
| 18 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 19 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 20 | Hệ thống | Hệ thống | Có | Hệ thống |

**Tỉ lệ đồng thuận:** 18 / 20 = 90% (đạt mức tối thiểu 80%, tức 16/20). Hai ca lệch: 8 và 13. Không cần viết lại định nghĩa.

## Quy tắc phân biệt cho các ca không trùng

- **Ca 8 là Hệ thống, không phải Ngầm:** trợ lý dẫn điều khoản không tồn tại là sai so với thiết kế, và sai đó hiện ra trong tin nhắn nên nhân viên hoặc khách đọc là thấy; Ngầm chỉ dùng khi không ai nhận ra cho tới khi kiểm tra mẫu. Số tiền đúng chỉ làm lỗi nhẹ đi, không làm nó thành lỗi ngầm.
- **Ca 13 là Giới hạn hệ thống, không phải Hệ thống:** câu hỏi hoàn phí bảo hiểm nằm ngoài phạm vi của trợ lý, nên gốc lỗi là giới hạn phạm vi, kể cả khi trợ lý xử lý giới hạn đó kém (trả lời chung chung); cách xử lý kém nằm ở cột khắc phục.

## Bảng khắc phục cho 5 ca, mỗi loại một ca

Cách phát hiện dùng các event trong `chi_so.md` (có `trace_id`). Người phụ trách là một vai trò.

| Ca | Loại lỗi | Phát hiện bằng gì | Khắc phục thế nào | Ai phụ trách |
| --: | --- | --- | --- | --- |
| 1 | Do người dùng | Event `refund_ledger_write` có `ket_qua` = loi_so_tai_khoan; cảnh báo khi vượt 2% số yêu cầu trong một ngày | Kiểm tra độ dài số tài khoản ngay lúc nhập và hiện cảnh báo trước khi gửi; số sai thì yêu cầu khách nhập lại | PM trợ lý hoàn phí |
| 20 | Hệ thống | Đối soát mỗi giờ: một `request_id` có hơn một bản ghi `refund_ledger_write` với `ket_qua` = ok; ngưỡng 0 ca | Tạo `idempotency_key` từ `request_id` và số tiền; sổ cái từ chối khoá đã dùng, trả lại kết quả cũ | Kỹ sư trưởng agent |
| 18 | Ngữ cảnh | Tuần nào cũng đếm `ticket_reopened` có lý do về số tiền mà `audit_sample_checked` cho thấy `so_tien_da_hoan` = `so_tien_dung`; cảnh báo khi vượt 1% số yêu cầu mỗi tuần | Mẫu tin nhắn luôn ghi cách tính, ví dụ 30.000 đ × 50% = 15.000 đ | Trưởng nhóm CSKH |
| 13 | Giới hạn hệ thống | Event `handoff_to_staff` có `reason` = ngoai_pham_vi, theo tuần; mỗi tuần rà 20 trace ngoài phạm vi, ngưỡng 0 trace trả lời chung chung mà không nói rõ không xử lý | Nhận diện yêu cầu ngoài phạm vi (bảo hiểm), nói rõ trợ lý không xử lý và chuyển nhân viên kèm tóm tắt | PM trợ lý hoàn phí |
| 17 | Ngầm | Event `audit_sample_checked`: kiểm tra mẫu 100 đơn mỗi tuần so với bảng giá hiện hành; ngưỡng 1% đơn lệch | Xoá bộ nhớ đệm khi có bảng giá mới và ghi phiên bản bảng giá vào trace | Kế toán trưởng |
