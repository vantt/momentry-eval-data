---
id: 2026-10-25-chuyen-diem-sang-file-nhap-truong-63a6
code: M-SA4Q
aliases: [M-SA4Q]
date: 2026-10-25
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c03#L52", "claude:5a1e7c03#L53", "claude:5a1e7c03#L54", "claude:5a1e7c03#L55"]
hook: "Làm tròn 6,25 thành 6,2: file điểm đủ 42 dòng nhưng có thể lệch"
tension: nho_ma_to
sides: ["File xuất đúng ba cột, đủ 42 dòng, trông hoàn chỉnh", "Python làm tròn về số chẵn, điểm giữa như 6,25 có thể lệch quy ước"]
strength: 2
stakes: 2
hits: 1
runs: 1
unverified: [facts]
unverified_facts: ["6,25", "6,2", "6,35", "6,4"]
privacy: unchecked
links: []
threads: []
---

# Chuyển điểm sang file nhập trường: làm tròn kiểu Python có thể lệch với quy ước

**Bối cảnh:** Trường yêu cầu file nhập điểm theo mẫu có ba cột, trong đó cột điểm giữa kỳ làm tròn một chữ số. Điểm gốc nằm trong file CSV của lớp.
**Chuyện gì xảy ra:** Agent dùng pandas round(1) để làm tròn 42 điểm và xuất ra file xlsx với đúng ba cột và 42 dòng. Hàm round của Python và numpy làm tròn về số chẵn khi đúng giữa, nên 6,25 thành 6,2 và 6,35 thành 6,4, khác với quy ước làm tròn nửa lên thường dùng trong chấm điểm. Trong phiên không thấy bước nào đối chiếu số làm tròn với điểm gốc có số đúng giữa hay không.
**Bài học:** Khi làm tròn điểm cho nhà trường, dùng quy ước của trường (thường là nửa lên) và kiểm tra vài điểm có số 5 ở chữ số thứ hai, đừng tin hàm mặc định.
**Artefact:** Bảng ba điểm mẫu trước và sau làm tròn, đặt cạnh quy ước của trường (che mã và tên học sinh).
**Góc người ngoài:** cách làm phổ biến là Mở mẫu của trường, so sánh tên cột và kiểu dữ liệu, rồi mới xuất file; ở đây khác ở Agent kiểm tra số lượng nhưng chưa kiểm tra đúng định dạng mẫu, nên có rủi ro file không được trường chấp nhận. Người đọc có thể học từ đây cách xác định điều gì nên kiểm tra và điều gì có thể bỏ qua khi xuất dữ liệu cho hệ thống bên ngoài.
