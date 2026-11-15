---
id: 2026-11-02-nguoi-dung-don-dep-theo-tung-40f9
code: M-SKAE
aliases: [M-SKAE]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:c4caee3c#L3942", "claude:c4caee3c#L3947", "claude:c4caee3c#L3966", "claude:c4caee3c#L3997"]
hook: "Dọn từng phần ngay khi xong, không đợi đầy đĩa mới xoá bừa"
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

# Người dùng dọn dẹp theo từng phần: xoá ngay những gì đã xong (worktree đã merge, nhánh nháp, log, dữ liệu tạm) và giữ lại đúng những gì agent còn đang dùng, rồi ghi rõ đã xoá gì.

**Chuyện gì xảy ra:** Người dùng dọn dẹp theo từng phần: xoá ngay những gì đã xong (worktree đã merge, nhánh nháp, log, dữ liệu tạm) và giữ lại đúng những gì agent còn đang dùng, rồi ghi rõ đã xoá gì.
**Góc người ngoài:** cách làm phổ biến là Thường người dùng để rác tích tụ đến khi đầy đĩa mới dọn một lần, hoặc xoá bừa; ở đây khác ở Lệnh 'cái gì xong thì dọn cho gọn' được thực hiện có chọn lọc, dung lượng giảm từ 21G còn 6,4G mà không đụng tới việc đang chạy. Người đọc sẽ muốn biết cách làm việc đó an toàn.
