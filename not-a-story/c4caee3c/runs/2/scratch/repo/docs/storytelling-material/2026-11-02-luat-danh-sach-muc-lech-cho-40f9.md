---
id: 2026-11-02-luat-danh-sach-muc-lech-cho-40f9
code: M-T6E3
aliases: [M-T6E3]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3912", "claude:c4caee3c#L3913", "claude:c4caee3c#L3919", "claude:c4caee3c#L3930"]
hook: "Luật mức lệch cũ lỗi thời: chỉ chặn khi tụt quá 0,01"
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

# Luật danh sách mức lệch cho phép lỗi thời, đổi thành chỉ chặn khi tụt

**Bối cảnh:** Danh sách mức lệch chấp nhận được đo trên gói vi cũ. Khi gói vi đổi, vi-snippet lệch +0,024 và không nằm trong danh sách.
**Chuyện gì xảy ra:** Lead hỏi người dùng và được chọn quy tắc chỉ chặn khi tụt quá 0,01, cải thiện thì luôn qua, và cho vi-synonym tụt tới 0,03. Quy tắc này không cần duyệt lại mỗi lần gói vi thay đổi.
**Bài học:** Ngưỡng dạng 'cho phép một mức lệch cụ thể' sẽ cũ theo từng bản. Đặt luật theo chiều, chỉ chặn khi xấu đi.
