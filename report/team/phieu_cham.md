# Phiếu chấm hội đồng Gate 2a

- Nhóm chấm (hội đồng): **04552**, lớp L3A.
- Nhóm được chấm: **SaoCungDuoc**, lớp L3A.
- Repo: https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics
- Nhánh và commit được chấm: `main`, `1d2558706cab2beb77f0f2908d18251500a84f9b`.
- Ngày review: **21/11/2026 (GMT+7)**.
- Trạng thái: **Bản đề xuất chấm sau review hồ sơ, chờ thành viên hội đồng xác nhận và hỏi–đáp trực tiếp**. Có sử dụng Codex hỗ trợ đọc, đối chiếu và soạn phiếu; điểm và quyết định cần được nhóm 04552 tự kiểm tra trước khi công bố.
- Phạm vi: đọc hồ sơ và code nguồn; chưa thực thi code repo được chấm. Không suy ra kết quả ở nhánh hoặc commit khác.

## Điểm đề xuất theo thang hội đồng

| Tiêu chí | Điểm | Lý do và bằng chứng |
| --- | ---: | --- |
| Đề xuất khớp bằng chứng | **0/10** | [Hồ sơ launch](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/ho_so_launch_v0.md) còn trống cả 7 mục và chưa chọn một trong ba đề xuất. Chưa đủ bằng chứng cho mức 5 hoặc 10; đây là thiếu đề xuất để đối chiếu, không phải kết luận nhóm đã đưa đề xuất mâu thuẫn. [Bảng chi phí B4](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/bang_chi_phi.md) đã nêu số bất lợi 11.743–12.415 đ/việc [simulated], nhưng chưa đưa cách xử lý vào hồ sơ quyết định. |
| Số giả lập và phạm vi | **10/10** | [Bảng chi phí A2–A4, B1–B4](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/bang_chi_phi.md) có nhãn `simulated` ở các chi phí tổng hợp hoặc tiêu đề cột. A3 đề xuất chỉ `noi_dia + hang_nang` (0,22× và 0,69× [simulated]); loại `quoc_te` (1,88× [simulated], thành công 27,3%) và `doi_tac` (0,85× [simulated], thành công 54,4%). Đủ bằng chứng định lượng cho phạm vi; kế hoạch YAML chưa cập nhật phạm vi này, được đánh giá riêng ở tiêu chí pilot. |
| Pilot ra được quyết định | **0/10** | [Kế hoạch pilot](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/pilot_plan.yaml) chưa điền đơn vị phân nhóm, cỡ mẫu, DE, số cụm, đối chứng cùng thời gian, rollback và ngày quyết định. Cả 3 luật dừng vẫn là khung chứa dấu hỏi; tỷ lệ đối chứng 0,5 và `randomized: true` sẵn có chưa đủ chứng minh thiết kế phù hợp. Không đủ căn cứ cho mức 5 hoặc 10. |
| **Tổng** | **10/30** | Chỉ chấm 30 điểm hội đồng; không thay phần 70 điểm đối chiếu của trợ giảng. |

## Quyết định đề xuất của hội đồng

**No-go** tại commit được chấm: chưa duyệt kế hoạch pilot.

Bảng A–B và bảng lỗi đã có nội dung đáng ghi nhận, nhưng chưa có đề xuất launch hoàn chỉnh và thiết kế pilot để kiểm soát an toàn hoặc xác định tác động. Không dùng riêng mức chi phí 4.472 đ/việc [simulated] làm căn cứ cho chạy pilot.

### Việc cần làm để quay lại cổng

1. Điền đủ 7 mục hồ sơ launch: con số, trạng thái, vai trò phụ trách; chọn một đề xuất và giải thích số bất lợi B4 (0,98–1,03× nhân viên tự làm [simulated]).
2. Hoàn thiện D1, D2 và YAML: phạm vi, cách chia, cỡ mẫu hiệu dụng, số cụm, đánh đổi về mức chênh/power, đối chứng và rủi ro lan truyền tác động.
3. Viết ít nhất 3 luật dừng có chỉ số, ngưỡng, thời gian, hành động, người có quyền dừng và vế KHÔNG THÌ; bổ sung rollback và ngày quyết định.
4. Điền 3 chỉ số tính thử, thêm chỉ số dùng và an toàn, ít nhất 6 event có `trace_id`, ít nhất 2 rủi ro kinh tế trong [chi_so.md](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/chi_so.md).
5. Nhóm được chấm tự chỉ định người phụ trách và hạn xử lý các việc trên; gửi commit mới để hội đồng đánh giá lại.

## Một câu hỏi cho đội trình

**B4 cho thấy xem lại 100% tốn 11.743–12.415 đ/việc [simulated], trong khi pilot còn trống cỡ mẫu và luật dừng. Nhóm sẽ chọn No-go hay Go có điều kiện, và cần hoàn tất những bằng chứng, ngưỡng dừng nào trước khi bắt đầu pilot?**

**Câu trả lời của đội trình:** Chưa có; ghi lại sau phiên hỏi–đáp thực tế. Nội dung trong repo không được xem là câu trả lời trực tiếp.

**Điểm/quyết định sau khi hội đồng xác nhận:** Chưa xác nhận. Nếu đánh giá lại commit mới, ghi commit, thay đổi điểm và lý do riêng; giữ rõ bản đã được review.

## Đối chiếu các yêu cầu liên quan

| Phần | Quan sát tại commit được chấm |
| --- | --- |
| A và B | Bảng chi phí có A1–A4, B1 đủ 9 kịch bản, B2–B4; ghi nhận mô hình tính cả lần chạy lỗi và 222 yêu cầu không thành công khi so chi phí hệ thống. Chưa xác nhận thực thi code. |
| C | [Bảng lỗi](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/bang_loi.md) có 20 cặp nhãn, đồng thuận 18/20 = 90%, quy tắc cho ca 13 và 17; đủ 5 dòng khắc phục có cách phát hiện, ngưỡng/tần suất và vai trò phụ trách. Việc cho phép dùng AI gắn nhãn là tuyên bố của nhóm trong file, chưa được hội đồng xác minh với giảng viên. |
| D | D1, D2 và các trường thiết yếu của YAML còn trống; chưa đủ để quyết định pilot. |
| E | 7 mục launch còn trống; 3 kết quả chỉ số, 6 dòng event và 2 dòng rủi ro mới là mẫu. |
| Báo cáo nhóm | [group_report.md](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/1d2558706cab2beb77f0f2908d18251500a84f9b/report/team/group_report.md) còn mẫu, chưa tổng hợp kết quả và phản hồi duyệt chéo. |

## Checklist review hồ sơ

- [x] Đã cố định commit và đọc các file bằng chứng.
- [x] Đã kiểm tra đề xuất: chưa được chọn trong hồ sơ launch.
- [x] Đã xem số bất lợi B4 và cách gắn nhãn simulated.
- [x] Đã kiểm tra lý do thu hẹp phạm vi trong A3.
- [x] Đã kiểm tra thiết kế đối chứng, cỡ mẫu, luật dừng và rollback: còn thiếu.
- [x] Đã ghi một câu hỏi và các việc cần hoàn thiện.
- [ ] Thành viên hội đồng đã tự đối chiếu, xác nhận điểm và quyết định.
- [ ] Đã hỏi trực tiếp và ghi câu trả lời của đội trình.
