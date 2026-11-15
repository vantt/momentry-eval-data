---
id: 2026-11-03-reviewer-doc-lap-hai-loi-lam
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
hook: "Reviewer tìm ra uninstall Windows xoá không được gì nhưng báo thành công"
tension: cam_ma_van_lot
sides: ["Uninstall báo thành công", "Thực ra không xoá được gì, và installer báo Node quá cũ cho mọi người"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Agent tưởng đã xong: 230 test xanh và installer chạy trơn trên Linux. Reviewer độc lập đọc code theo hành vi Windows thì thấy cài trên Windows luôn báo 'Node quá cũ' dù máy có Node, còn gỡ cài báo thành công nhưng không xoá được file nào. Test chạy trên Linux không bắt được lỗi kiểu quoting này, nên ai viết công cụ đa nền tảng cần đọc code theo từng nền tảng."
audience: dev viết công cụ dòng lệnh có installer đa nền tảng
---

# Reviewer độc lập: hai lỗi làm install và uninstall Windows hỏng

**Góc kể:** Agent tưởng đã xong: 230 test xanh và installer chạy trơn trên Linux. Reviewer độc lập đọc code theo hành vi Windows thì thấy cài trên Windows luôn báo 'Node quá cũ' dù máy có Node, còn gỡ cài báo thành công nhưng không xoá được file nào. Test chạy trên Linux không bắt được lỗi kiểu quoting này, nên ai viết công cụ đa nền tảng cần đọc code theo từng nền tảng.
**Bối cảnh:** Toàn bộ 230 test và kiểm thử installer trên Linux đã xanh trước khi có review.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng: installer PowerShell 5.1 truyền sai dấu nháy vào `node -p`, khiến mọi lần cài báo 'Node quá cũ'; uninstall trên Windows gọi cmd.exe với nháy lồng nhau nên không xoá được gì nhưng vẫn báo thành công. Một lỗi nặng thứ ba suýt xoá cache của người dùng vì cache nằm trong thư mục cài.
**Bài học:** Test trên Linux không bắt được quoting của PowerShell 5.1 và cmd.exe. Cần một reviewer đọc code theo hành vi của từng nền tảng.
**Artefact:** File báo cáo review (các mục H1–H4). Không cần che.
