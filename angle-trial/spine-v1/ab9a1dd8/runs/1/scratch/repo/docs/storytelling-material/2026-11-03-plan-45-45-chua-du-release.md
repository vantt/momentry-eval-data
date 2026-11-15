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
angle: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build in public đang hoàn tất đợt đóng gói và phát hành. Agent đã báo xong với 45/45 việc và Linux xanh hết, nhưng khi push lên GitHub thì macOS và Windows đỏ, còn stop hook không cho dừng cho tới khi bản phát hành thật cài được. Ai đóng gói CLI đa nền tảng nên biết: plan xong chưa phải release xong."
audience: dev làm công cụ CLI đa nền tảng và đóng gói phần mềm
spine_context: Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build in public; đang hoàn tất plan đóng gói và phân phối.
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Hoàn tất plan đóng gói tới mức tốt đẹp, không chỉ đánh dấu xong các việc trong plan."
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233"]
spine_obstacle: "Linux xanh hết, nhưng việc còn lại cần push lên GitHub để CI chạy lần đầu, và máy này không có Windows."
spine_obstacle_lines: ["claude:ab9a1dd8#L2230"]
spine_turn: "Tưởng xong vì 45/45 việc đã đánh dấu và Linux xanh; hoá ra push lên thì macOS và Windows đỏ, và stop hook vẫn không cho dừng cho tới khi bản phát hành thật cài được."
spine_turn_lines: ["claude:ab9a1dd8#L2230", "claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L2948"]
spine_action: "Sửa lỗi macOS (đường dẫn qua symlink) và Windows (tên thư mục ngắn, PowerShell 5.1, quyền Administrator), rồi cắt v0.1.0 để release.yml chạy thật."
spine_action_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3021"]
spine_outcome: "CI xanh 9/9 tổ hợp; v0.1.0 đã công bố, và lệnh cài một dòng cài được đúng bản đó từ GitHub."
spine_outcome_lines: ["claude:ab9a1dd8#L2945", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3042"]
spine_takeaway: "Plan xong chưa phải xong: chỉ đóng việc khi lệnh cài thật chạy được từ nguồn công khai."
spine_takeaway_lines: ["claude:ab9a1dd8#L2948", "claude:ab9a1dd8#L3042"]
completeness: 7
---

# Plan 45/45 chưa đủ: release thật mới đóng được việc

**Góc kể:** Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu build in public đang hoàn tất đợt đóng gói và phát hành. Agent đã báo xong với 45/45 việc và Linux xanh hết, nhưng khi push lên GitHub thì macOS và Windows đỏ, còn stop hook không cho dừng cho tới khi bản phát hành thật cài được. Ai đóng gói CLI đa nền tảng nên biết: plan xong chưa phải release xong.
**Bối cảnh:** Stop hook của phiên yêu cầu làm tới khi hoàn tất. Plan đã đánh dấu 45/45 việc.
**Chuyện gì xảy ra:** Ba lần stop hook bắt agent làm tiếp: đẩy lên main, chạy CI thật trên 9 tổ hợp, rồi cắt v0.1.0. Release chạy xanh từ đầu đến cuối trong một lần, và lệnh cài một dòng trong README chạy được với bản vừa phát hành.
**Bài học:** Plan xong khác release xong. Chỉ đóng việc khi lệnh cài thật chạy được từ nguồn công khai.
**Artefact:** Trang release trên GitHub và đầu ra lệnh cài trong HOME tạm. Che tên người dùng.
