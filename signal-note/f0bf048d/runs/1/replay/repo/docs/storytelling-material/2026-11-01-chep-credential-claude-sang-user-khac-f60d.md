---
id: 2026-11-01-chep-credential-claude-sang-user-khac-f60d
code: M-9TP6
aliases: [M-9TP6]
date: 2026-11-01
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L3502", "claude:f0bf048d#L3505", "claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
hook: "Chép credential sang user khác chạy tốt, đến khi token tự làm mới"
tension: giup_ma_hai
sides: ["copy credentials cho nhanh", "một bên làm mới token thì bên kia 401 giữa lúc chạy cho khách"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một hệ thống agent nghiệp vụ chạy trên máy chủ, và người làm đang tách việc vận hành sang một user Linux riêng. Phiên Claude Code nằm trong home của từng user, nên user mới chưa có phiên nào. Chép file đăng nhập sang cho nhanh nghe hợp lý, nhưng token OAuth tự làm mới theo chu kỳ: bản nào làm mới trước sẽ làm bản kia hết hạn, và agent đang chạy có thể lỗi 401 giữa chừng. Ai chia sẻ credential giữa các user trên máy chủ nên biết điều này trước."
audience: dev vận hành máy chủ có agent AI dùng Claude Code
spine_context: "Máy chủ đang tách việc vận hành agent nghiệp vụ sang một user Linux riêng, và user mới cần phiên Claude Code riêng."
spine_context_lines: ["claude:f0bf048d#L3502", "claude:f0bf048d#L3505"]
spine_want: Muốn user mới dùng được Claude mà không phải đăng nhập lại.
spine_want_lines: ["claude:f0bf048d#L3502"]
spine_obstacle: "Mỗi user Linux có phiên Claude Code riêng trong home, nên user mới chưa có phiên nào."
spine_obstacle_lines: ["claude:f0bf048d#L3505"]
spine_turn: "Tưởng chép file đăng nhập sang là dùng chung được lâu dài; hoá ra token OAuth tự làm mới, bản chép còn lại sẽ hỏng."
spine_turn_lines: ["claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
spine_action: "Đưa lệnh chép file đăng nhập sang user mới, và khuyên vẫn /login riêng."
spine_action_lines: ["claude:f0bf048d#L3516"]
spine_takeaway: Hai bản sao token OAuth đá nhau khi làm mới; mỗi user Linux nên đăng nhập riêng.
spine_takeaway_lines: ["claude:f0bf048d#L3505", "claude:f0bf048d#L3516"]
completeness: 6
---

# Chép credential Claude sang user khác: token tự làm mới làm hỏng bản còn lại

**Góc kể:** Dự án là một hệ thống agent nghiệp vụ chạy trên máy chủ, và người làm đang tách việc vận hành sang một user Linux riêng. Phiên Claude Code nằm trong home của từng user, nên user mới chưa có phiên nào. Chép file đăng nhập sang cho nhanh nghe hợp lý, nhưng token OAuth tự làm mới theo chu kỳ: bản nào làm mới trước sẽ làm bản kia hết hạn, và agent đang chạy có thể lỗi 401 giữa chừng. Ai chia sẻ credential giữa các user trên máy chủ nên biết điều này trước.
**Bối cảnh:** Tách user opc-ops cần phiên Claude Code riêng, và chủ hỏi vì sao phải login lại khi máy đã có Claude.
**Chuyện gì xảy ra:** Mỗi user Linux có phiên riêng trong home. Copy file credentials dùng chung thì lúc đầu chạy được, nhưng khi một bên tự làm mới token, bên kia sẽ lỗi 401 giữa chừng, thường đúng lúc đang chạy việc cho khách. Agent khuyên login lại cùng tài khoản, mất khoảng một phút.
**Bài học:** Token OAuth tự làm mới khiến hai bản sao đá nhau. Mỗi user Linux nên có phiên đăng nhập riêng.
**Artefact:** Không có.
