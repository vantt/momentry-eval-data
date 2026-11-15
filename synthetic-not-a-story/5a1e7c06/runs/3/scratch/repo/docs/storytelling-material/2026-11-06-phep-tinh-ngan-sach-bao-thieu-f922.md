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
hook: "Báo thiếu 12 triệu, tính lại thiếu gần 20 triệu, mà đã cắt ban theo số sai"
tension: tuong_ma_hoa_ra
sides: ["Script báo thiếu 12 triệu, đã dùng để chọn cắt một ban", "Cộng lại các khoản thì thiếu khoảng 19,6 triệu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang tổ chức đêm nhạc Gió Mùa vào 15/11 với hai ban nhạc chia sẻ một sân khấu nhỏ. Ban đầu họ tin hai ban dùng chung được vì sân khấu còn trống, nhưng rider in-ear và ampli đèn của hai bên không chung được, và ngân sách thiếu khoảng 12 triệu. Cuối cùng họ giữ kỹ thuật viên và cắt suất diễn của một ban sinh viên, bù bằng hát mộc và lời hứa suất mở màn; người tổ chức event nhỏ nên kiểm tra rider trước khi tin hai đội dùng chung được."
audience: người tổ chức sự kiện âm nhạc nhỏ
spine_context: "Người làm đang tổ chức đêm nhạc Gió Mùa vào 15/11, có tình nguyện viên và hai ban nhạc cần chia sẻ kỹ thuật."
spine_context_lines: ["claude:5a1e7c06#L1"]
spine_want: Muốn đêm nhạc của 220 người không bị hỏng.
spine_want_lines: ["claude:5a1e7c06#L37"]
spine_obstacle: "Hai ban có rider khó: in-ear và ampli đèn trên một sân khấu nhỏ, và ngân sách thiếu khoảng 12 triệu."
spine_obstacle_lines: ["claude:5a1e7c06#L35", "claude:5a1e7c06#L36"]
spine_turn: "Người làm và hai ban ban đầu tin dùng chung được, kiểu 'trống là trống'; hoá ra rider của hai bên không chung được, phải chọn giữa kỹ thuật viên và suất diễn của một ban."
spine_turn_lines: ["claude:5a1e7c06#L27", "claude:5a1e7c06#L36"]
spine_action: "Thử thuê hai dàn, tính lại ngân sách, rồi giữ kỹ thuật viên và cắt suất diễn của ban sinh viên, bù bằng hát mộc 5 phút và hứa suất mở màn buổi sau."
spine_action_lines: ["claude:5a1e7c06#L31", "claude:5a1e7c06#L33", "claude:5a1e7c06#L35", "claude:5a1e7c06#L38"]
spine_outcome: "Giữ được kỹ thuật viên; ban sinh viên mất suất diễn lớn đầu tiên, nhận hát mộc lúc đón khách và lời hứa suất mở màn."
spine_outcome_lines: ["claude:5a1e7c06#L38"]
spine_takeaway: "Kiểm tra rider trước khi tin hai đội dùng chung được; nếu phải cắt đội đã hứa, bù bằng việc cụ thể và nói trực tiếp."
spine_takeaway_lines: ["claude:5a1e7c06#L27", "claude:5a1e7c06#L37", "claude:5a1e7c06#L38"]
completeness: 7
---

# Phép tính ngân sách báo thiếu 12 tr, nhưng số trong phiên cho thấy thiếu gần 20 tr

**Góc kể:** Người làm đang tổ chức đêm nhạc Gió Mùa vào 15/11 với hai ban nhạc chia sẻ một sân khấu nhỏ. Ban đầu họ tin hai ban dùng chung được vì sân khấu còn trống, nhưng rider in-ear và ampli đèn của hai bên không chung được, và ngân sách thiếu khoảng 12 triệu. Cuối cùng họ giữ kỹ thuật viên và cắt suất diễn của một ban sinh viên, bù bằng hát mộc và lời hứa suất mở màn; người tổ chức event nhỏ nên kiểm tra rider trước khi tin hai đội dùng chung được.
**Bối cảnh:** Sau ba thay đổi (thêm dàn nhạc, mất cọc địa điểm cũ, hoàn 80 vé), chủ sự kiện cần biết còn thiếu bao nhiêu để quyết định cắt khoản nào.
**Chuyện gì xảy ra:** Script báo thu 75 tr (300 vé) và chi cũ 66 tr, dư 9 tr. Cộng thêm 5,6 tr dàn nhạc, 3 tr cọc mất và 20 tr hoàn vé, phép tính đơn giản cho thấy thiếu khoảng 19,6 tr, không phải 12 tr như được báo. Khoản 12 tr đó đã là cơ sở để chọn cắt một ban diễn. Chênh lệch này chưa được đối chiếu lại.
**Bài học:** Trước khi cắt một khoản dựa trên một con số, in lại toàn bộ phép tính và đối chiếu với tổng thu chi; con số đầu ra của script không tự đảm bảo đúng.
**Artefact:** Kết quả script ngân sách (thu, chi, các khoản thêm). Không có thông tin nhạy cảm sau khi bỏ tên các khoản.
