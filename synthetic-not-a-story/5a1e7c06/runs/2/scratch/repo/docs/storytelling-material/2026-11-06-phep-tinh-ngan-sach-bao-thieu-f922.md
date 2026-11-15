---
id: 2026-11-06-phep-tinh-ngan-sach-bao-thieu-f922
code: M-6B1W
aliases: [M-6B1W]
date: 2026-11-06
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c06"
sessions: ["claude:5a1e7c06"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c06#L32", "claude:5a1e7c06#L33", "claude:5a1e7c06#L34", "claude:5a1e7c06#L35", "claude:5a1e7c06#L36"]
hook: "Script báo thiếu 12 triệu, cộng lại thật ra thiếu gần 20 triệu"
tension: tuong_ma_hoa_ra
sides: ["Script báo thiếu 12 triệu, và đã dùng làm cơ sở cắt một ban", "Cộng các khoản số trong phiên thì thiếu khoảng 19,6 triệu, chưa ai đối chiếu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người tổ chức đêm nhạc Gió Mùa (15/11) phải cắt chi phí sau ba thay đổi lớn: thêm dàn nhạc, mất cọc địa điểm cũ, hoàn 80 vé. Agent báo còn thiếu khoảng 12 triệu, và việc cắt suất diễn của một ban sinh viên được chốt theo con số đó. Nhưng cộng lại các khoản trong phiên thì thiếu khoảng 19,6 triệu, và khoản cắt được chỉ đủ 12 triệu. Người nghe nên quan tâm vì quyết định cắt theo một con số chưa đối chiếu có thể lệch cả chục triệu."
audience: người tổ chức sự kiện dùng AI để tính ngân sách
spine_context: "Đêm nhạc Gió Mùa diễn ra 15/11, cần xếp tình nguyện viên và gộp tech rider cho hai ban."
spine_context_lines: ["claude:5a1e7c06#L1"]
spine_want: Biết còn thiếu bao nhiêu để chọn khoản cắt.
spine_want_lines: ["claude:5a1e7c06#L32"]
spine_obstacle: "Thuê hai bộ thiết bị thêm 5,6 tr; sau ba thay đổi, ngân sách vẫn thiếu."
spine_obstacle_lines: ["claude:5a1e7c06#L30", "claude:5a1e7c06#L35"]
spine_turn: "Tưởng còn thiếu 12 tr; cộng các số trong phiên thì thiếu khoảng 19,6 tr."
spine_turn_lines: ["claude:5a1e7c06#L30", "claude:5a1e7c06#L33", "claude:5a1e7c06#L34", "claude:5a1e7c06#L35"]
spine_action: "Chạy script ngân sách với ba khoản thêm, rồi chốt cắt suất diễn của Mây Thấp và giữ kỹ thuật âm thanh."
spine_action_lines: ["claude:5a1e7c06#L33", "claude:5a1e7c06#L38"]
spine_outcome: "Mây Thấp bị cắt, tiết kiệm 12 tr; theo phép cộng trên vẫn thiếu khoảng 7,6 tr (tính từ 19,6 tr trừ 12 tr)."
spine_outcome_lines: ["claude:5a1e7c06#L35", "claude:5a1e7c06#L38"]
spine_takeaway: "Trước khi cắt khoản dựa trên một con số, tính lại từ tổng thu và tổng chi rồi đối chiếu."
spine_takeaway_lines: ["claude:5a1e7c06#L34", "claude:5a1e7c06#L35"]
completeness: 7
---

# Phép tính ngân sách báo thiếu 12 tr, nhưng số trong phiên cho thấy thiếu gần 20 tr

**Góc kể:** Người tổ chức đêm nhạc Gió Mùa (15/11) phải cắt chi phí sau ba thay đổi lớn: thêm dàn nhạc, mất cọc địa điểm cũ, hoàn 80 vé. Agent báo còn thiếu khoảng 12 triệu, và việc cắt suất diễn của một ban sinh viên được chốt theo con số đó. Nhưng cộng lại các khoản trong phiên thì thiếu khoảng 19,6 triệu, và khoản cắt được chỉ đủ 12 triệu. Người nghe nên quan tâm vì quyết định cắt theo một con số chưa đối chiếu có thể lệch cả chục triệu.
**Bối cảnh:** Sau ba thay đổi (thêm dàn nhạc, mất cọc địa điểm cũ, hoàn 80 vé), chủ sự kiện cần biết còn thiếu bao nhiêu để quyết định cắt khoản nào.
**Chuyện gì xảy ra:** Script báo thu 75 tr (300 vé) và chi cũ 66 tr, dư 9 tr. Cộng thêm 5,6 tr dàn nhạc, 3 tr cọc mất và 20 tr hoàn vé, phép tính đơn giản cho thấy thiếu khoảng 19,6 tr, không phải 12 tr như được báo. Khoản 12 tr đó đã là cơ sở để chọn cắt một ban diễn. Chênh lệch này chưa được đối chiếu lại.
**Bài học:** Trước khi cắt một khoản dựa trên một con số, in lại toàn bộ phép tính và đối chiếu với tổng thu chi; con số đầu ra của script không tự đảm bảo đúng.
**Artefact:** Kết quả script ngân sách (thu, chi, các khoản thêm). Không có thông tin nhạy cảm sau khi bỏ tên các khoản.
