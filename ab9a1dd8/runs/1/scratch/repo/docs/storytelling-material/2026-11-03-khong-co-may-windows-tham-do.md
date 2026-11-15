---
id: 2026-11-03-khong-co-may-windows-tham-do
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, artefact]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2845", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3053", "claude:ab9a1dd8#L3074", "claude:ab9a1dd8#L3091", "claude:ab9a1dd8#L3239"]
hook: "Chạy CI xanh vẫn chưa chứng minh được hook có được gọi"
tension: tuong_ma_hoa_ra
sides: ["CI Claude xanh, tưởng hook đã chạy", "Chưa có bằng chứng hook được gọi, Codex còn thất bại"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Không có máy Windows: thăm dò hook bằng runner CI

**Bối cảnh:** Không có máy Windows nào đã đăng nhập Claude Code và Codex. Hook trên Windows có thể chạy qua Git Bash hoặc cmd tùy host, và chưa ai kiểm.
**Chuyện gì xảy ra:** Agent tra cộng đồng: Claude Code có thể chạy hook qua Git Bash, Codex qua cmd. Lệnh hook được đổi sang đường dẫn gạch chéo tới momentry.cmd để chạy ở cả hai. Workflow chạy tay trên runner Windows cài thật rồi mở phiên không có khoá API, và đọc hook.log tìm dòng hook.spawned. Lần chạy Claude xanh nhưng chưa đủ để khẳng định hook được gọi; Codex lần đầu thất bại.
**Bài học:** Cài xong không có nghĩa là hook chạy; hãy đo đúng điều cần đo, ví dụ có dòng hook.spawned hay không.
**Artefact:** Đoạn hook.log có hoặc không có dòng hook.spawned, che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Dev trên Linux/macOS thường ghi 'chưa kiểm trên Windows' hoặc nhờ người dùng báo lỗi sau khi phát hành; ở đây khác ở Runner GitHub miễn phí là máy Windows thật, nên có thể điều tra hành vi phụ thuộc OS, thậm chí thăm dò công cụ của bên thứ ba, mà không cần mua máy hay dùng tài khoản cá nhân. Người làm một mình sẽ muốn cách này.
