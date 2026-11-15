---
id: 2026-11-03-lenh-co-dau-nhay-long-lam-d5ef
code: M-TCKE
aliases: [M-TCKE]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2026", "claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049"]
hook: "Cặp nháy đôi khiến installer Windows luôn báo Node quá cũ"
tension: nho_ma_to
sides: ["Máy có Node mới, cài đặt hợp lệ", "Dấu nháy đôi làm phiên bản thành 0, installer báo quá cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry đang đóng gói bộ cài đặt cho Windows và Linux, mục tiêu là installer chạy được trên cả hai. Trên Linux mọi test đã qua, nhưng người làm tưởng vậy là đủ. Reviewer đọc code độc lập tìm ra lệnh Node trong PowerShell bị hỏng dấu nháy, khiến installer Windows luôn báo Node quá cũ dù máy đã có Node mới. Dev đóng gói công cụ đa nền tảng nên cần biết test xanh không đảm bảo đường cài trên Windows."
audience: dev đóng gói CLI đa nền tảng
spine_context: "Dự án momentry đang đóng gói bộ cài đặt cho Windows và Linux, mục tiêu là installer chạy được trên cả hai."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Installer chạy được trên Windows, và gỡ cài đặt sạch."
spine_want_lines: ["claude:ab9a1dd8#L2017"]
spine_obstacle: "Chưa có máy Windows thật, nên phần Windows chỉ kiểm tra được bằng cách đọc code; test chạy trên Linux."
spine_obstacle_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_turn: "Tưởng test Linux xanh (230 qua) nghĩa là installer ổn; hoá ra lệnh node -p có dấu nháy đôi bị PowerShell 5.1 làm hỏng, phiên bản đọc thành 0 và installer luôn báo Node quá cũ."
spine_turn_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
spine_action: "Sửa lỗi theo nhóm, bắt đầu từ các lỗi nặng ở nhánh Windows (H2, H3, H4) và vài lỗi trung bình, nhẹ, rồi chạy lại test."
spine_action_lines: ["claude:ab9a1dd8#L2039", "claude:ab9a1dd8#L2049", "claude:ab9a1dd8#L2062"]
spine_outcome: "230/230 test qua, 0 lỗi; H1 và các lỗi còn lại chờ máy Windows thật để xác nhận."
spine_outcome_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2058", "claude:ab9a1dd8#L2062"]
spine_takeaway: "Test xanh trên Linux không đủ cho đường cài trên Windows; cần chạy thật trên Windows, vì reviewer đọc code có thể bắt được lỗi mà test không thấy."
spine_takeaway_lines: ["claude:ab9a1dd8#L2017", "claude:ab9a1dd8#L2026"]
completeness: 7
---

# Lệnh có dấu nháy lồng làm installer Windows luôn báo Node quá cũ

**Góc kể:** Dự án momentry đang đóng gói bộ cài đặt cho Windows và Linux, mục tiêu là installer chạy được trên cả hai. Trên Linux mọi test đã qua, nhưng người làm tưởng vậy là đủ. Reviewer đọc code độc lập tìm ra lệnh Node trong PowerShell bị hỏng dấu nháy, khiến installer Windows luôn báo Node quá cũ dù máy đã có Node mới. Dev đóng gói công cụ đa nền tảng nên cần biết test xanh không đảm bảo đường cài trên Windows.
**Bối cảnh:** Một reviewer subagent đọc code độc lập, không chạy được Windows, trong khi toàn bộ test trên Linux đã qua.
**Chuyện gì xảy ra:** Reviewer tìm 4 lỗi nặng, 5 lỗi trung bình và 7 lỗi nhẹ. Lỗi nặng nhất: dấu nháy đôi bên trong lệnh node -p bị PowerShell 5.1 truyền thô, Node đọc thành cú pháp lỗi và phiên bản thành 0, nên installer luôn báo Node quá cũ. Một lỗi khác khiến uninstall trên Windows không xoá gì nhưng vẫn báo thành công. Agent sửa cả bốn lỗi nặng và năm lỗi trung bình trong một lượt.
**Bài học:** Dấu nháy lồng trong PowerShell 5.1 là bẫy; reviewer độc lập đọc code tìm được điều test Linux không thấy, nhưng vẫn cần chạy thật trên Windows để xác nhận.
**Artefact:** Dòng lệnh trước và sau khi sửa.
