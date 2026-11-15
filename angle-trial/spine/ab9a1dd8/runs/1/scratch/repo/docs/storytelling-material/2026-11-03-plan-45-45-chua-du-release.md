---
id: 2026-11-03-plan-45-45-chua-du-release
date: 2026-11-03
repo: repo
status: raw
signals: [người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L2994", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3042", "claude:ab9a1dd8#L3047"]
hook: "Plan xong 45/45 việc, nhưng chưa tính là xong"
tension: tuong_ma_hoa_ra
sides: ["Cả 45 việc trong plan đã đánh dấu xong", "Stop hook bắt làm tiếp tới khi release thật chạy xanh"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang làm gói cài đặt để người khác dùng được. Plan đã đánh dấu 45/45 việc và Linux xanh, nên tưởng là xong; nhưng lần push đầu lên CI, macOS và Windows đỏ ở những lỗi Linux không thấy. Plan xong chưa phải release xong: chỉ đóng việc khi bản phát hành thật có lệnh cài một dòng chạy được. Ai làm CLI đa nền tảng sẽ gặp đúng chỗ này."
audience: "dev làm CLI hoặc công cụ đa nền tảng, build in public"
spine_context: "Công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang làm gói cài đặt để người khác dùng được."
spine_context_lines: [profile, "claude:ab9a1dd8#L2230"]
spine_want: "Hoàn tất plan đóng gói và phân phối, để người dùng cài bằng một lệnh."
spine_want_lines: ["claude:ab9a1dd8#L664"]
spine_obstacle: "Linux xanh hết, nhưng CI trên macOS và Windows chưa từng chạy."
spine_obstacle_lines: ["claude:ab9a1dd8#L2230", "claude:ab9a1dd8#L2945"]
spine_turn: "Tưởng xong vì 45/45 việc và Linux xanh; hoá ra lần push đầu lên CI, macOS và Windows đỏ ở những lỗi Linux không thấy."
spine_turn_lines: ["claude:ab9a1dd8#L2230", "claude:ab9a1dd8#L2945"]
spine_action: "Sửa các lỗi macOS và Windows, push lên main, rồi cắt v0.1.0 và thử lệnh cài từ GitHub."
spine_action_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3042"]
spine_outcome: "CI 9/9 tổ hợp xanh; v0.1.0 công bố, lệnh cài một dòng chạy được. Hook trên Windows với Claude Code và Codex thật vẫn chưa đo, chuyển thành issue."
spine_outcome_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3042", "claude:ab9a1dd8#L3047"]
spine_takeaway: "Plan đánh dấu xong chưa phải release xong; chỉ đóng việc khi lệnh cài thật chạy được từ nguồn công khai, và CI đa nền tảng phải chạy trước."
spine_takeaway_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3042"]
completeness: 7
---

# Plan 45/45 chưa đủ: release thật mới đóng được việc

**Góc kể:** Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang làm gói cài đặt để người khác dùng được. Plan đã đánh dấu 45/45 việc và Linux xanh, nên tưởng là xong; nhưng lần push đầu lên CI, macOS và Windows đỏ ở những lỗi Linux không thấy. Plan xong chưa phải release xong: chỉ đóng việc khi bản phát hành thật có lệnh cài một dòng chạy được. Ai làm CLI đa nền tảng sẽ gặp đúng chỗ này.
**Bối cảnh:** Stop hook của phiên yêu cầu làm tới khi hoàn tất. Plan đã đánh dấu 45/45 việc.
**Chuyện gì xảy ra:** Ba lần stop hook bắt agent làm tiếp: đẩy lên main, chạy CI thật trên 9 tổ hợp, rồi cắt v0.1.0. Release chạy xanh từ đầu đến cuối trong một lần, và lệnh cài một dòng trong README chạy được với bản vừa phát hành.
**Bài học:** Plan xong khác release xong. Chỉ đóng việc khi lệnh cài thật chạy được từ nguồn công khai.
**Artefact:** Trang release trên GitHub và đầu ra lệnh cài trong HOME tạm. Che tên người dùng.
