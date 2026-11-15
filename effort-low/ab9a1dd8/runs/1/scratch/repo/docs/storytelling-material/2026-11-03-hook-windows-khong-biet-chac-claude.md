---
id: 2026-11-03-hook-windows-khong-biet-chac-claude
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
hook: "Một dòng hook Windows, hai shell khác nhau, chưa ai đo"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook Windows: không biết chắc Claude Code và Codex chạy hook bằng shell nào

**Bối cảnh:** Installer Windows phải ghi lệnh hook vào settings của Claude Code và hooks.json của Codex. Hai công cụ có thể dùng cmd, PowerShell hoặc Git Bash.
**Chuyện gì xảy ra:** Qua tìm kiếm, agent thấy báo cáo cộng đồng cho rằng Claude Code dùng Git Bash, còn Codex dùng cmd. Lệnh hook được đổi sang đường dẫn có dấu gạch chéo tới momentry.cmd để chạy được ở cả hai. Phần này vẫn chưa được đo trong phiên thật nên được ghi rõ là chưa kiểm.
**Bài học:** Đường dẫn lệnh hook trên Windows nên chạy được trên nhiều shell; và ghi rõ phần nào là suy luận từ báo cáo chứ chưa đo.
**Artefact:** Một dòng cấu hình hook trước và sau khi đổi dấu gạch. Che đường dẫn người dùng.
