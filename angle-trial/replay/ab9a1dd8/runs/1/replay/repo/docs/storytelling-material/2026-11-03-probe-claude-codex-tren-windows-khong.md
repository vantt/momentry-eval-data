---
id: 2026-11-03-probe-claude-codex-tren-windows-khong
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3077", "claude:ab9a1dd8#L3091", "claude:ab9a1dd8#L3233"]
hook: "Không đăng nhập, không khoá API, vẫn đo được hook"
tension: it_ma_nhieu
sides: ["Phiên không có khoá API, chỉ báo lỗi đăng nhập", "hook.log vẫn cho biết hook đã được gọi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe Claude/Codex trên Windows: không đăng nhập vẫn đo được hook

**Bối cảnh:** Issue đo hook trên Windows không thể làm đầy đủ vì máy không có Claude Code và Codex đã đăng nhập.
**Chuyện gì xảy ra:** Agent tạo workflow chỉ chạy tay trên runner Windows, cài công cụ thật, rồi mở phiên không có khoá API. Nếu hook.log có dòng hook.spawned thì hook đã được gọi trước khi báo lỗi đăng nhập. Không dùng bí mật hay tài khoản của người dùng.
**Bài học:** Dùng log của hook như tín hiệu. Lỗi đăng nhập không nhất thiết nghĩa là hook chưa chạy.
**Artefact:** Ảnh workflow probe và dòng log hook.spawned. Che tên người dùng và đường dẫn home.
**Góc người ngoài:** cách làm phổ biến là Dev không có máy Windows thường đoán hành vi, hoặc nhờ người có máy kiểm tay; ở đây khác ở Đo được một hành vi phụ thuộc môi trường mà máy Linux không thể mô phỏng, và không cần tài khoản hay khoá API. Người đọc sẽ muốn biết cách dựng một bài đo như vậy.
