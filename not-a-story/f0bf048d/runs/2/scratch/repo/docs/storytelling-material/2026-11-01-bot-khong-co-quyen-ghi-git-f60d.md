---
id: 2026-11-01-bot-khong-co-quyen-ghi-git-f60d
code: M-G41F
aliases: [M-G41F]
date: 2026-11-01
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3327", "claude:f0bf048d#L3333", "claude:f0bf048d#L3340"]
hook: "Repo Free không chặn nổi bot: chặn bằng quyền, không bằng lời dặn"
tension: cam_ma_van_lot
sides: ["Hook pre-push chặn bot ghi vào main", "Bot bỏ qua bằng --no-verify nên chỉ còn cách bỏ quyền ghi"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Người làm đang dựng một System Operator chạy bằng agent trên máy riêng, theo kế hoạch Giai đoạn 2 tách quyền."
spine_context_lines: ["claude:f0bf048d#L3320"]
spine_want: System Operator không ghi được vào nhánh main và không leo lên root được.
spine_want_lines: ["claude:f0bf048d#L3320"]
spine_obstacle: "Repo private gói Free không bảo vệ được main, và hook pre-push bỏ qua được bằng --no-verify."
spine_obstacle_lines: ["claude:f0bf048d#L3327"]
spine_action: "Viết kế hoạch chi tiết trong file plan, chưa chạy gì trên máy. Agent chỉ có deploy key đọc, commit vào nhánh ops/ rồi người làm fetch về xem diff và merge."
spine_action_lines: ["claude:f0bf048d#L3320", "claude:f0bf048d#L3340"]
spine_takeaway: "Giới hạn bằng cơ chế (quyền), không bằng lời dặn, vì agent bị điều khiển có thể phớt lờ lời dặn."
spine_takeaway_lines: ["claude:f0bf048d#L3340"]
completeness: 5
---

# Bot không có quyền ghi: git fetch thay vì push

**Bối cảnh:** Chủ hỏi tại sao bộ cài đặt của System Operator không được push lên git.
**Chuyện gì xảy ra:** Repo private của tài khoản cá nhân dùng gói Free không bảo vệ được main. Nếu bot có quyền ghi thì nó ghi được main, và hook pre-push bị bỏ qua bằng --no-verify. Phương án: bộ cài đặt vẫn được push bình thường bằng tài khoản chủ. System Operator chỉ có deploy key đọc, commit vào nhánh ops/ rồi chủ fetch về xem diff và merge. Chặn bằng quyền, không bằng lời dặn.
**Bài học:** Đừng dựa vào lời dặn để chặn agent push. Không cấp quyền ghi thì nó không thể ghi.
**Artefact:** Sơ đồ quyền: ai đọc, ai ghi, ai merge.
