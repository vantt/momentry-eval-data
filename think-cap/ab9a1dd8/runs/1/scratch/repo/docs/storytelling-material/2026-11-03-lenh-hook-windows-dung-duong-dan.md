---
id: 2026-11-03-lenh-hook-windows-dung-duong-dan
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2820", "claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
hook: "Một file .cmd với đường dẫn gạch chéo chạy được ở cả hai shell Windows"
tension: it_ma_nhieu
sides: ["một đường dẫn gạch chéo tới momentry.cmd", "chạy được ở cả cmd lẫn Git Bash"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh hook Windows: dùng đường dẫn gạch chéo và file .cmd để chạy được ở cả cmd lẫn Git Bash

**Bối cảnh:** Theo các báo cáo cộng đồng, Claude Code chạy hook qua Git Bash còn Codex chạy qua cmd. Chưa ai kiểm trên một phiên thật.
**Chuyện gì xảy ra:** Agent chọn lệnh hook dạng đường dẫn có gạch chéo tới file momentry.cmd để chạy được ở cả hai shell. /bip gọi momentry theo tên vì installer đã thêm thư mục shim vào PATH. Tài liệu ghi rõ phần này chưa được đo trên phiên thật.
**Bài học:** Lệnh hook trên Windows nên dùng đường dẫn gạch chéo và một file .cmd để chạy được ở nhiều shell. Ghi rõ đây là suy luận từ báo cáo cộng đồng cho tới khi đo được.
**Artefact:** Đoạn cấu hình hook trong tài liệu cài đặt, che đường dẫn người dùng.
