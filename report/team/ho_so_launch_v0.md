# Hồ sơ launch v0 · Trợ lý hoàn phí LogiX-VN (Gate 2a)

Số liệu tính bằng `src/lab13.py` trên mẫu 1.200 yêu cầu (dữ liệu giả lập). Cột trạng thái chỉ nhận: **Xong, có bằng chứng · Chưa · Giả lập**. Mục dựa trên cột `_simulated` ghi Giả lập.

| # | Mục | Con số chính | Trạng thái | Người phụ trách |
| --: | --- | --- | --- | --- |
| 1 | Chi phí mỗi việc thành công | 4.472 đ [simulated], gấp 16,3 lần hoá đơn token và tool chia số yêu cầu (274,7 đ); giờ nhân viên chiếm 92,5% tổng chi phí. Chi tiết: `bang_chi_phi.md` A2 | Giả lập | PM trợ lý hoàn phí |
| 2 | Ba yếu tố nhạy nhất | 1. số ca làm lại gấp đôi: +51,8% · 2. tỉ lệ xem lại gấp đôi: +40,7% · 3. lương nhân viên tăng 25%: +23,1%. Giá token yếu nhất (+5,6%). `bang_chi_phi.md` B1, B2 | Giả lập | PM trợ lý hoàn phí |
| 3 | So với nhân viên tự làm (12.000 đ) | Cả hệ thống 5.865 đ mỗi yêu cầu = 0,49x [simulated]. Phạm vi noi_dia + hang_nang cộng cố định: 4.599 đ = 0,38x (một nửa khối lượng: 5.784 đ = 0,48x). Xem lại 100%: 11.743 đ = 0,98x, hoặc 12.415 đ = 1,03x nếu làm lại 15,3 phút | Giả lập | Giám đốc tài chính |
| 4 | Chỉ số chính, dùng, an toàn | Trong đợt chạy thử (không có đối chứng): chính 82,83% · bỏ qua gợi ý 27,12% · mở lại 7 ngày 4,25%. `chi_so.md` E1 | Xong, có bằng chứng | Trưởng nhóm CSKH |
| 5 | Bảng lỗi và cách khắc phục | 20 ca lỗi, năm loại theo Google PAIR; hai bộ nhãn độc lập trùng 18/20 = 90% (lệch ca 8 và 13, đã có quy tắc); bảng khắc phục 5 ca, mỗi loại một ca, có cách phát hiện đo được. `bang_loi.md` | Xong, có bằng chứng | Kỹ sư trưởng agent |
| 6 | Pilot plan | Chia theo nhân viên, 20 dùng trợ lý và 20 đối chứng, ngẫu nhiên; mức chênh phát hiện được 6 điểm, 859 yêu cầu mỗi nhóm, DE 6,96, m ≥ 299; phạm vi noi_dia + hang_nang; ba luật dừng đủ bốn vế; quyết định 2027-01-15. `pilot_plan.yaml` | Xong, có bằng chứng | Giám đốc vận hành |
| 7 | Rủi ro kinh tế | Làm lại gấp đôi: 6.787 đ (+51,8%) · xem lại 100% kéo dài: 0,98x đến 1,03x · khối lượng một nửa: +2.370 đ mỗi việc cố định · giới hạn 1 lần: thêm 85 yêu cầu sang nhân viên. `chi_so.md` E2 | Giả lập | PM trợ lý hoàn phí |

## Con số bất lợi và cách xử lý

- **Phát hiện được tối thiểu 6 điểm, không phải 5.** Với 40 nhân viên, chia theo cụm tối đa 1.000 yêu cầu hiệu dụng mỗi nhóm, thấp hơn 1.251 cần cho 5 điểm. Nếu tác động thật chỉ là 5 điểm thì power còn khoảng 0,64. Xử lý: Giám đốc vận hành ký chấp nhận mức chênh 6 điểm trước ngày bắt đầu.
- **Xem lại 100% không tiết kiệm.** 0,98x đến 1,03x của chi phí nhân viên tự làm [simulated], vì tiền xem lại chiếm khoảng 90% chi phí. Xử lý: pilot học tỉ lệ xem lại có thể giảm an toàn; giảm theo bậc khi tỉ lệ sửa cộng bỏ dưới 15%.
- **Tỉ lệ mở lại hiện tại 4,25%.** Ngưỡng tuyệt đối 3% sẽ dừng pilot ngay tuần đầu. Xử lý: so với nhóm đối chứng (chênh 2 điểm) kèm trần tuyệt đối 6%.
- **Hai loại không đáng xử lý.** quoc_te: 1,88x, thành công 27,3%; doi_tac: 0,85x và có điều khoản riêng. Xử lý: loại khỏi phạm vi pilot.
- **Phút xem lại và làm lại là số giả lập.** Xử lý: bật event có `trace_id` và thay bằng phút đo thật sau tuần 1.

## Đề xuất

**Go có điều kiện** cho pilot noi_dia + hang_nang, bắt đầu 2026-12-14, với các điều kiện:

1. Giám đốc vận hành ký chấp nhận mức chênh 6 điểm (power khoảng 0,64 nếu tác động thật là 5 điểm), kiểm tra trước 2026-12-14.
2. Bật đủ event có `trace_id` và thay phút simulated bằng phút đo thật sau tuần 1, người phụ trách Kỹ sư trưởng agent, kiểm tra 2026-12-21.
3. Có kế hoạch giảm xem lại theo bậc, người phụ trách Trưởng nhóm CSKH, kiểm tra cuối bước 0.25 (2026-12-28).
4. Đưa quoc_te và doi_tac ra khỏi phạm vi và sửa các lỗi hệ thống đã ghi trong bảng lỗi trước ngày bắt đầu, người phụ trách PM trợ lý hoàn phí, kiểm tra 2026-12-14.
