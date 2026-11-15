---
id: 2026-11-02-o-dia-day-vi-worktree-cua-40f9
code: M-13S0
aliases: [M-13S0]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506", "claude:c4caee3c#L508", "claude:c4caee3c#L610", "claude:c4caee3c#L640", "claude:c4caee3c#L680", "claude:c4caee3c#L733", "claude:c4caee3c#L740"]
hook: "Đĩa đầy đến mức lệnh kiểm tra đĩa cũng lỗi"
tension: gap_ma_phai_chon
sides: ["Muốn kiểm tra xem đĩa đầy vì đâu", "Lệnh kiểm tra cũng lỗi vì hết hạn mức"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ổ đĩa đầy vì worktree của agent nằm trong /tmp

**Bối cảnh:** Nhiều agent chạy song song, mỗi agent có worktree riêng và mỗi worktree có node_modules khoảng 1,3 GB. Tất cả nằm trong /tmp, một tmpfs 16 GB có hạn mức.
**Chuyện gì xảy ra:** Khi hạn mức đầy, lệnh shell của mọi agent đều lỗi EDQUOT, và chính lệnh dùng để kiểm tra đĩa cũng lỗi. Agent dừng 11 tiến trình, chuyển nguyên worktree sang thư mục khác trên ổ chính, rồi chạy git worktree repair để nhận đường dẫn mới. Không mất thay đổi nào. Dung lượng /tmp sau đó chỉ còn 26%. Các agent được gọi lại bằng SendMessa ge và tiếp tục từ chỗ dừng.
**Bài học:** Đặt worktree, bản dựng và log lớn ngoài tmpfs ngay từ đầu, và ghi quy tắc này vào brief của mọi agent.
**Artefact:** Thông báo lỗi EDQUOT (không có nội dung nhạy cảm).
