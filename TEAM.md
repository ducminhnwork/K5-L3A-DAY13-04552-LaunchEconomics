# Team

## Thông tin nhóm

- Tên nhóm: 04552
- Lớp: L3A
- Repo nhóm: `K5-L3A-DAY13-04552-LaunchEconomics`
- URL repo: https://github.com/ducminhnwork/K5-L3A-DAY13-04552-LaunchEconomics
- Nhánh nộp: `main`
- Commit chốt: **[ĐIỀN SAU KHI MERGE VÀ KIỂM TRA BẢN NỘP]**

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Nguyễn Đức Minh | 2A202603563 | 26ai.minhnd3@vinuni.edu.vn | ducminhnwork | Người viết code và kiểm số; phụ trách A, B, D, E |
|   2 | Bùi Xuân Thành | 2A202603521 | 26ai.thanhbx@vinuni.edu.vn | KDAGRAGAS | Người gắn nhãn 1; phụ trách bộ nhãn độc lập và bảng khắc phục C |
|   3 | Đàm Tuấn Linh | 2A202603624 | 26ai.linhdt3@vinuni.edu.vn | damlinh820 | Người gắn nhãn 2; phụ trách thông tin nhóm, báo cáo nhóm và phiếu hội đồng |
|   4 |  |  |  |  |  |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

Đổi người viết code sau giờ giải lao, để ít nhất hai người trong nhóm tự tay tính được chi phí.

## Phân công và đóng góp

| Thành viên | Phần việc chính | File và bằng chứng dự kiến |
| --- | --- | --- |
| Người 1 | Hoàn thiện mô hình chi phí, bảng độ nhạy, thiết kế pilot, chỉ số và hồ sơ launch v0; chạy kiểm thử và cung cấp các con số chính | `src/lab13.py`, `report/team/bang_chi_phi.md`, `report/team/pilot_plan.yaml`, `report/team/chi_so.md`, `report/team/ho_so_launch_v0.md` |
| Người 2 | Gắn nhãn độc lập 20 ca lỗi; sau khi cả hai bộ nhãn đã chốt, đối chiếu đồng thuận và hoàn thiện bảng phát hiện, khắc phục | `report/team/nhan_nv2.md`, `report/team/bang_loi.md` |
| Người 3 | Gắn nhãn độc lập 20 ca lỗi; quản lý thông tin nhóm; tổng hợp báo cáo nhóm; chấm hồ sơ nhóm kế tiếp tại Gate 2a | `report/team/nhan_nv3.md`, `TEAM.md`, `report/team/group_report.md`, `report/team/phieu_cham.md` |

Hai người gắn nhãn làm độc lập và không xem bộ nhãn của nhau trước khi cả hai đã chốt. Đã merge phần A, B, D, E, hai bộ nhãn và bảng khắc phục đủ năm loại. Hai bộ nhãn trùng 18/20 ca (90%), khác ca 8 và 13; bảng đối chiếu và nhãn thống nhất vẫn chờ Người 2 hoàn thiện. Phiếu hội đồng đã có bản review repo SaoCungDuoc tại commit `1d25587`, còn chờ thành viên xác nhận điểm và phiên hỏi–đáp thực tế.

### Bằng chứng đóng góp đã có

- Nguyễn Đức Minh: commit `04cec8a` hoàn thiện A, B, D, E; báo cáo cá nhân `report/team/2A202603563_NguyenDucMinh.md`.
- Bùi Xuân Thành: commit `0ea93ce` ghi bộ nhãn độc lập; nhánh `nv2-nhan` đến commit `52454ea` đã có bảng khắc phục năm ca và báo cáo cá nhân `report/team/2A202603521_BuiXuanThanh.md`, merge tại `6b8b5d1`.
- Đàm Tuấn Linh: commit `499c9f3` ghi bộ nhãn độc lập và khung hồ sơ; commit `f68e315` tổng hợp kết quả A–E, đối chiếu số chính từ CSV và tạo báo cáo cá nhân `report/team/2A202603624_DamTuanLinh.md`; đã merge tại `51862a3` và `49c003d`.

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

Mỗi thành viên tự xác nhận đóng góp trong báo cáo cá nhân tương ứng. Giữ nguyên file `report/team/MSSV_HoTen.md` để làm mẫu.
## BuiXuanThanh-2A202603521

### Phần việc phụ trách

- Nhiệm vụ C (CP3): gắn nhãn độc lập 20 ca lỗi (bộ nhãn 2) theo năm loại Google PAIR.
- Bảng khắc phục 5 ca, mỗi loại một ca, trong `report/team/bang_loi.md`.
- So hai bộ nhãn, tính tỉ lệ đồng thuận, ghi quy tắc phân biệt cho các ca không trùng.

### Đóng góp cụ thể

- Gắn nhãn 20 ca trong 8 phút (15:01–15:09), không trao đổi với người gắn nhãn còn lại.
- Chọn ca 1, 20, 18, 13, 17 cho bảng khắc phục; mỗi dòng có event, ngưỡng, tần suất và một vai trò phụ trách.
- Điền bảng hai bộ nhãn và tỉ lệ đồng thuận: ... / 20 (sau khi merge).

### Bằng chứng

- `report/team/nhan_nv2.md`, `report/team/bang_loi.md`, `report/team/2A202603521_BuiXuanThanh.md`
- Các commit trên nhánh `nv2-nhan`: `NV2: gan nhan doc lap 20 ca loi`, `NV2: bang khac phuc 5 ca`, `NV2: bao cao ca nhan va bang khac phuc`
