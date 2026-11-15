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
angle: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent đang làm bộ cài đặt cho Windows. Test trên Linux đều xanh, nên người làm tin installer và uninstall đã chạy được. Reviewer độc lập đọc code theo hành vi của PowerShell và cmd.exe, và phát hiện uninstall không xoá được gì nhưng vẫn báo thành công. Ai làm CLI đa nền tảng nên quan tâm, vì test xanh trên một nền tảng không chứng minh được nền tảng khác."
audience: dev làm công cụ CLI đa nền tảng
spine_context: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent, đang làm bộ cài đặt và gỡ cài đặt cho Windows."
spine_context_lines: [profile, "claude:ab9a1dd8#L2017"]
spine_want: "Muốn cài đặt và gỡ cài đặt chạy đúng trên Windows, không chỉ trên Linux."
spine_want_lines: ["claude:ab9a1dd8#L2017"]
spine_obstacle: "Toàn bộ test trên Linux đều xanh (230 test), nhưng không bắt được lỗi quoting của PowerShell 5.1 và cmd.exe."
spine_obstacle_lines: ["claude:ab9a1dd8#L2026"]
spine_turn: "Tưởng test xanh nghĩa là installer và uninstall đã chạy được; hoá ra reviewer độc lập tìm ra installer báo Node quá cũ cho mọi người, và uninstall trên Windows không xoá được gì nhưng vẫn báo thành công."
spine_turn_lines: ["claude:ab9a1dd8#L2026"]
spine_action: "Sửa các lỗi nặng và trung bình trong phạm vi: tách thư mục cài khỏi cache, sửa cách truyền dấu nháy, rồi chạy lại test."
spine_action_lines: ["claude:ab9a1dd8#L2062"]
spine_outcome: "Test chạy lại đạt 230 qua, 0 lỗi; hai việc còn lại cần máy Windows thật và cần push tag."
spine_outcome_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2058"]
spine_takeaway: Test xanh trên một nền tảng không chứng minh được nền tảng khác; cần đọc code theo hành vi của từng shell.
spine_takeaway_lines: ["claude:ab9a1dd8#L2026"]
completeness: 7
---

# Reviewer độc lập: hai lỗi làm install và uninstall Windows hỏng

**Góc kể:** Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent đang làm bộ cài đặt cho Windows. Test trên Linux đều xanh, nên người làm tin installer và uninstall đã chạy được. Reviewer độc lập đọc code theo hành vi của PowerShell và cmd.exe, và phát hiện uninstall không xoá được gì nhưng vẫn báo thành công. Ai làm CLI đa nền tảng nên quan tâm, vì test xanh trên một nền tảng không chứng minh được nền tảng khác.
**Bối cảnh:** Toàn bộ 230 test và kiểm thử installer trên Linux đã xanh trước khi có review.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng: installer PowerShell 5.1 truyền sai dấu nháy vào `node -p`, khiến mọi lần cài báo 'Node quá cũ'; uninstall trên Windows gọi cmd.exe với nháy lồng nhau nên không xoá được gì nhưng vẫn báo thành công. Một lỗi nặng thứ ba suýt xoá cache của người dùng vì cache nằm trong thư mục cài.
**Bài học:** Test trên Linux không bắt được quoting của PowerShell 5.1 và cmd.exe. Cần một reviewer đọc code theo hành vi của từng nền tảng.
**Artefact:** File báo cáo review (các mục H1–H4). Không cần che.
