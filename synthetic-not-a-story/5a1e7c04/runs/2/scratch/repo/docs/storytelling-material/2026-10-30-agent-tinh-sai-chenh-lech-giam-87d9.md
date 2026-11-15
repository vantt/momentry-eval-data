---
id: 2026-10-30-agent-tinh-sai-chenh-lech-giam-87d9
code: M-80HA
aliases: [M-80HA]
date: 2026-10-30
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c04#L36", "claude:5a1e7c04#L38"]
hook: "Agent tính sai 70k thay vì 103,5k mỗi đơn, thiệt hại thấp hơn một phần ba"
tension: tuong_ma_hoa_ra
sides: ["Người dùng quyết định dựa trên con số 35 triệu nghe có vẻ chắc", "Tính đúng thì 400 đơn khoảng 41 triệu, trần 500 khoảng 52 triệu"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang lo đợt ra mắt serum vitamin C tuần đầu, thì mã thử nội bộ GLOW30 lộ ra qua một người ảnh hưởng, trong khi đồng nghiệp đang trên máy bay. Để chọn cách xử lý, họ cần biết mã này làm mất bao nhiêu lợi nhuận, và agent báo chênh lệch mỗi đơn là khoảng 70k. Nhưng 15% của giá 690k là 103,5k, nên con số thiệt hại bị đánh giá thấp gần một phần ba. Ai dùng AI để tính số gấp nên tự nhân lại trước khi tin."
audience: dev dùng AI để tính số khi ra quyết định gấp
spine_context: "Người làm đang lo đợt ra mắt serum vitamin C tuần đầu, có người ảnh hưởng đăng mã giảm giá cho khách."
spine_context_lines: ["claude:5a1e7c04#L1", "claude:5a1e7c04#L35"]
spine_want: Cần biết mã GLOW30 đang làm mất bao nhiêu lợi nhuận để chọn cách xử lý.
spine_want_lines: ["claude:5a1e7c04#L35", "claude:5a1e7c04#L36"]
spine_obstacle: "Mã thử nội bộ GLOW30 còn hoạt động, và đồng nghiệp đang trên máy bay, không liên lạc được ngay."
spine_obstacle_lines: ["claude:5a1e7c04#L35"]
spine_turn: "Agent tính chênh lệch mỗi đơn là khoảng 70k; hoá ra 15% của 690k là 103,5k, nên thiệt hại bị đánh giá thấp gần một phần ba."
spine_turn_lines: ["claude:5a1e7c04#L36"]
spine_action: Người làm chọn giữ GLOW30 với trần 500 lượt và làm theo các bước agent đưa ra.
spine_action_lines: ["claude:5a1e7c04#L37", "claude:5a1e7c04#L38"]
spine_outcome: "Khi đó GLOW30 đã có 431 lượt dùng, còn con số 35 triệu cho 500 lượt được đưa ra dựa trên phép tính sai."
spine_outcome_lines: ["claude:5a1e7c04#L38", "claude:5a1e7c04#L40"]
spine_takeaway: "Khi AI đưa số để quyết định gấp, tự nhân lại phép đơn giản (giá × phần trăm × số đơn) trước khi tin."
spine_takeaway_lines: ["claude:5a1e7c04#L36", "claude:5a1e7c04#L38"]
completeness: 7
---

# Agent tính sai chênh lệch giảm giá, khiến thiệt hại bị đánh giá thấp khoảng một phần ba

**Góc kể:** Người làm đang lo đợt ra mắt serum vitamin C tuần đầu, thì mã thử nội bộ GLOW30 lộ ra qua một người ảnh hưởng, trong khi đồng nghiệp đang trên máy bay. Để chọn cách xử lý, họ cần biết mã này làm mất bao nhiêu lợi nhuận, và agent báo chênh lệch mỗi đơn là khoảng 70k. Nhưng 15% của giá 690k là 103,5k, nên con số thiệt hại bị đánh giá thấp gần một phần ba. Ai dùng AI để tính số gấp nên tự nhân lại trước khi tin.
**Bối cảnh:** Trong sự cố, người dùng cần con số để chọn giữa tắt mã và giữ mã với trần, nên con số này ảnh hưởng trực tiếp đến quyết định.
**Chuyện gì xảy ra:** Agent viết chênh lệch mỗi đơn là khoảng 70k và 400 đơn khoảng 28 triệu. Nhưng 690k nhân 15% là 103,5k, nên chênh lệch đúng là khoảng 103,5k mỗi đơn. Theo cách tính đúng, 400 đơn khoảng 41 triệu, và trần 500 khoảng 52 triệu so với mức 15%. Con số 35 triệu mà người dùng dựa vào để quyết định thấp hơn khoảng một phần ba. Kết luận chọn trần vẫn có thể đúng, nhưng cần tính lại với số đúng.
**Bài học:** Khi báo số để ra quyết định gấp, hãy ghi rõ công thức và số đầu vào, và tự kiểm lại phép nhân cơ bản trước khi gửi.
**Artefact:** Bảng tính gồm giá, chênh lệch phần trăm và số đơn, không cần chụp ảnh.
