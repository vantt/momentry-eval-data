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
hook: "Bot có quyền ghi thì --no-verify vượt hết hook, nên chỉ cho đọc"
tension: cam_ma_van_lot
sides: ["Hook pre-push chặn push xấu lên main", "Bot có quyền ghi chỉ cần --no-verify là qua"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng một agent vận hành chạy trên máy chủ, và muốn đưa bộ cài đặt của nó lên git để chạy đúng phiên bản đã duyệt. Ban đầu cách tự nhiên là cho bot push thẳng, dựa vào hook pre-push để chặn push xấu. Hoá ra repo private gói Free không khoá được nhánh main, và bot có quyền ghi thì chỉ cần --no-verify là vượt hook. Ai cho agent quyền git nên biết: chặn bằng quyền truy cập, không bằng lời dặn hay hook."
audience: dev dùng agent có quyền truy cập git
spine_context: "Người làm đang dựng một System Operator, một agent vận hành chạy trên máy chủ, và chuẩn bị đưa bộ cài đặt của nó lên git."
spine_context_lines: ["claude:f0bf048d#L3320"]
spine_want: Muốn bộ cài đặt được push lên git để System Operator chạy theo đúng phiên bản đã duyệt.
spine_want_lines: ["claude:f0bf048d#L3324", "claude:f0bf048d#L3333"]
spine_obstacle: "Repo private trên gói GitHub Free không khoá được nhánh main, và bot có quyền ghi thì vượt được hook pre-push bằng --no-verify."
spine_obstacle_lines: ["claude:f0bf048d#L3327"]
spine_turn: "Tưởng cho bot push thẳng là ổn vì hook pre-push sẽ chặn push xấu; hoá ra bot có quyền ghi thì bỏ qua được hook, nên quyền ghi chính là chỗ cần chặn."
spine_turn_lines: ["claude:f0bf048d#L3324", "claude:f0bf048d#L3327"]
spine_action: "Bỏ phương án bot push. System Operator chỉ có deploy key đọc, commit vào nhánh ops/ rồi người làm fetch về xem diff và merge."
spine_action_lines: ["claude:f0bf048d#L3340"]
spine_outcome: "Người làm duyệt làm 2.1 và 2.2; bước đầu mới là kiểm tra trạng thái hệ thống, chưa có kết quả triển khai."
spine_outcome_lines: ["claude:f0bf048d#L3345", "claude:f0bf048d#L3352"]
spine_takeaway: Đừng dựa vào lời dặn hay hook để chặn agent ghi vào repo; không cấp quyền ghi thì nó không ghi được.
spine_takeaway_lines: ["claude:f0bf048d#L3340"]
completeness: 7
---

# Bot không có quyền ghi: git fetch thay vì push

**Góc kể:** Người làm đang dựng một agent vận hành chạy trên máy chủ, và muốn đưa bộ cài đặt của nó lên git để chạy đúng phiên bản đã duyệt. Ban đầu cách tự nhiên là cho bot push thẳng, dựa vào hook pre-push để chặn push xấu. Hoá ra repo private gói Free không khoá được nhánh main, và bot có quyền ghi thì chỉ cần --no-verify là vượt hook. Ai cho agent quyền git nên biết: chặn bằng quyền truy cập, không bằng lời dặn hay hook.
**Bối cảnh:** Chủ hỏi tại sao bộ cài đặt của System Operator không được push lên git.
**Chuyện gì xảy ra:** Repo private của tài khoản cá nhân dùng gói Free không bảo vệ được main. Nếu bot có quyền ghi thì nó ghi được main, và hook pre-push bị bỏ qua bằng --no-verify. Phương án: bộ cài đặt vẫn được push bình thường bằng tài khoản chủ. System Operator chỉ có deploy key đọc, commit vào nhánh ops/ rồi chủ fetch về xem diff và merge. Chặn bằng quyền, không bằng lời dặn.
**Bài học:** Đừng dựa vào lời dặn để chặn agent push. Không cấp quyền ghi thì nó không thể ghi.
**Artefact:** Sơ đồ quyền: ai đọc, ai ghi, ai merge.
