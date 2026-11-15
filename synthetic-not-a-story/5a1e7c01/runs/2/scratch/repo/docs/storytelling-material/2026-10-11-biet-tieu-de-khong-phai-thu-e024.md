---
id: 2026-10-11-biet-tieu-de-khong-phai-thu-e024
code: M-2N78
aliases: [M-2N78]
date: 2026-10-11
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L60", "claude:5a1e7c01#L61", "claude:5a1e7c01#L62", "claude:5a1e7c01#L63", "claude:5a1e7c01#L64", "claude:5a1e7c01#L65"]
hook: "Biết tiêu đề không có lỗi, chủ bản tin vẫn xin 10 tiêu đề"
tension: khac
sides: ["đã biết tiêu đề không phải thủ phạm làm tụt tỉ lệ mở", "vẫn xin 10 gợi ý và chọn tiêu đề dài hơn kèm tiền tố"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Thư Chủ Nhật là bản tin email hằng tuần, và người làm đang viết số 48 về quỹ khẩn cấp. Người làm từng nghĩ tiêu đề là lý do, nhưng hoá ra không phải tại tiêu đề. Bài vẫn cần một tiêu đề, nên họ chọn một cái dài hơn kèm tiền tố. Ai viết email hay thông báo cho người khác đọc sẽ thấy điều này quen."
audience: người viết email hoặc thông báo cho người đọc
spine_context: "Thư Chủ Nhật là bản tin email hằng tuần, người làm đang viết số 48 về quỹ khẩn cấp."
spine_context_lines: ["claude:5a1e7c01#L1", "claude:5a1e7c01#L50"]
spine_want: "Viết xong số 48 với một tiêu đề, dù đã biết tiêu đề không phải nguyên nhân."
spine_want_lines: ["claude:5a1e7c01#L1", "claude:5a1e7c01#L60"]
spine_turn: Tưởng tiêu đề là lý do; hoá ra không phải tại tiêu đề.
spine_turn_lines: ["claude:5a1e7c01#L60"]
spine_action: "Nhận 10 gợi ý, chọn số 2, thêm tiền tố 'Quỹ khẩn cấp:', rồi cập nhật dòng đầu bài."
spine_action_lines: ["claude:5a1e7c01#L61", "claude:5a1e7c01#L62", "claude:5a1e7c01#L63", "claude:5a1e7c01#L65"]
spine_outcome: "Dòng đầu bài đã đổi thành 'Quỹ khẩn cấp: 20 triệu đã đủ chưa?'."
spine_outcome_lines: ["claude:5a1e7c01#L63", "claude:5a1e7c01#L65"]
spine_takeaway: Chẩn đoán cho thấy một yếu tố không phải nguyên nhân không có nghĩa là bỏ việc vẫn phải làm.
spine_takeaway_lines: ["claude:5a1e7c01#L60", "claude:5a1e7c01#L62"]
completeness: 6
---

# Biết tiêu đề không phải thủ phạm, chủ bản tin vẫn xin 10 tiêu đề và chọn số 2

**Góc kể:** Thư Chủ Nhật là bản tin email hằng tuần, và người làm đang viết số 48 về quỹ khẩn cấp. Người làm từng nghĩ tiêu đề là lý do, nhưng hoá ra không phải tại tiêu đề. Bài vẫn cần một tiêu đề, nên họ chọn một cái dài hơn kèm tiền tố. Ai viết email hay thông báo cho người khác đọc sẽ thấy điều này quen.
**Bối cảnh:** Sau khi chẩn đoán xong rằng tiêu đề không gây tụt tỉ lệ mở, chủ bản tin vẫn cần tiêu đề cho số 48 vì đó là việc phải làm của bài.
**Chuyện gì xảy ra:** Chủ bản tin nói rõ ngắn dài lẫn lộn cũng được, và cười rằng giờ đã biết không phải tại tiêu đề. Agent đưa 10 gợi ý, chủ chọn số 2 là '20 triệu đã đủ chưa?' và thêm tiền tố 'Quỹ khẩn cấp:' dù tiêu đề dài hơn. Agent cập nhật dòng đầu bài trong một lần sửa.
**Bài học:** Tiêu đề vẫn là thứ người đọc thấy đầu tiên, dù nó không phải nguyên nhân số liệu; đừng bỏ việc viết nó chỉ vì một lần chẩn đoán đã sai hướng.
**Artefact:** Danh sách 10 tiêu đề gốc để so sánh với tiêu đề được chọn.
