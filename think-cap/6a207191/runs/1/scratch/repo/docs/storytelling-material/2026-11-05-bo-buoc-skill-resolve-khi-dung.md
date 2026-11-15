---
id: 2026-11-05-bo-buoc-skill-resolve-khi-dung
date: 2026-11-05
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1483"]
hook: "Agent bỏ bước skill_resolve, kết quả vẫn đúng như dự đoán"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bỏ bước skill_resolve khi dùng skill gửi: kết quả giống nhau nhưng quy trình bị bỏ

**Bối cảnh:** Quy trình của hub yêu cầu gọi skill_resolve trước để hub chọn skill phù hợp cho việc gửi skill.
**Chuyện gì xảy ra:** Agent đi thẳng tới skillstation-send mà không gọi skill_resolve. Kết quả trùng với dự đoán nên không ảnh hưởng gì, nhưng agent tự thừa nhận đã bỏ qua bước này và hứa lần sau gọi trước.
**Bài học:** Làm đúng thứ tự quy trình ngay cả khi kết quả có vẻ hiển nhiên. Kết quả đúng không xoá được bước bị bỏ.
**Artefact:** Không có.
