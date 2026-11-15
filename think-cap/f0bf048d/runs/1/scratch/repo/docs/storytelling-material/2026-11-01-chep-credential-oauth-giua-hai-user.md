---
id: 2026-11-01-chep-credential-oauth-giua-hai-user
date: 2026-11-01
repo: repo
status: raw
signals: ["5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L3505", "claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
hook: "Chép credential sang user khác chạy được, rồi 401 khi token quay vòng"
tension: giup_ma_hai
sides: ["Chép file credential cho nhanh, chạy được ngay", "Mỗi lần làm mới token, bản của user kia hỏng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chép credential OAuth giữa hai user Linux sẽ đá nhau khi token quay vòng

**Bối cảnh:** Claude Code cần đăng nhập riêng cho mỗi user Linux; user mới chưa có phiên.
**Chuyện gì xảy ra:** Đề xuất chép file credential của user cũ sang. Chép được và chạy được lúc đầu, nhưng mỗi phiên tự làm mới token và token cũ bị thay, nên user này làm mới thì bản của user kia hỏng với lỗi 401. Khuyến nghị đăng nhập riêng cho mỗi user (chỉ mất khoảng một phút).
**Bài học:** Token OAuth tự quay vòng; hai process dùng chung một bản chép sẽ làm hỏng nhau.
