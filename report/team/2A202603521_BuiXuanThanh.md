# Báo cáo cá nhân — BuiXuanThanh-2A202603521

## 1. Thông tin thành viên

- Họ tên: Bùi Xuân Thành
- MSSV: 2A202603521
- Email: 26ai.thanhbx@vinuni.edu.vn
- Vai trong nhóm: Người gắn nhãn 2 (nhóm 3 người, nhánh `nv2-nhan`)

## 2. Phần việc phụ trách

Nhiệm vụ C (CP3) · Bảng lỗi và cách khắc phục:

- Gắn nhãn độc lập 20 ca lỗi theo năm loại của Google PAIR (bộ nhãn 2).
- Bảng khắc phục 5 ca, mỗi loại một ca, trong `report/team/bang_loi.md`.
- Bước cuối sau khi merge: so hai bộ nhãn, tính tỉ lệ đồng thuận, ghi quy tắc phân biệt cho các ca không trùng.

## 3. Đóng góp cụ thể

- Gắn nhãn 20 ca trong 8 phút, không trao đổi với người gắn nhãn 1 và không xem file hướng dẫn chi tiết trước khi gắn xong. Phân bố nhãn: Do người dùng 4 · Hệ thống 5 · Ngữ cảnh 4 · Giới hạn hệ thống 4 · Ngầm 3.
- Chọn 5 ca cho bảng khắc phục: ca 1 (Do người dùng), ca 20 (Hệ thống), ca 18 (Ngữ cảnh), ca 13 (Giới hạn hệ thống), ca 17 (Ngầm). Mỗi dòng có cách phát hiện đo được (event, ngưỡng, tần suất) và một vai trò phụ trách.
- Tỉ lệ đồng thuận hai bộ nhãn: 18 / 20 = 90% (lệch ca 8 và 13); bảng so nhãn và quy tắc do trưởng nhóm đối chiếu và ghi trong `bang_loi.md`.

## 4. Bằng chứng

- `report/team/nhan_nv2.md`: bộ nhãn độc lập, commit `NV2: gan nhan doc lap 20 ca loi` trên nhánh `nv2-nhan`.
- `report/team/bang_loi.md`: bảng khắc phục 5 ca, commit `NV2: bang khac phuc 5 ca`.
- Commit so nhãn và tỉ lệ đồng thuận (`bang_loi.md` hoàn chỉnh): `4519818`.

## 5. Công cụ AI đã dùng

- Dùng Claude để giải thích định nghĩa 5 loại PAIR và cách phân biệt; nhãn từng ca do tôi tự quyết, AI không xem hay sửa nhãn trước khi so
- Dùng Claude hỗ trợ làm bảng khắc phục 

## 6. Tự đánh giá

- Hoàn thành phần gắn nhãn độc lập đúng thời gian và đủ 20 ca, đủ năm loại.
- Điều học được: gắn nhãn theo nguyên nhân gốc chứ không theo chỗ cần sửa; lỗi Ngầm khác lỗi Hệ thống ở chỗ không ai nhận ra cho tới khi kiểm tra.
- Cần cải thiện việc xác định nhãn trong từng trường hợp
