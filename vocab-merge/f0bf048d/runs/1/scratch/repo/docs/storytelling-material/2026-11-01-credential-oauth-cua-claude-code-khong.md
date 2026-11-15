---
id: 2026-11-01-credential-oauth-cua-claude-code-khong
date: 2026-11-01
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3505", "claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
hook: "Chép token đăng nhập sang user thứ hai, cả hai cùng bị 401"
tension: giup_ma_hai
sides: ["chép credential để user thứ hai dùng ngay", "token làm mới thay bản cũ, hai bên đá nhau 401"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Credential OAuth của Claude Code không thể chép giữa hai user Linux: token làm mới làm hỏng bản còn lại

**Bối cảnh:** Người dùng muốn chép phiên đăng nhập có sẵn sang user mới thay vì đăng nhập lại.
**Chuyện gì xảy ra:** Phiên Claude Code tự làm mới token theo chu kỳ và token cũ bị thay. Hai user dùng chung một bản chép sẽ đá nhau, lỗi 401 xuất hiện giữa lượt chạy thật. Chép chỉ chạy được lúc đầu. Khuyến nghị: mỗi user tự /login.
**Bài học:** Mỗi user một phiên đăng nhập OAuth; không chép token có cơ chế tự làm mới.
**Artefact:** Thông báo 401 minh hoạ (che token).
