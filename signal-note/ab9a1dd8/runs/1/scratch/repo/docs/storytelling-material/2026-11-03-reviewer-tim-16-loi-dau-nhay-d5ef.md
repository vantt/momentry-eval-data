---
id: 2026-11-03-reviewer-tim-16-loi-dau-nhay-d5ef
code: M-1B4N
aliases: [M-1B4N]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2058"]
hook: "Dấu nháy kép làm bản cài Windows luôn báo Node quá cũ"
tension: nho_ma_to
sides: ["Một cặp dấu nháy kép trong lệnh kiểm phiên bản", "PowerShell đọc phiên bản thành 0, cài đặt luôn từ chối"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang đóng gói bản cài cho Windows. Trước khi có reviewer, phần này được báo là đã xong vì test trên Linux đều qua. Reviewer đọc code mà không chạy Windows thì thấy lệnh kiểm phiên bản Node dùng dấu nháy kép, PowerShell làm hỏng, khiến installer luôn báo Node quá cũ. Ai viết code chạy trên nhiều hệ điều hành cần đọc theo từng nền tảng, vì test xanh trên một máy không chứng minh máy khác chạy được."
audience: dev viết installer hoặc code chạy trên nhiều hệ điều hành
spine_context: "momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang đóng gói bản cài cho Windows theo plan packaging-distribution."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Hoàn tất plan đóng gói và phân phối, rồi nhờ reviewer độc lập đọc lại."
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2017"]
spine_obstacle: "Không có máy Windows thật, nên hai việc còn lại chưa làm được."
spine_obstacle_lines: ["claude:ab9a1dd8#L2017"]
spine_turn: "Tưởng phần Windows đã xong vì test trên Linux đều qua; hoá ra lệnh kiểm phiên bản Node dùng dấu nháy kép bị PowerShell làm hỏng, nên installer luôn báo Node quá cũ."
spine_turn_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2058"]
spine_action: "Sửa các lỗi reviewer báo, bắt đầu từ lỗi nặng H2 và H3, rồi đến các lỗi trung bình và nhẹ."
spine_action_lines: ["claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2062"]
spine_outcome: "Test vẫn 230 qua, 0 lỗi sau các sửa đã ghi; trích đoạn chưa cho thấy H1 đã sửa và chưa có kết quả chạy trên Windows."
spine_outcome_lines: ["claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
spine_takeaway: Code đa nền tảng cần đọc theo từng nền tảng; test xanh trên một máy không chứng minh máy khác chạy được.
spine_takeaway_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
completeness: 7
---

# Reviewer tìm 16 lỗi: dấu nháy kép trong PowerShell làm bản cài Windows luôn báo Node quá cũ

**Góc kể:** momentry là công cụ đọc transcript các phiên làm việc với coding agent, và người làm đang đóng gói bản cài cho Windows. Trước khi có reviewer, phần này được báo là đã xong vì test trên Linux đều qua. Reviewer đọc code mà không chạy Windows thì thấy lệnh kiểm phiên bản Node dùng dấu nháy kép, PowerShell làm hỏng, khiến installer luôn báo Node quá cũ. Ai viết code chạy trên nhiều hệ điều hành cần đọc theo từng nền tảng, vì test xanh trên một máy không chứng minh máy khác chạy được.
**Bối cảnh:** Sau khi viết installer và uninstall cho ba hệ điều hành, một reviewer độc lập đọc code, không chạy trên Windows.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 trung bình và 7 nhẹ. Lỗi H1: node -p với dấu nháy kép làm PowerShell 5.1 truyền hỏng, Node đọc phiên bản thành 0, installer luôn báo Node quá cũ. Lỗi H2: uninstall gọi cmd với escape sai nên không xoá gì nhưng vẫn báo thành công. Lỗi H3: trên Windows cache nằm trong thư mục cài, nên gỡ thường có thể xoá dữ liệu đáng giữ.
**Bài học:** Code đa nền tảng cần đọc theo từng nền tảng. Máy Linux không bắt được các lỗi này; CI Windows là lưới cuối.
**Artefact:** Trích ba dòng H1, H2, H3 của báo cáo review (che đường dẫn).
