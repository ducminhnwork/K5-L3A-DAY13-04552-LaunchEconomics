# Phiếu chấm hội đồng Gate 2a

- Nhóm chấm: **04552**, lớp L3A.
- Nhóm được chấm: **SaoCungDuoc**, lớp L3A.
- Repo: https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics
- Commit chấm lại: `main`, `d8a77239e3f814aacb9147745be088b614c684d7`.
- Ngày chấm lại: **21/11/2026 (GMT+7)**.
- Trạng thái: **Điểm và quyết định đề xuất sau review hồ sơ mới, chờ thành viên hội đồng tự kiểm tra và xác nhận**. Có dùng Codex hỗ trợ đọc và soạn phiếu; không giả lập hỏi–đáp trực tiếp.
- Phạm vi: đã đọc hồ sơ launch, YAML, bảng chi phí, bảng lỗi, chỉ số và báo cáo nhóm tại commit trên; chưa thực thi code của nhóm được chấm.

## Điểm đề xuất sau chấm lại

| Tiêu chí | Điểm | Lý do và bằng chứng |
| --- | ---: | --- |
| Đề xuất khớp bằng chứng | **10/10** | [Hồ sơ launch](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/ho_so_launch_v0.md) đã đủ 7 mục, chọn Go có điều kiện và nêu các số bất lợi: xem lại 100% tốn 11.743–12.415 đ/việc [simulated], power chỉ 0,64 nếu tác động thật 5 điểm, hang_nang mở lại 8,23%. Có điều kiện xử lý, vai trò phụ trách và mốc kiểm tra. Khắc phục lý do 0 điểm ở lần trước. |
| Số giả lập và phạm vi | **10/10** | [Bảng chi phí](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/bang_chi_phi.md), [hồ sơ launch](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/ho_so_launch_v0.md) và [chỉ số](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/chi_so.md) ghi nhãn simulated cho chi phí tổng hợp. Phạm vi chỉ noi_dia + hang_nang; loại quoc_te vì 1,88× [simulated], thành công 27,3%; loại doi_tac vì thành công 54,4% và chi phí hệ thống 0,92× [simulated]. Phạm vi này đã được đưa vào YAML. |
| Pilot ra được quyết định | **10/10** | [YAML](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/pilot_plan.yaml) có đối chứng đồng thời, ngẫu nhiên phân tầng 20 + 20 nhân viên, m tối thiểu 299, n hiệu dụng tối thiểu 859 và lịch đo 14 ngày. Bốn luật dừng có ngưỡng, thời gian, hành động và vai trò. [chi_so.md](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/chi_so.md) đã thống nhất công thức C: ca lam_lai chỉ tính phút đo thật; 12.000 đ chỉ cho ca handoff, đếm một lần. Đã quy đổi cố định về 2.172 đ/yêu cầu, bổ sung operational_monitoring và data_lock; đủ căn cứ nâng từ 5 lên 10 điểm theo rubric. |
| **Tổng** | **30/30** | Tăng 5 điểm so với lần 2; các lý do trừ điểm pilot đã được khắc phục. Không thay phần 70 điểm đối chiếu của trợ giảng. |

## Quyết định đề xuất

**Go có điều kiện**, chỉ cho pilot noi_dia + hang_nang.

Bản mới đã xử lý bốn điểm còn vướng của lần chấm 25/30. **30/30 là điểm chất lượng hồ sơ theo rubric, không có nghĩa mọi điều kiện triển khai đã được thực hiện.** Vẫn giữ các điều kiện của nhóm trong [hồ sơ launch](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/ho_so_launch_v0.md): ký chấp nhận mức chênh 6 điểm, sửa chống hoàn trùng, bật event đo thời gian thật, giảm xem lại an toàn và theo dõi riêng hang_nang.

| Điểm phản biện lần trước | Bằng chứng khắc phục ở commit mới |
| --- | --- |
| Công thức YAML khác event | Hai file cùng định nghĩa C; ca lam_lai chỉ tính phút làm lại; 12.000 đ chỉ cho ca chuyển nhân viên, mỗi request_id một lần; không cộng thêm phút cho ca handoff. |
| Cố định và biến đổi khác mẫu số | Cùng mẫu số mỗi yêu cầu trong phạm vi: khối lượng một nửa 18.412,5 yêu cầu/tháng; cố định ≈ 2.172 đ/yêu cầu; 9.600 + 2.172 ≈ 11.772 đ, dưới 12.000 đ [simulated]. |
| Lịch theo dõi chưa rõ | data_lock ghi nhận tới hết 03/01, chờ 24 giờ đóng tới hết 04/01, theo dõi 7 ngày tới hết 11/01, quyết định 12/01; thiếu mẫu thì kéo dài thu nhận và lùi quyết định. |
| interim_looks dễ gây hiểu nhầm | Có operational_monitoring hằng tuần cho chi phí, mức sử dụng, hoàn trùng; tách khỏi việc kiểm định hiệu quả chỉ số chính. |

Điều kiện thực hiện trước 07/12/2026 và các mốc sau đó vẫn cần được người có vai trò trong hồ sơ xác nhận; chưa có dữ liệu pilot thực tế để kết luận hiệu quả.

## Đối chiếu câu hỏi cỡ mẫu với kế hoạch mới

Câu hỏi đã chuẩn bị trước đây giả định bước 0.50 chỉ một tuần và ngày quyết định 15/01. Hai mốc này không còn khớp bản hiện tại: [YAML](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/pilot_plan.yaml) đã ghi bước 0.50 từ **21/12/2026 đến 03/01/2027 (14 ngày)**, quyết định **12/01/2027**.

Tính tay theo các giả định của lab, phân bổ đều giữa nhân viên và hai nhánh:

```text
Yêu cầu/người/ngày = 1.500 × (982/1.200) ÷ 40 = 30,6875
m sau 14 ngày = 429,625
DE tại m này = 1 + (429,625 − 1) × 0,02 = 9,5725
n_hiệu_dụng mỗi nhánh = 20 × 429,625 ÷ 9,5725 ≈ 897,6 > 859
```

DE 6,96 trong YAML tương ứng thiết kế tối thiểu m = 299; không dùng DE đó cho m ≈ 430. Lượng yêu cầu trên là dự báo, không phải mẫu đã thu được.

Nếu yêu cầu cuối nhận hết ngày 03/01, đóng đúng hạn hết ngày 04/01 rồi theo dõi 7 ngày sau đóng, dữ liệu hoàn chỉnh hết ngày 11/01; quyết định 12/01 khả thi về lịch nhưng ít dư địa. Phải kiểm tra dấu thời gian, dữ liệu thiếu và số lượng thực tế của cả hai nhánh.

Đây là đối chiếu từ kế hoạch mới, **không phải lời trả lời trực tiếp đã ghi nhận của đội trình**.

## Câu hỏi sau lần chấm 25/30 và phản hồi bằng hồ sơ

**Câu hỏi:** Trong YAML, chi phí hệ thống cộng 12.000 đ cho mọi ca không thành công, nhưng chi_so.md chỉ cộng theo event handoff_to_staff. Các ca lam_lai được ghi nhận và cộng chi phí thế nào để luật 9.600 đ/yêu cầu không bỏ sót hoặc cộng trùng, và ngưỡng này đã quy đổi chi phí cố định về cùng mẫu số chưa?

**Phản hồi bằng văn bản trong repo:** [Báo cáo nhóm, mục 7](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/group_report.md), [chú thích YAML](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/pilot_plan.yaml) và [bảng event](https://github.com/VictorUIT/K5-L3A-DAY13-SaoCungDuoc-LaunchEconomics/blob/d8a77239e3f814aacb9147745be088b614c684d7/report/team/chi_so.md) cùng xác định:

- Token/tool tính mọi lần chạy; xem lại và làm lại tính theo phút đo thật; ca lam_lai không cộng thêm 12.000 đ.
- Chỉ ca chuyển nhân viên cộng 12.000 đ/request_id một lần, không cộng thêm phút xem lại/làm lại cho cùng ca.
- Mẫu số là số yêu cầu trong phạm vi của nhánh trợ lý theo tuần, mỗi request_id một lần.
- Trong mẫu có 34 ca chuyển nhân viên và 48 ca lam_lai; C = (3.072.513 + 34 × 12.000) ÷ 982 ≈ 3.544 đ/yêu cầu [simulated]. Khi xem lại 100%, C khoảng 11.178 đ/yêu cầu với 9 phút làm lại/ca [simulated].
- Cố định quy về 2.172 đ/yêu cầu ở khối lượng một nửa; giải thích cũ 2.370 đ/việc thành công đã được thay.
- Bảng A/B giữ cách tính theo đề lab; C là định nghĩa vận hành riêng cho luật dừng, đã được nêu tách biệt.

Đây là phản hồi kiểm chứng được từ hồ sơ, không phải bản ghi nguyên văn lời nói tại buổi. Các đánh dấu xác nhận/trao đổi trực tiếp do thành viên chỉnh trong phiếu trước lượt chấm này được giữ nguyên; điểm 30/30 là đề xuất mới cần thành viên xác nhận riêng.

## Các điểm đã cải thiện và điểm còn chờ

- A–B: đầy đủ bảng chi phí và độ nhạy; B4 thừa nhận xem lại 100% gần như không tiết kiệm.
- C: có hai bộ nhãn, đồng thuận 18/20 = 90%, quy tắc cho ca 13/17 và đủ 5 loại khắc phục.
- D: có D1/D2, số cụm và cỡ mẫu; 4 luật dừng; đã kéo dài bước 0.50, chỉ áp luật chi phí từ bước này.
- E: có 3 chỉ số tính thử, thêm chỉ số dùng/an toàn, bảng event gồm 11 dòng (một dòng gộp đóng/mở lại), 5 rủi ro và hồ sơ 7 mục.
- Đã đối chiếu số chính bằng phép tính từ CSV trong workspace: 982 yêu cầu trong phạm vi, 34 ca handoff, 48 ca làm lại; cố định 2.172,44 đ/yêu cầu và C khoảng 3.544,31 đ/yêu cầu [simulated]. Chưa chạy code repo SaoCungDuoc.
- Không giữ điểm trừ cũ sau khi đã có bằng chứng khắc phục. Cần tiếp tục đo thời gian thật và kiểm tra phân bổ mẫu khi pilot bắt đầu.

## Lịch sử chấm

| Lần | Commit | Điểm từng tiêu chí | Tổng | Quyết định đề xuất | Lý do thay đổi |
| --- | --- | --- | ---: | --- | --- |
| 1 | `1d2558706cab2beb77f0f2908d18251500a84f9b` | 0 + 10 + 0 | 10/30 | No-go | Hồ sơ launch và kế hoạch pilot còn mẫu. |
| 2 | `b7586bd5efa8bfd449cedf1d32c0b303ca251938` | 10 + 10 + 5 | 25/30 | Go có điều kiện | Đã có hồ sơ, thiết kế, lịch và luật dừng; cần thống nhất cách đo chi phí. |
| 3 | `d8a77239e3f814aacb9147745be088b614c684d7` | 10 + 10 + 10 | 30/30 | Go có điều kiện | Đã thống nhất công thức/event, cùng mẫu số chi phí, lịch khóa dữ liệu và theo dõi vận hành. |

Bảng ghi kết quả đề xuất review theo từng commit. Các đánh dấu xác nhận của thành viên từ trước được bảo toàn; điểm 30/30 ở lần 3 chưa được xem là đã được thành viên xác nhận.

## Phụ lục giữ nguyên trao đổi đã ghi nhận ở lần trước

Các câu hỏi, câu trả lời và ghi chú bên dưới được lưu để bảo toàn nguồn. Mốc lịch và nhận định “chưa có commit chứa kế hoạch” là trạng thái ở lần chấm trước, đã được cập nhật bằng kết quả chấm lại phía trên; không dùng các ghi chú cũ như kết luận hiện tại.

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


## Checklist chấm lại

- [x] Đã đọc lại hồ sơ tại commit mới và đối chiếu rubric 0/5/10.
- [x] Đã cập nhật lý do tăng điểm, quyết định và điều kiện.
- [x] Đã tính lại cỡ mẫu theo lịch 14 ngày và cửa sổ theo dõi.
- [x] Đã giữ riêng lịch sử chấm và lời trả lời bằng văn bản.
- [x] Thành viên hội đồng tự kiểm tra và xác nhận điểm/quyết định.
- [x] Đã hỏi trực tiếp và ghi câu trả lời cho các điểm còn vướng.
- [x] Thành viên xác nhận riêng điểm đề xuất 30/30 của lần chấm tại `d8a7723`.
