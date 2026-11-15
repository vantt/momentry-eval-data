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
hook: "Agent tính 70k mỗi đơn, đúng ra là 103,5k, thiệt hại lệch một phần ba"
tension: tuong_ma_hoa_ra
sides: ["Người dùng quyết định dựa trên con số 35 triệu của agent", "690k nhân 15% ra 103,5k, nên 400 đơn gần 41 triệu"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tính sai chênh lệch giảm giá, khiến thiệt hại bị đánh giá thấp khoảng một phần ba

**Bối cảnh:** Trong sự cố, người dùng cần con số để chọn giữa tắt mã và giữ mã với trần, nên con số này ảnh hưởng trực tiếp đến quyết định.
**Chuyện gì xảy ra:** Agent viết chênh lệch mỗi đơn là khoảng 70k và 400 đơn khoảng 28 triệu. Nhưng 690k nhân 15% là 103,5k, nên chênh lệch đúng là khoảng 103,5k mỗi đơn. Theo cách tính đúng, 400 đơn khoảng 41 triệu, và trần 500 khoảng 52 triệu so với mức 15%. Con số 35 triệu mà người dùng dựa vào để quyết định thấp hơn khoảng một phần ba. Kết luận chọn trần vẫn có thể đúng, nhưng cần tính lại với số đúng.
**Bài học:** Khi báo số để ra quyết định gấp, hãy ghi rõ công thức và số đầu vào, và tự kiểm lại phép nhân cơ bản trước khi gửi.
**Artefact:** Bảng tính gồm giá, chênh lệch phần trăm và số đơn, không cần chụp ảnh.
