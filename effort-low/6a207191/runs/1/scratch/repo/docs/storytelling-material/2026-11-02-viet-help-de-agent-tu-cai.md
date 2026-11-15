---
id: 2026-11-02-viet-help-de-agent-tu-cai
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L551", "claude:6a207191#L604", "claude:6a207191#L636", "claude:6a207191#L639", "claude:6a207191#L640", "claude:6a207191#L657", "claude:6a207191#L766"]
hook: "Viết --help sao cho agent chưa đọc README vẫn cài xong"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Viết --help để agent tự cài: tiêu chí 'không đọc README vẫn xong'

**Bối cảnh:** User muốn chỉ cần nói 'cài X giúp tôi' là agent tự làm được, chỉ dựa vào --help.
**Chuyện gì xảy ra:** Agent thêm các rule CMD-13 đến CMD-19: help của init, doctor, update và uninstall phải tự đủ dùng, không hỏi đáp khi thiếu terminal, mỗi kết quả có dòng Next, JSON theo một khuôn chung. Tiêu chí kiểm là một agent mới không đọc README vẫn cài xong. Điểm đầu tiên chạm người dùng cũng được ghi thành một file riêng.
**Bài học:** Hãy biến 'dễ dùng' thành tiêu chí đo được. 'Agent không đọc README vẫn xong' là một kiểm tra rõ ràng.
**Artefact:** Bảng 12 bước Verify trong SKILL.md.
