---
id: 2026-11-02-verify-khong-can-script-12-buoc-c4b4
code: M-WA9H
aliases: [M-WA9H]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L900", "claude:6a207191#L910", "claude:6a207191#L922", "claude:6a207191#L951"]
hook: "12 bước viết bằng chữ thay cho script, lint vẫn qua 212 quy tắc"
tension: it_ma_nhieu
sides: ["Không viết thêm dòng code nào để bảo trì", "Vẫn kiểm tra đủ 12 bước, chỉ 2 bước cần phán đoán"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Một skill packaging-distribution dùng cho các dự án CLI của người làm, đang chuẩn hoá cách cài đặt, cập nhật và kiểm tra."
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L701"]
spine_want: Skill tự kiểm tra được việc hiện tại mà không thêm code phải bảo trì.
spine_want_lines: ["claude:6a207191#L900"]
spine_action: Thêm bước Verify 12 điểm vào SKILL.md thay vì viết script kiểm tra.
spine_action_lines: ["claude:6a207191#L934", "claude:6a207191#L951"]
spine_outcome: Script kiểm tra cấu trúc vẫn chạy qua với 212 rule; SKILL.md còn 1044 từ.
spine_outcome_lines: ["claude:6a207191#L945"]
spine_takeaway: "Trước khi viết script kiểm tra, xem danh sách lệnh trong văn bản đã đủ chưa; script chỉ đáng viết khi muốn khoá vào CI."
spine_takeaway_lines: ["claude:6a207191#L929"]
completeness: 5
---

# Verify không cần script: 12 bước trong SKILL.md thay vì code phải bảo trì

**Bối cảnh:** Chủ dự án hỏi skill có nên tự verify việc hiện tại không. Agent đề xuất script audit, rồi nhận ra script là thêm code phải bảo trì và đi ngược mục tiêu skill gọn.
**Chuyện gì xảy ra:** Agent đề xuất 12 bước verify ngắn trong SKILL.md, chạy trong HOME tạm để không đụng cấu hình thật. Chỉ 2 bước cần phán đoán là đầu README và agent-native test. Chủ dự án đồng ý. Sau thay đổi, lint vẫn qua 212 quy tắc và SKILL.md còn 1044 từ.
**Bài học:** Khi đang muốn viết script kiểm tra, hỏi trước xem danh sách lệnh trong văn bản đã đủ chưa. Script chỉ đáng viết khi muốn khoá vào CI.
**Artefact:** Bảng 12 bước verify. Không có thông tin cần che.
