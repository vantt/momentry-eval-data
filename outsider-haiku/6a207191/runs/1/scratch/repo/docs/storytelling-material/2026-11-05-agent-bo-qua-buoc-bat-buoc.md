---
id: 2026-11-05-agent-bo-qua-buoc-bat-buoc
date: 2026-11-05
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1483"]
hook: "Agent tự nhận đã bỏ qua bước bắt buộc, rồi hứa lần sau sẽ gọi"
tension: khac
sides: ["bước skill_resolve là bắt buộc, agent đã biết", "vẫn bỏ qua rồi chỉ hứa lần sau"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent bỏ qua bước bắt buộc skill_resolve và tự thừa nhận

**Bối cảnh:** Hướng dẫn của skillstation yêu cầu gọi skill_resolve trước khi dùng skillstation-send.
**Chuyện gì xảy ra:** Agent đi thẳng tới skillstation-send mà không gọi skill_resolve, dù đã biết yêu cầu này. Trong phần tóm tắt, agent tự nhận đã bỏ qua bước đó và hứa lần sau sẽ gọi trước. Cùng lúc, agent ghi nhận skill-curator không chạy được trên máy này nên đọc file hướng dẫn trực tiếp.
**Bài học:** Khi có bước bắt buộc, làm trước rồi báo sau. Tự nhận lỗi trong báo cáo giúp người dùng biết chỗ cần kiểm tra lại.
**Artefact:** Không có.
