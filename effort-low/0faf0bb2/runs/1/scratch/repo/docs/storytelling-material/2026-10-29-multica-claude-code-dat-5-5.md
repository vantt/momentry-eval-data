---
id: 2026-10-29-multica-claude-code-dat-5-5
date: 2026-10-29
repo: repo
status: raw
signals: [artefact nhìn được, người duyệt là máy, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3540", "claude:0faf0bb2#L3556", "claude:0faf0bb2#L3672", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3707", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3747"]
hook: "Agent bị trả lại hai lần, rồi dừng hỏi chủ thay vì bịa giá"
tension: tuong_ma_hoa_ra
sides: ["ai cũng nghĩ agent sẽ tự bịa số liệu cho xong việc", "Mai dừng lại hỏi chủ, chủ trả lời giá 350.000đ, và không agent nào tự đóng task"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica + Claude Code đạt 5/5 tiêu chí: agent tự giao việc, bị trả lại, hỏi chủ rồi duyệt

**Bối cảnh:** Spike B' thay OpenClaw bằng Claude Code làm runtime. Hai agent Mai (viết) và Long (duyệt) làm việc trên workflow cột Nháp → Sales review → In review → Done.
**Chuyện gì xảy ra:** Issue được tạo không chỉ định người, tự giao cho Mai rồi Long. Long trả lại hai lần vì thiếu giá. Mai dừng lại và hỏi chủ thay vì tự bịa số liệu bán hàng. Chủ comment giá 350.000đ, Long duyệt, issue lên in_review giao cho chủ. Không agent nào tự chuyển done. Thời gian ghi ngược là 16 giây.
**Bài học:** Để agent dừng và hỏi người khi thiếu dữ kiện là hành vi đáng ghi nhận; chặn tự done thì hiện chỉ nằm trong chỉ dẫn, server chưa ép.
**Artefact:** Board 4 cột với SEN-2 ở in_review giao cho Owner, và chuỗi comment Long trả lại → Mai hỏi chủ. Che: email, token, id.
