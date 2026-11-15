---
id: 2026-11-03-reviewer-doc-lap-hai-loi-lam-d5ef
code: M-CBZJ
aliases: [M-CBZJ]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
hook: "Uninstall Windows báo thành công nhưng không xoá được gì"
tension: cam_ma_van_lot
sides: ["Reviewer độc lập tìm ra lỗi nặng trước khi phát hành", "Gỡ cài đặt báo thành công dù không xoá gì, và suýt xoá luôn cache người dùng"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer độc lập: hai lỗi làm install và uninstall Windows hỏng

**Bối cảnh:** Toàn bộ 230 test và kiểm thử installer trên Linux đã xanh trước khi có review.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng: installer PowerShell 5.1 truyền sai dấu nháy vào `node -p`, khiến mọi lần cài báo 'Node quá cũ'; uninstall trên Windows gọi cmd.exe với nháy lồng nhau nên không xoá được gì nhưng vẫn báo thành công. Một lỗi nặng thứ ba suýt xoá cache của người dùng vì cache nằm trong thư mục cài.
**Bài học:** Test trên Linux không bắt được quoting của PowerShell 5.1 và cmd.exe. Cần một reviewer đọc code theo hành vi của từng nền tảng.
**Artefact:** File báo cáo review (các mục H1–H4). Không cần che.
