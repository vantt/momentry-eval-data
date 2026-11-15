---
id: 2026-11-06-phep-tinh-ngan-sach-bao-thieu-f922
code: M-6B1W
aliases: [M-6B1W]
date: 2026-11-06
repo: repo
status: raw
signals: ["1. Số trước, số sau", 3. Điều tưởng đúng hoá sai]
source: "chat Claude, claude:5a1e7c06"
sessions: ["claude:5a1e7c06"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c06#L32", "claude:5a1e7c06#L33", "claude:5a1e7c06#L34", "claude:5a1e7c06#L35", "claude:5a1e7c06#L36"]
hook: "Báo thiếu 12 triệu, cộng lại thiếu gần 20 triệu, mà đã cắt ban theo số 12"
tension: tuong_ma_hoa_ra
sides: ["Script báo thiếu 12 triệu và quyết định dựa trên đó", "Cộng tay thiếu khoảng 19,6 triệu, chưa ai đối chiếu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Đêm nhạc Gió Mùa (15/11) đang chuẩn bị, người làm phải xếp lại ngân sách sau khi thêm dàn nhạc, mất cọc địa điểm cũ và hoàn vé. Phép tính trong phiên báo thiếu khoảng 12 triệu, nên quyết định cắt ban mở màn để bù. Cộng lại từ các số đã có thì thiếu gần 19,6 triệu, nghĩa là cắt như vậy vẫn còn thiếu hơn 7 triệu. Ai tin một con số đầu ra mà không cộng lại từ khoản gốc có thể cắt nhầm."
audience: dev dùng AI để tính số liệu và người làm việc với bảng chi thu
spine_context: "Đêm nhạc Gió Mùa (15/11) đang chuẩn bị, cần xếp tình nguyện viên và gộp tech rider của hai ban nhạc."
spine_context_lines: ["claude:5a1e7c06#L1"]
spine_want: Giữ đủ kỹ thuật cho đêm nhạc mà vẫn nằm trong ngân sách.
spine_want_lines: ["claude:5a1e7c06#L32"]
spine_obstacle: "Sau ba thay đổi (thêm dàn nhạc, mất cọc địa điểm cũ, hoàn vé), ngân sách không còn đủ."
spine_obstacle_lines: ["claude:5a1e7c06#L35"]
spine_turn: "Phép tính trong phiên báo thiếu khoảng 12 triệu; cộng lại từ các khoản đã có thì thiếu khoảng 19,6 triệu."
spine_turn_lines: ["claude:5a1e7c06#L34", "claude:5a1e7c06#L35"]
spine_action: "Giữ kỹ thuật âm thanh, cắt ban mở màn để bù khoản thiếu."
spine_action_lines: ["claude:5a1e7c06#L38"]
spine_outcome: "Quyết định cắt đã chốt; theo phép cộng, sau khi cắt vẫn thiếu khoảng 7,6 triệu."
spine_outcome_lines: ["claude:5a1e7c06#L34", "claude:5a1e7c06#L35", "claude:5a1e7c06#L38"]
spine_takeaway: "Trước khi cắt khoản nào dựa trên một con số, cộng lại từ các khoản gốc thay vì tin con số đã nói ra."
spine_takeaway_lines: ["claude:5a1e7c06#L34", "claude:5a1e7c06#L35"]
completeness: 7
---

# Phép tính ngân sách báo thiếu 12 tr, nhưng số trong phiên cho thấy thiếu gần 20 tr

**Góc kể:** Đêm nhạc Gió Mùa (15/11) đang chuẩn bị, người làm phải xếp lại ngân sách sau khi thêm dàn nhạc, mất cọc địa điểm cũ và hoàn vé. Phép tính trong phiên báo thiếu khoảng 12 triệu, nên quyết định cắt ban mở màn để bù. Cộng lại từ các số đã có thì thiếu gần 19,6 triệu, nghĩa là cắt như vậy vẫn còn thiếu hơn 7 triệu. Ai tin một con số đầu ra mà không cộng lại từ khoản gốc có thể cắt nhầm.
**Bối cảnh:** Sau ba thay đổi (thêm dàn nhạc, mất cọc địa điểm cũ, hoàn 80 vé), chủ sự kiện cần biết còn thiếu bao nhiêu để quyết định cắt khoản nào.
**Chuyện gì xảy ra:** Script báo thu 75 tr (300 vé) và chi cũ 66 tr, dư 9 tr. Cộng thêm 5,6 tr dàn nhạc, 3 tr cọc mất và 20 tr hoàn vé, phép tính đơn giản cho thấy thiếu khoảng 19,6 tr, không phải 12 tr như được báo. Khoản 12 tr đó đã là cơ sở để chọn cắt một ban diễn. Chênh lệch này chưa được đối chiếu lại.
**Bài học:** Trước khi cắt một khoản dựa trên một con số, in lại toàn bộ phép tính và đối chiếu với tổng thu chi; con số đầu ra của script không tự đảm bảo đúng.
**Artefact:** Kết quả script ngân sách (thu, chi, các khoản thêm). Không có thông tin nhạy cảm sau khi bỏ tên các khoản.
