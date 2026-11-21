# Phiếu chấm hội đồng Gate 2a

Nhóm số n chấm nhóm số n + 1; nhóm cuối chấm nhóm 1. Chấm theo bằng chứng trong hồ sơ, không theo cách trình bày: một đề xuất No-go có lý do bằng số được điểm cao hơn một đề xuất Go bỏ qua con số bất lợi.

- Nhóm chấm (hội đồng): **04552**
- Nhóm được chấm: **[ĐIỀN KHI NHẬN PHÂN CÔNG LÚC 17:00]**
- Hồ sơ/commit được chấm: **[ĐIỀN URL HOẶC MÃ COMMIT]**

| Tiêu chí | 0 điểm | 5 điểm | 10 điểm | Điểm | Lý do (có số) |
| --- | --- | --- | --- | ---: | --- |
| Đề xuất khớp bằng chứng | Mâu thuẫn với số của chính nhóm | Khớp nhưng bỏ qua một con số bất lợi | Khớp, nêu cả con số bất lợi và cách xử lý | ... | ... |
| Số giả lập và phạm vi | Không nhãn; phạm vi "mọi yêu cầu" | Có nhãn hoặc có thu hẹp phạm vi | Nhãn ở mọi số giả lập; phạm vi thu hẹp có lý do bằng số | ... | ... |
| Pilot ra được quyết định | Không đối chứng hoặc thiếu cỡ mẫu | Đủ cỡ mẫu, luật dừng chung chung | Tách được tác động, đủ mẫu, luật dừng có ngưỡng, thời hạn, người có quyền dừng | ... | ... |
| **Tổng** | | | | **... / 30** | |

**Quyết định của hội đồng:** Go · Go có điều kiện · No-go (giữ một)

**Lý do:** ...

**Một câu hỏi cho đội trình:** ...

**Câu trả lời của đội trình (ghi lại tại buổi):** ...

## Checklist bằng chứng trước khi chốt điểm

- [ ] Đã đối chiếu đề xuất cuối với chính các con số trong `bang_chi_phi.md` và `ho_so_launch_v0.md` của nhóm được chấm.
- [ ] Đã tìm ít nhất một con số bất lợi và kiểm tra nhóm có nêu cách xử lý hay không.
- [ ] Đã rà mọi số dựa trên dữ liệu giả lập xem có nhãn `simulated` hay không.
- [ ] Đã kiểm tra phạm vi pilot được thu hẹp bằng lý do định lượng.
- [ ] Đã kiểm tra nhóm đối chứng, cách ngẫu nhiên hóa, cỡ mẫu và số cụm mỗi nhóm.
- [ ] Đã kiểm tra luật dừng có đủ ngưỡng, thời hạn, hành động và người có quyền dừng.
- [ ] Mỗi lý do chấm điểm có ít nhất một con số hoặc dẫn chứng cụ thể từ hồ sơ.
- [ ] Quyết định hội đồng là đúng một trong ba lựa chọn: Go, Go có điều kiện hoặc No-go.

## Chuẩn bị cho phiên hỏi–đáp

Phần này là ghi chú chuẩn bị, chưa phải kết quả chấm. Khi nhận hồ sơ, chọn một câu hỏi phù hợp với bằng chứng của nhóm được chấm và ghi vào mục “Một câu hỏi cho đội trình” ở trên.

| Chủ đề | Câu hỏi dự kiến | Bằng chứng cần tìm trong hồ sơ nhóm được chấm |
| --- | --- | --- |
| Chi phí khi xem lại 100% | Nếu tuần đầu phải xem lại 100%, chi phí mỗi việc thành công là bao nhiêu và còn tiết kiệm so với 12.000 đ không? | B4, giả định phút xem lại/làm lại, nhãn simulated, kế hoạch giảm xem lại an toàn |
| Cỡ mẫu theo cụm | Nhóm có bao nhiêu cụm mỗi nhánh, cỡ mẫu hiệu dụng bao nhiêu và chấp nhận đánh đổi nào nếu chưa đủ cho mức chênh 5 điểm? | D1, đơn vị phân nhóm, ICC, DE, mức chênh và power |
| Luật dừng an toàn | So với tỷ lệ mở lại hiện tại, ngưỡng của nhóm có làm pilot dừng ngay tuần đầu không; ai có quyền dừng và trong bao lâu? | Tỷ lệ hiện tại, đối chứng, trần tuyệt đối, luật dừng và rollback |

### Các số nhóm 04552 cần chuẩn bị khi được hỏi

- Xem lại 100%: 11.743 đ/việc với làm lại 9 phút; 12.415 đ/việc với thời gian trung bình trong dữ liệu, bằng 0,98–1,03 lần nhân viên tự làm [simulated]. Pilot phải học cách giảm xem lại an toàn.
- Cách chia: 20 nhân viên trợ lý và 20 đối chứng; cần 859 yêu cầu hiệu dụng mỗi nhóm, ít nhất 299 yêu cầu mỗi nhân viên, DE 6,96; chấp nhận mức chênh 6 điểm. Nếu tác động thật chỉ 5 điểm thì power khoảng 0,64.
- An toàn: tỷ lệ mở lại hiện tại 4,25%; kế hoạch đặt ngưỡng cao hơn đối chứng từ 2 điểm phần trăm hoặc vượt 6% trong một tuần; Giám đốc vận hành tắt trợ lý trong 30 phút.
- Nhiệm vụ C: hai bộ nhãn trùng 18/20 ca = 90%; bảng khắc phục đủ năm loại. Bảng thống nhất ca 8 và 13 chưa hoàn tất, cần nêu đúng trạng thái khi trình.

Nguồn: `bang_chi_phi.md`, `pilot_plan.yaml`, `bang_loi.md`, hai bộ nhãn độc lập và phần “Duyệt chéo Gate 2a” trong `docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md`.
