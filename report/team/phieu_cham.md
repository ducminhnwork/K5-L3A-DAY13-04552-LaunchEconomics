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

## Câu hỏi về cỡ mẫu cho đội trình

**Bước 0.50 kéo dài 1 tuần (khoảng 2026-12-28 đến 2027-01-03). Với khoảng 1.500 × 82% ÷ 40 ≈ 30,7 yêu cầu trong phạm vi mỗi nhân viên mỗi ngày, mỗi người chỉ có khoảng 215 yêu cầu, ít hơn 299 mà D1 câu e yêu cầu. Nhóm đo chỉ số chính trong bao nhiêu ngày để đủ 859 hiệu dụng mỗi nhóm, mà vẫn chừa đủ 7 ngày theo dõi mở lại trước ngày quyết định 2027-01-15?**

**Câu trả lời của đội trình về cỡ mẫu:** Chưa có. Tài liệu trả lời được cung cấp dưới đây nói về chi phí xem lại, không trả lời câu hỏi cỡ mẫu này.

## Hỏi–đáp bổ sung về chi phí xem lại 100%

**Nguồn ghi nhận:** Tài liệu `tra_loi_hoi_dong.md` do thành viên nhóm 04552 cung cấp, tiêu đề tài liệu ghi “Nhóm SaoCungDuoc (L3A)”. Đây là câu trả lời bằng văn bản được cung cấp, chưa xác nhận đã trao đổi trực tiếp. Nội dung này không trả lời câu hỏi cỡ mẫu ở trên.

**Câu hỏi:** Nếu tuần đầu phải xem lại 100%, chi phí mỗi việc thành công là bao nhiêu, và luật dừng chi phí 8.000 đ trong `pilot_plan.yaml` có tự kích hoạt ngay không?

**Câu trả lời theo tài liệu được cung cấp:**

### 1. Chi phí khi xem lại 100%

Phạm vi pilot noi_dia + hang_nang (982 yêu cầu, 900 việc thành công), theo B4 trong `bang_chi_phi.md` [simulated]:

- Xem lại: 948 yêu cầu × 5 phút × 2.000 đ = 9.480.000 đ
- Token + tool của mọi lần chạy: 224.513 đ
- Làm lại: 48 ca × phút làm lại × 2.000 đ

| Phút làm lại mỗi ca | Chi phí mỗi việc thành công | Chi phí cả hệ thống mỗi yêu cầu (cộng 82 ca không thành công × 12.000 đ) |
| --- | ---: | ---: |
| 9 phút (theo đề) | 10.568.513 ÷ 900 = **11.743 đ = 0,98×** | 11.764 đ = 0,98× |
| 15,3 phút (trung bình trong dữ liệu) | 11.173.313 ÷ 900 = **12.415 đ = 1,03×** | 12.380 đ = 1,03× |

Xem lại 100% thì trợ lý gần như không tiết kiệm được so với nhân viên tự làm (12.000 đ) [simulated].

### 2. Luật dừng chi phí có tự kích hoạt không

- **Mốc 8.000 đ/việc thành công** (hướng dẫn mẫu): có, sẽ kích ngay tuần đầu vì 11.743 đ > 8.000 đ. Vì vậy `pilot_plan.yaml` của nhóm **không dùng mốc này**.
- **Luật nhóm đang dùng:** NẾU chi phí biến đổi cả hệ thống mỗi yêu cầu > **9.600 đ** (= 0,8 × 12.000 đ, chừa 2.370 đ cố định mỗi việc khi khối lượng còn một nửa, A4) TRONG **2 tuần liên tiếp** THÌ PM trợ lý hoàn phí giảm xem lại theo bậc, thu hẹp về noi_dia và giới hạn 2 lần chạy.
  - Tuần đầu: **không kích**, vì luật cần 2 tuần liên tiếp.
  - Hết tuần 2 (20/12, bước 0.25): **có kích** nếu vẫn xem lại 100% (11.764 đ > 9.600 đ). Mốc kiểm tra "giảm xem lại theo bậc" trong hồ sơ là 21/12, muộn hơn một ngày. Luật có thể thu hẹp pilot về noi_dia trước khi kế hoạch giảm xem lại kịp áp dụng. Nhóm thừa nhận đây là điểm chưa khớp.

### 3. Cách xử lý

1. Bước 0.10 và 0.25 (07/12–20/12): chi phí khi xem lại 100% đã biết trước (0,98–1,03× [simulated]); chỉ theo dõi, không áp luật dừng chi phí.
2. Luật 9.600 đ tính **từ bước 0.50 (21/12)**. Trước mốc này, tỉ lệ xem lại phải đã giảm theo bậc khi tỉ lệ sửa + bỏ < 15% trong 1 tuần (đợt chạy thử: 21,1% trong phạm vi, 27/128).
3. Mục tiêu thời gian: mỗi lần xem lại ≤ 5,1 phút (làm lại 9 phút) hoặc ≤ 4,8 phút (làm lại 15,3 phút) để hoà vốn; đo phút thật bằng event `staff_review_decision` từ tuần 1, thay số simulated.
4. Luật an toàn (mở lại 7 ngày) vẫn áp dụng ngay từ tuần đầu, không thay đổi.

Nhóm sẽ cập nhật `pilot_plan.yaml` (luật chi phí "TRONG 2 tuần liên tiếp kể từ bước 0.50") và điều kiện tương ứng trong `ho_so_launch_v0.md`.

### Ghi chú đối chiếu của hội đồng

- Phần trả lời mô tả một kế hoạch mới dùng ngưỡng 9.600 đ và bắt đầu bước 0.50 ngày 21/12; chưa cung cấp commit chứa kế hoạch đó. Không dùng nội dung này để tự thay đổi kết quả chấm tại commit `1d2558706cab2beb77f0f2908d18251500a84f9b`.
- Nhận định “mốc 8.000 đ sẽ kích ngay tuần đầu” cần được làm rõ: nếu luật có điều kiện **hai tuần liên tiếp**, tuần đầu vượt ngưỡng chưa đủ để kích hoạt. Phải đọc đồng thời ngưỡng, thời gian và hành động; không chỉ so sánh 11.743 với 8.000 đ.
- Ngưỡng 9.600 đ được mô tả theo **mỗi yêu cầu**, còn chi phí cố định 2.370 đ theo **mỗi việc thành công**; không cộng hai đại lượng này trước khi quy đổi về cùng mẫu số.
- Việc miễn áp luật chi phí ở hai bước đầu và thay ngày bắt đầu là phương án nhóm nêu trong tài liệu, chưa phải điều kiện đã được hội đồng chấp thuận. Cần đối chiếu YAML, hồ sơ launch và commit cập nhật; xác định ngân sách giai đoạn học, người chịu trách nhiệm và tiêu chí chuyển bước.
- Câu hỏi cỡ mẫu vẫn chưa có câu trả lời trong tài liệu này. Điểm và quyết định chỉ được cập nhật sau khi hội đồng xác nhận bằng chứng mới.

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
