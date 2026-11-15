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
angle: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang làm gói cài đặt cho Windows và Linux. Toàn bộ 230 test trên Linux đều xanh, nên người làm tin installer và uninstall trên Windows cũng ổn. Reviewer độc lập đọc code theo hành vi của PowerShell 5.1 và cmd.exe thì thấy installer Windows luôn báo 'Node quá cũ', còn uninstall báo thành công dù không xoá được gì. Test trên Linux không bắt được loại lỗi quoting này, nên ai viết installer đa nền tảng cần đọc code theo từng shell thật."
audience: dev viết installer hoặc script đa nền tảng
spine_context: "Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang làm gói cài đặt cho Windows và Linux."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: Muốn installer và uninstall chạy đúng trên Windows trước khi phát hành.
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2017"]
spine_obstacle: "Test trên Linux không bắt được lỗi quoting của PowerShell 5.1 và cmd.exe, nên lỗi Windows không lộ ra."
spine_obstacle_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_turn: "Tưởng installer và uninstall trên Windows đã ổn vì test Linux xanh; hoá ra installer báo 'Node quá cũ' cho mọi người, còn uninstall báo thành công nhưng không xoá được gì."
spine_turn_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_action: "Bắt đầu sửa từ các lỗi nặng, đã xong H2, H3, H4 và vài lỗi vừa, nhẹ, rồi chạy lại test."
spine_action_lines: ["claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2062"]
spine_outcome: "Sau khi sửa, 230/230 test vẫn qua; lỗi Windows chưa chạy thật, cần CI Windows xác nhận H1 và H2."
spine_outcome_lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2058"]
spine_takeaway: Test trên Linux không đủ cho installer đa nền tảng; cần đọc code theo hành vi từng shell hoặc chạy CI trên Windows thật.
spine_takeaway_lines: ["claude:ab9a1dd8#L2026"]
completeness: 7
---

# Reviewer độc lập: hai lỗi làm install và uninstall Windows hỏng

**Góc kể:** Một công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent đang làm gói cài đặt cho Windows và Linux. Toàn bộ 230 test trên Linux đều xanh, nên người làm tin installer và uninstall trên Windows cũng ổn. Reviewer độc lập đọc code theo hành vi của PowerShell 5.1 và cmd.exe thì thấy installer Windows luôn báo 'Node quá cũ', còn uninstall báo thành công dù không xoá được gì. Test trên Linux không bắt được loại lỗi quoting này, nên ai viết installer đa nền tảng cần đọc code theo từng shell thật.
**Bối cảnh:** Toàn bộ 230 test và kiểm thử installer trên Linux đã xanh trước khi có review.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng: installer PowerShell 5.1 truyền sai dấu nháy vào `node -p`, khiến mọi lần cài báo 'Node quá cũ'; uninstall trên Windows gọi cmd.exe với nháy lồng nhau nên không xoá được gì nhưng vẫn báo thành công. Một lỗi nặng thứ ba suýt xoá cache của người dùng vì cache nằm trong thư mục cài.
**Bài học:** Test trên Linux không bắt được quoting của PowerShell 5.1 và cmd.exe. Cần một reviewer đọc code theo hành vi của từng nền tảng.
**Artefact:** File báo cáo review (các mục H1–H4). Không cần che.
