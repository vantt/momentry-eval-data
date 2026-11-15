---
id: 2026-11-03-reviewer-agent-tim-16-loi-install-d5ef
code: M-64WM
aliases: [M-64WM]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2058"]
hook: "Install Windows luôn báo Node quá cũ, uninstall không xoá gì vẫn báo xong"
tension: tuong_ma_hoa_ra
sides: ["Test Linux xanh, tưởng installer ổn", "Reviewer tìm 16 lỗi, hai lỗi nặng hỏng trên Windows"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang đóng gói bản cài đặt cho cả Windows lẫn Linux. Khi test Linux đã xanh 230/230, người làm tưởng installer đã ổn. Reviewer độc lập đọc lại và tìm ra hai lỗi nặng làm cài đặt và gỡ cài đặt hỏng trên Windows, trong khi test Linux không bắt được. Ai làm công cụ đa nền tảng nên nghe vì test xanh trên một hệ điều hành không chứng minh gì cho hệ khác."
audience: dev làm công cụ dòng lệnh đa nền tảng và viết test cho installer
spine_context: Momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent; người làm đang đóng gói bản cài đặt cho Windows và Linux.
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: Hoàn tất gói cài đặt theo plan packaging-distribution.
spine_want_lines: ["claude:ab9a1dd8#L664"]
spine_obstacle: "Test Linux xanh, nhưng lỗi nặng chỉ lộ khi đọc code cho Windows; máy Windows thật chưa có để chạy thử."
spine_obstacle_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_turn: Tưởng installer đã ổn vì test Linux xanh; hoá ra hai lỗi nặng làm cài đặt và gỡ cài đặt hỏng trên Windows.
spine_turn_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_action: "Nhờ reviewer độc lập đọc installer, gỡ cài đặt và cập nhật, rồi sửa các lỗi nặng và trung bình."
spine_action_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2039"]
spine_outcome: "Test chạy lại đạt 230/230; đã sửa H2, H3, H4, M3, L3 và L5."
spine_outcome_lines: ["claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
spine_takeaway: Test trên một hệ điều hành không thay được đường chạy riêng theo nền tảng; người review cần hiểu shell cụ thể.
spine_takeaway_lines: ["claude:ab9a1dd8#L2026"]
completeness: 7
---

# Reviewer agent tìm 16 lỗi: install Windows luôn báo 'Node quá cũ', uninstall không xoá gì nhưng vẫn báo thành công

**Góc kể:** Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang đóng gói bản cài đặt cho cả Windows lẫn Linux. Khi test Linux đã xanh 230/230, người làm tưởng installer đã ổn. Reviewer độc lập đọc lại và tìm ra hai lỗi nặng làm cài đặt và gỡ cài đặt hỏng trên Windows, trong khi test Linux không bắt được. Ai làm công cụ đa nền tảng nên nghe vì test xanh trên một hệ điều hành không chứng minh gì cho hệ khác.
**Bối cảnh:** Code và test đã xanh trên Linux. Một agent review độc lập được gọi đọc installer, uninstall và update.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng làm install và uninstall hỏng trên Windows. PowerShell 5.1 làm mất dấu nháy trong lệnh node -p, nên version đọc ra 0 và installer luôn báo quá cũ. cmd.exe không hiểu dấu nháy kiểu Node nên lệnh xoá trễ thất bại mà vẫn báo thành công. Một lỗi khác có thể xoá cả cache trên Windows. Test Linux không bắt được những lỗi này.
**Bài học:** Đường chạy riêng theo nền tảng cần người đọc có hiểu biết về shell cụ thể. Test trên Linux không thay thế được.
**Artefact:** Dòng code PowerShell trước và sau khi sửa dấu nháy. Không có dữ liệu nhạy cảm.
