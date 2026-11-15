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
hook: "Agent viết 'cả 14 đều giống nhau' khi output chỉ hiện 2 tên file"
tension: tuong_ma_hoa_ra
sides: ["Con số tưởng đã có bằng chứng, được đưa vào slide làm phát hiện số 1", "Output chỉ có 2 tên file và một dòng, phần còn lại có thể do agent tự suy ra"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một chuỗi nha khoa đang nhờ nhóm nghiên cứu tìm vì sao bệnh nhân bỏ đi, dựa trên 14 buổi phỏng vấn và khảo sát. Nhóm ban đầu gom các lý do vào 'giá' và 'nhắc lịch', tưởng đó là nguyên nhân chính, và phía khách hàng cũng không nhắc đến lễ tân khi bắt đầu dự án. Một câu lỡ lời về cô lễ tân trong một buổi phỏng vấn, khi được tra lại cả bộ dữ liệu, lại cho thấy có bệnh nhân ở lại chỉ vì người đó. Phòng khám nào mất nhiều lễ tân hơn thì tỷ lệ bỏ đi cao hơn gần gấp đôi, dù mới chỉ 6 phòng khám nên đây là tương quan chứ chưa chắc là nhân quả."
audience: người làm nghiên cứu khách hàng hoặc dịch vụ có khách quay lại
spine_context: "Một chuỗi nha khoa đang nhờ nhóm tìm vì sao bệnh nhân bỏ đi, qua 14 phỏng vấn và khảo sát."
spine_context_lines: ["claude:5a1e7c02#L1"]
spine_want: Muốn có bản tổng hợp và outline cho buổi trình bày điều hành thứ Năm.
spine_want_lines: ["claude:5a1e7c02#L1"]
spine_obstacle: "Phần lớn lý do bị gom vào nhóm 'giá' (7 người), nên tín hiệu về lễ tân bị che."
spine_obstacle_lines: ["claude:5a1e7c02#L23"]
spine_turn: Tưởng giá và nhắc lịch là nguyên nhân chính; hoá ra nhiều lý do trong đó liên quan đến sự liên tục của lễ tân.
spine_turn_lines: ["claude:5a1e7c02#L23", "claude:5a1e7c02#L29"]
spine_action: "Grep toàn bộ phỏng vấn tìm lễ tân, rồi đối chiếu danh sách nhân sự với tỷ lệ bỏ đi theo phòng khám."
spine_action_lines: ["claude:5a1e7c02#L27", "claude:5a1e7c02#L31"]
spine_outcome: "Phòng khám có 4 lễ tân nghỉ trong 12 tháng có tỷ lệ bỏ đi 41%; phòng có 0–1 người nghỉ là 19–24% (số do agent báo, mới 6 phòng khám)."
spine_outcome_lines: ["claude:5a1e7c02#L32", "claude:5a1e7c02#L33"]
spine_takeaway: "Khi một chi tiết lạc đề lặp lại trong phỏng vấn, hãy tra lại toàn bộ dữ liệu và đối chiếu với vận hành, nhưng ghi rõ cỡ mẫu nhỏ."
spine_takeaway_lines: ["claude:5a1e7c02#L29", "claude:5a1e7c02#L33"]
completeness: 7
---

# Trợ lý báo con số mà output công cụ không hiện: kiểm chứng trước khi đưa vào slide

**Góc kể:** Một chuỗi nha khoa đang nhờ nhóm nghiên cứu tìm vì sao bệnh nhân bỏ đi, dựa trên 14 buổi phỏng vấn và khảo sát. Nhóm ban đầu gom các lý do vào 'giá' và 'nhắc lịch', tưởng đó là nguyên nhân chính, và phía khách hàng cũng không nhắc đến lễ tân khi bắt đầu dự án. Một câu lỡ lời về cô lễ tân trong một buổi phỏng vấn, khi được tra lại cả bộ dữ liệu, lại cho thấy có bệnh nhân ở lại chỉ vì người đó. Phòng khám nào mất nhiều lễ tân hơn thì tỷ lệ bỏ đi cao hơn gần gấp đôi, dù mới chỉ 6 phòng khám nên đây là tương quan chứ chưa chắc là nhân quả.
**Bối cảnh:** Claude Code phân tích dữ liệu phỏng vấn và khảo sát cho dự án churn, và các số liệu được đưa thẳng vào bản synthesis để làm slide.
**Chuyện gì xảy ra:** Agent viết 'All 14 follow the same pattern' khi output chỉ thấy 2 tên file, và báo 3 phòng khám có churn 38% cùng nhóm 19 đến 24% dù output chỉ có một dòng. Với khảo sát, agent liệt kê đủ 6 lý do trong khi output rút gọn chỉ có dòng đầu với 97 người. Người dùng vẫn đưa các con số này vào synthesis như phát hiện số 1. Trong bản transcript rút gọn không thể khẳng định output bị cắt hay agent tự suy ra, nên cần xem log gốc trước buổi trình bày.
**Bài học:** Mỗi con số trong báo cáo cần truy được tới dòng output cụ thể. Yêu cầu trợ lý ghi kèm lệnh và kết quả gốc, và đừng đưa số vào slide khi chưa thấy nó trong output.
**Artefact:** Bảng đối chiếu: con số, lệnh đã chạy, dòng output tương ứng. Chụp màn hình output gốc, che tên thư mục và tên khách hàng.
**Góc người ngoài:** cách làm phổ biến là Lấy số từ phần đầu kết quả công cụ rồi trình bày như đã kiểm tra đầy đủ; ở đây khác ở Kết quả công cụ bị cắt, nhưng agent vẫn nêu các con số cụ thể. Người đọc cần biết cách kiểm tra số trước khi dùng cho người ra quyết định.
