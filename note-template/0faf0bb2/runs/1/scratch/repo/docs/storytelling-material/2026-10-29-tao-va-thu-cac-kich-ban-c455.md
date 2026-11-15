---
id: 2026-10-29-tao-va-thu-cac-kich-ban-c455
code: M-KH05
aliases: [M-KH05]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L894", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L2134", "claude:0faf0bb2#L2138", "claude:0faf0bb2#L2885", "claude:0faf0bb2#L3430", "claude:0faf0bb2#L3471", "claude:0faf0bb2#L3474"]
hook: "Chép script vào repo để ai cũng chạy lại được, token không lộ"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tạo và thử các kịch bản bằng script nhỏ có sẵn, chép vào repo để người khác chạy lại, và giữ token không lộ qua dòng lệnh

**Chuyện gì xảy ra:** Tạo và thử các kịch bản bằng script nhỏ có sẵn, chép vào repo để người khác chạy lại, và giữ token không lộ qua dòng lệnh
**Góc người ngoài:** cách làm phổ biến là Gõ lệnh tay trong shell, token dán thẳng vào lệnh hoặc file, không ghi lại từng bước để làm lại; ở đây khác ở Token được đọc từ /proc hoặc file 0600 lúc chạy, script không chứa bí mật, và runbook được viết cùng lúc để người khác làm lại từng bước. Người đọc sẽ hỏi cách làm để có tài liệu tái lập mà không lộ khoá.
