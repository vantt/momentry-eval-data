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
hook: "Bot chỉ có quyền đọc, vì --no-verify bỏ qua mọi hook"
tension: cam_ma_van_lot
sides: ["hook pre-push chặn bot ghi vào main", "một cờ --no-verify là bỏ qua hết"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bot không có quyền ghi: git fetch thay vì push

**Bối cảnh:** Chủ hỏi tại sao bộ cài đặt của System Operator không được push lên git.
**Chuyện gì xảy ra:** Repo private của tài khoản cá nhân dùng gói Free không bảo vệ được main. Nếu bot có quyền ghi thì nó ghi được main, và hook pre-push bị bỏ qua bằng --no-verify. Phương án: bộ cài đặt vẫn được push bình thường bằng tài khoản chủ. System Operator chỉ có deploy key đọc, commit vào nhánh ops/ rồi chủ fetch về xem diff và merge. Chặn bằng quyền, không bằng lời dặn.
**Bài học:** Đừng dựa vào lời dặn để chặn agent push. Không cấp quyền ghi thì nó không thể ghi.
**Artefact:** Sơ đồ quyền: ai đọc, ai ghi, ai merge.
