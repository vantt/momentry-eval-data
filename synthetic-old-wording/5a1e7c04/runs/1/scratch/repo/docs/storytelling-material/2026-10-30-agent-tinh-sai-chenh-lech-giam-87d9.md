---
id: 2026-10-30-agent-tinh-sai-chenh-lech-giam-87d9
code: M-80HA
aliases: [M-80HA]
date: 2026-10-30
repo: repo
status: raw
signals: [số trước-sau, khác]
source: "chat Claude, claude:5a1e7c04"
sessions: ["claude:5a1e7c04"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c04#L36", "claude:5a1e7c04#L38"]
hook: "Agent tính chênh lệch 70k một đơn, thực ra là 103,5k"
tension: nguoi_dung_may_sai
sides: ["agent tính 400 đơn thiệt khoảng 28 triệu", "phép nhân đúng ra khoảng 41 triệu, thấp hơn một phần ba"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Đang chạy tuần ra mắt serum vitamin C thì một mã test nhân viên chưa xoá lọt vào bài đăng của influencer, và người làm nhờ AI tính xem thiệt bao nhiêu. AI báo chênh lệch mỗi đơn khoảng 70k và tổng khoảng 35 triệu cho trần 500 lượt, nhưng 690k nhân 15% là 103,5k, nên con số đúng gần 52 triệu, cao hơn gần một phần ba. Kết luận giữ mã có trần có thể vẫn đúng, nhưng quyết định gấp đã dựa trên số sai. Ai dùng AI để tính số trước khi quyết định nên kiểm lại phép nhân cơ bản."
audience: dev và người làm sản phẩm dùng AI để tính số khi phải quyết định gấp
spine_context: "Đang chạy tuần ra mắt serum vitamin C, tối mai 8 giờ có influencer đăng mã giảm giá."
spine_context_lines: ["claude:5a1e7c04#L1", "claude:5a1e7c04#L35"]
spine_want: Cần con số thiệt hại để chọn giữa tắt mã và giữ mã có trần.
spine_want_lines: ["claude:5a1e7c04#L37"]
spine_obstacle: "Mã GLOW30 là mã test cho nhân viên chưa xoá, đã dùng 400 lần trong lúc influencer đăng nhầm mã."
spine_obstacle_lines: ["claude:5a1e7c04#L35"]
spine_turn: "Agent tưởng chênh lệch mỗi đơn là khoảng 70k; hoá ra 690k nhân 15% là 103,5k."
spine_turn_lines: ["claude:5a1e7c04#L36"]
spine_action: "Người làm chọn giữ GLOW30 với trần 500 lượt, dựa trên con số 35 triệu."
spine_action_lines: ["claude:5a1e7c04#L37", "claude:5a1e7c04#L38"]
spine_outcome: "Lúc kiểm tra GLOW30 đã có 431 lượt dùng; con số 35 triệu thấp hơn cách tính đúng khoảng 52 triệu (500 × 103,5k)."
spine_outcome_lines: ["claude:5a1e7c04#L38", "claude:5a1e7c04#L40"]
spine_takeaway: "Khi báo số để ra quyết định gấp, ghi rõ công thức và số đầu vào, và tự kiểm lại phép nhân trước khi gửi."
spine_takeaway_lines: ["claude:5a1e7c04#L36"]
completeness: 7
---

# Agent tính sai chênh lệch giảm giá, khiến thiệt hại bị đánh giá thấp khoảng một phần ba

**Góc kể:** Đang chạy tuần ra mắt serum vitamin C thì một mã test nhân viên chưa xoá lọt vào bài đăng của influencer, và người làm nhờ AI tính xem thiệt bao nhiêu. AI báo chênh lệch mỗi đơn khoảng 70k và tổng khoảng 35 triệu cho trần 500 lượt, nhưng 690k nhân 15% là 103,5k, nên con số đúng gần 52 triệu, cao hơn gần một phần ba. Kết luận giữ mã có trần có thể vẫn đúng, nhưng quyết định gấp đã dựa trên số sai. Ai dùng AI để tính số trước khi quyết định nên kiểm lại phép nhân cơ bản.
**Bối cảnh:** Trong sự cố, người dùng cần con số để chọn giữa tắt mã và giữ mã với trần, nên con số này ảnh hưởng trực tiếp đến quyết định.
**Chuyện gì xảy ra:** Agent viết chênh lệch mỗi đơn là khoảng 70k và 400 đơn khoảng 28 triệu. Nhưng 690k nhân 15% là 103,5k, nên chênh lệch đúng là khoảng 103,5k mỗi đơn. Theo cách tính đúng, 400 đơn khoảng 41 triệu, và trần 500 khoảng 52 triệu so với mức 15%. Con số 35 triệu mà người dùng dựa vào để quyết định thấp hơn khoảng một phần ba. Kết luận chọn trần vẫn có thể đúng, nhưng cần tính lại với số đúng.
**Bài học:** Khi báo số để ra quyết định gấp, hãy ghi rõ công thức và số đầu vào, và tự kiểm lại phép nhân cơ bản trước khi gửi.
**Artefact:** Bảng tính gồm giá, chênh lệch phần trăm và số đơn, không cần chụp ảnh.
