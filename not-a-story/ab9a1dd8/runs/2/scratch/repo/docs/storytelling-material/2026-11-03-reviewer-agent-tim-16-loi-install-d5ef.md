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
hook: "Reviewer tìm 16 lỗi: gỡ cài Windows báo thành công mà không xoá gì"
tension: cam_ma_van_lot
sides: ["Test Linux đều qua", "Windows luôn báo Node quá cũ, uninstall không xoá gì vẫn báo thành công"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry đang làm bộ cài đặt và gỡ cài cho người dùng, và phần việc này gần xong. Người làm tin code ổn vì 230 test trên Linux đều qua. Nhưng một reviewer độc lập đọc code và thấy trên Windows, installer luôn báo Node quá cũ, còn gỡ cài không xoá gì mà vẫn báo thành công. Ai build công cụ chạy trên nhiều hệ điều hành nên quan tâm: test xanh trên máy mình chưa chắc chạy trên máy người dùng."
audience: dev build công cụ chạy trên nhiều hệ điều hành
spine_context: "Dự án momentry đang làm bộ cài đặt và gỡ cài cho người dùng, theo kế hoạch đóng gói và phát hành."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: Hoàn tất gói phát hành đến khi mọi việc trong kế hoạch xong.
spine_want_lines: ["claude:ab9a1dd8#L664"]
spine_obstacle: "Test trên Linux đều qua, nhưng hai việc còn lại cần máy Windows thật và cần push tag."
spine_obstacle_lines: ["claude:ab9a1dd8#L2017"]
spine_turn: "Tưởng code ổn vì 230 test trên Linux đều qua; hoá ra trên Windows, installer luôn báo Node quá cũ, còn gỡ cài không xoá gì nhưng vẫn báo thành công."
spine_turn_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_action: "Reviewer độc lập đọc code, tìm 4 lỗi nặng, 5 trung bình, 7 nhẹ; người làm sửa hết trong phạm vi, bắt đầu từ lỗi nặng."
spine_action_lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039"]
spine_outcome: "Sau khi sửa, 230 test Linux vẫn qua, 0 lỗi; các lỗi Windows chưa được chạy thử trên Windows thật."
spine_outcome_lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2058"]
spine_takeaway: Test trên một nền tảng không thay thế được việc chạy đường riêng theo nền tảng; cần người đọc hiểu shell cụ thể hoặc chạy trên máy thật.
spine_takeaway_lines: ["claude:ab9a1dd8#L2026"]
completeness: 7
---

# Reviewer agent tìm 16 lỗi: install Windows luôn báo 'Node quá cũ', uninstall không xoá gì nhưng vẫn báo thành công

**Góc kể:** Dự án momentry đang làm bộ cài đặt và gỡ cài cho người dùng, và phần việc này gần xong. Người làm tin code ổn vì 230 test trên Linux đều qua. Nhưng một reviewer độc lập đọc code và thấy trên Windows, installer luôn báo Node quá cũ, còn gỡ cài không xoá gì mà vẫn báo thành công. Ai build công cụ chạy trên nhiều hệ điều hành nên quan tâm: test xanh trên máy mình chưa chắc chạy trên máy người dùng.
**Bối cảnh:** Code và test đã xanh trên Linux. Một agent review độc lập được gọi đọc installer, uninstall và update.
**Chuyện gì xảy ra:** Reviewer báo 4 lỗi nặng, 5 trung bình, 7 nhẹ. Hai lỗi nặng làm install và uninstall hỏng trên Windows. PowerShell 5.1 làm mất dấu nháy trong lệnh node -p, nên version đọc ra 0 và installer luôn báo quá cũ. cmd.exe không hiểu dấu nháy kiểu Node nên lệnh xoá trễ thất bại mà vẫn báo thành công. Một lỗi khác có thể xoá cả cache trên Windows. Test Linux không bắt được những lỗi này.
**Bài học:** Đường chạy riêng theo nền tảng cần người đọc có hiểu biết về shell cụ thể. Test trên Linux không thay thế được.
**Artefact:** Dòng code PowerShell trước và sau khi sửa dấu nháy. Không có dữ liệu nhạy cảm.
