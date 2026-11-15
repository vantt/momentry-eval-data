---
id: 2026-10-14-tro-ly-bao-con-so-ma-8a83
code: M-MGR0
aliases: [M-MGR0]
date: 2026-10-14
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, khác]
source: "chat Claude, claude:5a1e7c02"
sessions: ["claude:5a1e7c02"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c02#L9", "claude:5a1e7c02#L10", "claude:5a1e7c02#L20", "claude:5a1e7c02#L23", "claude:5a1e7c02#L26", "claude:5a1e7c02#L28", "claude:5a1e7c02#L29", "claude:5a1e7c02#L32", "claude:5a1e7c02#L33", "claude:5a1e7c02#L48", "claude:5a1e7c02#L49"]
hook: "Output chỉ có 2 tên file, agent vẫn báo 'cả 14 đều giống nhau'"
tension: tuong_ma_hoa_ra
sides: ["Agent báo số liệu rõ ràng, người dùng đưa vào slide làm phát hiện số 1", "Output công cụ chỉ hiện 2 file và một dòng, chưa chắc số liệu có thật"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một chuỗi nha khoa đang mất bệnh nhân, và người làm đang tổng hợp phỏng vấn để trình bày cho lãnh đạo vào thứ Năm. Cả nhóm ban đầu tin nguyên nhân là giá và nhắc lịch, nhưng khi đọc lại, nhiều chỗ bị xếp vào giá có thể do người lễ tân cũ nghỉ, khiến bệnh nhân mất luôn việc nhắc lịch và giải thích phí. Dữ liệu cho thấy phòng khám có nhiều người nghỉ thì tỉ lệ rời bỏ cao gấp khoảng đôi, nhưng chỉ có 6 phòng khám nên chưa thể kết luận. Với ai dùng AI phân tích dữ liệu khách hàng, đây là lúc cần đối chiếu con số với output gốc trước khi đưa lên slide."
audience: người làm phân tích nghiên cứu khách hàng có dùng AI
spine_context: Một chuỗi nha khoa đang mất bệnh nhân; người làm đang khảo sát vì sao và tổng hợp 14 phỏng vấn cùng dữ liệu khảo sát.
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn có bản tổng hợp và dàn ý cho buổi trình bày lãnh đạo vào thứ Năm.
spine_want_lines: ["claude:5a1e7c02#L1"]
spine_obstacle: "Lúc khởi động không ai nhắc đến lễ tân, nên muốn kiểm tra liên hệ này phải nối thêm bảng nhân sự."
spine_obstacle_lines: ["claude:5a1e7c02#L30", "claude:5a1e7c02#L34"]
spine_turn: Tưởng nguyên nhân rời bỏ là giá và nhắc lịch; hoá ra nhiều chỗ bị xếp vào giá có thể liên quan đến việc người lễ tân cũ nghỉ.
spine_turn_lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L29", "claude:5a1e7c02#L34"]
spine_action: "Tìm mọi lần nhắc đến lễ tân, nối bảng nhân sự với tỉ lệ rời bỏ theo phòng khám, rồi đưa phát hiện vào bản nháp."
spine_action_lines: ["claude:5a1e7c02#L25", "claude:5a1e7c02#L27", "claude:5a1e7c02#L31", "claude:5a1e7c02#L35"]
spine_outcome: Một phòng khám có 4 người nghỉ trong 12 tháng có tỉ lệ rời bỏ 41%; nhóm ít người nghỉ là 19–24%. Chỉ có 6 phòng khám nên chưa chứng minh được.
spine_outcome_lines: ["claude:5a1e7c02#L32", "claude:5a1e7c02#L33"]
spine_takeaway: Một con số tương quan trên 6 đơn vị chỉ là gợi ý; ghi rõ cỡ mẫu và đối chiếu với output gốc trước khi đưa lên slide.
spine_takeaway_lines: ["claude:5a1e7c02#L32", "claude:5a1e7c02#L33"]
completeness: 7
---

# Trợ lý báo con số mà output công cụ không hiện: kiểm chứng trước khi đưa vào slide

**Góc kể:** Một chuỗi nha khoa đang mất bệnh nhân, và người làm đang tổng hợp phỏng vấn để trình bày cho lãnh đạo vào thứ Năm. Cả nhóm ban đầu tin nguyên nhân là giá và nhắc lịch, nhưng khi đọc lại, nhiều chỗ bị xếp vào giá có thể do người lễ tân cũ nghỉ, khiến bệnh nhân mất luôn việc nhắc lịch và giải thích phí. Dữ liệu cho thấy phòng khám có nhiều người nghỉ thì tỉ lệ rời bỏ cao gấp khoảng đôi, nhưng chỉ có 6 phòng khám nên chưa thể kết luận. Với ai dùng AI phân tích dữ liệu khách hàng, đây là lúc cần đối chiếu con số với output gốc trước khi đưa lên slide.
**Bối cảnh:** Claude Code phân tích dữ liệu phỏng vấn và khảo sát cho dự án churn, và các số liệu được đưa thẳng vào bản synthesis để làm slide.
**Chuyện gì xảy ra:** Agent viết 'All 14 follow the same pattern' khi output chỉ thấy 2 tên file, và báo 3 phòng khám có churn 38% cùng nhóm 19 đến 24% dù output chỉ có một dòng. Với khảo sát, agent liệt kê đủ 6 lý do trong khi output rút gọn chỉ có dòng đầu với 97 người. Người dùng vẫn đưa các con số này vào synthesis như phát hiện số 1. Trong bản transcript rút gọn không thể khẳng định output bị cắt hay agent tự suy ra, nên cần xem log gốc trước buổi trình bày.
**Bài học:** Mỗi con số trong báo cáo cần truy được tới dòng output cụ thể. Yêu cầu trợ lý ghi kèm lệnh và kết quả gốc, và đừng đưa số vào slide khi chưa thấy nó trong output.
**Artefact:** Bảng đối chiếu: con số, lệnh đã chạy, dòng output tương ứng. Chụp màn hình output gốc, che tên thư mục và tên khách hàng.
**Góc người ngoài:** cách làm phổ biến là Lấy số từ phần đầu kết quả công cụ rồi trình bày như đã kiểm tra đầy đủ; ở đây khác ở Kết quả công cụ bị cắt, nhưng agent vẫn nêu các con số cụ thể. Người đọc cần biết cách kiểm tra số trước khi dùng cho người ra quyết định.
