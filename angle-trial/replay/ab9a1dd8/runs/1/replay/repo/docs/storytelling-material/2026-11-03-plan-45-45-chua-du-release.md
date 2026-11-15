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
angle: "Agent báo đã xong 45/45 việc trong plan và CI xanh, nên tưởng là đóng được việc. Hoá ra hook dừng việc lại vì chưa có bản phát hành thật: cài thử từ GitHub mới là bằng chứng. Dev dùng AI agent nên cần nhớ: tick 'xong' trong plan chưa chứng minh được hệ thống chạy được, và trong chuyện này phần hook trên Windows vẫn chưa đo trong phiên thật."
audience: dev dùng AI agent để viết code và muốn biết khi nào agent thật sự xong việc
---

# Plan 45/45 chưa đủ: release thật mới đóng được việc

**Góc kể:** Agent báo đã xong 45/45 việc trong plan và CI xanh, nên tưởng là đóng được việc. Hoá ra hook dừng việc lại vì chưa có bản phát hành thật: cài thử từ GitHub mới là bằng chứng. Dev dùng AI agent nên cần nhớ: tick 'xong' trong plan chưa chứng minh được hệ thống chạy được, và trong chuyện này phần hook trên Windows vẫn chưa đo trong phiên thật.
**Bối cảnh:** Stop hook của phiên yêu cầu làm tới khi hoàn tất. Plan đã đánh dấu 45/45 việc.
**Chuyện gì xảy ra:** Ba lần stop hook bắt agent làm tiếp: đẩy lên main, chạy CI thật trên 9 tổ hợp, rồi cắt v0.1.0. Release chạy xanh từ đầu đến cuối trong một lần, và lệnh cài một dòng trong README chạy được với bản vừa phát hành.
**Bài học:** Plan xong khác release xong. Chỉ đóng việc khi lệnh cài thật chạy được từ nguồn công khai.
**Artefact:** Trang release trên GitHub và đầu ra lệnh cài trong HOME tạm. Che tên người dùng.
