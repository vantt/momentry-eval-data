---
id: 2026-10-29-hai-du-an-doc-lap-cung
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L641", "claude:0faf0bb2#L1798", "claude:0faf0bb2#L1804", "claude:0faf0bb2#L1810", "claude:0faf0bb2#L1814"]
hook: "Hai dự án không quen nhau cùng cấp mã task bằng một câu UPDATE"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai dự án độc lập cùng chọn UPDATE ... RETURNING để cấp mã task

**Bối cảnh:** Phân tích mã cấp số task (PAP-123, KAN-12) trong Paperclip và Kaneo để chọn cách làm cho fgOPC.
**Chuyện gì xảy ra:** Paperclip tăng issueCounter của công ty bằng một câu UPDATE ... RETURNING. Kaneo làm tương tự với last_task_number của project. Hai codebase không liên quan cùng giải bài toán trùng mã khi nhiều người ghi, nên bằng chứng cho bài học này được nâng lên mức mạnh nhất trong bảng xếp hạng.
**Bài học:** Khi hai codebase độc lập cùng một mẫu giải, đó là tín hiệu mạnh để chọn mẫu đó.
**Artefact:** Hai câu SQL rút gọn, đặt cạnh nhau.
