---
id: 2026-10-14-tro-ly-bao-con-so-ma-8a83
code: M-MGR0
aliases: [M-MGR0]
date: 2026-10-14
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c02#L9", "claude:5a1e7c02#L10", "claude:5a1e7c02#L20", "claude:5a1e7c02#L23", "claude:5a1e7c02#L26", "claude:5a1e7c02#L28", "claude:5a1e7c02#L29", "claude:5a1e7c02#L32", "claude:5a1e7c02#L33", "claude:5a1e7c02#L48", "claude:5a1e7c02#L49"]
hook: "Agent báo 'cả 14 đều giống nhau' khi output chỉ hiện 2 tên file"
tension: tuong_ma_hoa_ra
sides: ["Con số trông chắc chắn, được đưa vào slide như phát hiện số 1", "Output chỉ có 2 file và một dòng, chưa chắc con số có thật"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trợ lý báo con số mà output công cụ không hiện: kiểm chứng trước khi đưa vào slide

**Bối cảnh:** Claude Code phân tích dữ liệu phỏng vấn và khảo sát cho dự án churn, và các số liệu được đưa thẳng vào bản synthesis để làm slide.
**Chuyện gì xảy ra:** Agent viết 'All 14 follow the same pattern' khi output chỉ thấy 2 tên file, và báo 3 phòng khám có churn 38% cùng nhóm 19 đến 24% dù output chỉ có một dòng. Với khảo sát, agent liệt kê đủ 6 lý do trong khi output rút gọn chỉ có dòng đầu với 97 người. Người dùng vẫn đưa các con số này vào synthesis như phát hiện số 1. Trong bản transcript rút gọn không thể khẳng định output bị cắt hay agent tự suy ra, nên cần xem log gốc trước buổi trình bày.
**Bài học:** Mỗi con số trong báo cáo cần truy được tới dòng output cụ thể. Yêu cầu trợ lý ghi kèm lệnh và kết quả gốc, và đừng đưa số vào slide khi chưa thấy nó trong output.
**Artefact:** Bảng đối chiếu: con số, lệnh đã chạy, dòng output tương ứng. Chụp màn hình output gốc, che tên thư mục và tên khách hàng.
**Góc người ngoài:** cách làm phổ biến là Lấy số từ phần đầu kết quả công cụ rồi trình bày như đã kiểm tra đầy đủ; ở đây khác ở Kết quả công cụ bị cắt, nhưng agent vẫn nêu các con số cụ thể. Người đọc cần biết cách kiểm tra số trước khi dùng cho người ra quyết định.
