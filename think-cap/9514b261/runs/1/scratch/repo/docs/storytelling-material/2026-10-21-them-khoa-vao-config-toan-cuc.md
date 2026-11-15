---
id: 2026-10-21-them-khoa-vao-config-toan-cuc
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3609", "claude:9514b261#L3620"]
hook: "Thêm một khoá vào config toàn cục có thể làm hỏng workspace bản cũ"
tension: nho_ma_to
sides: ["Chỉ thêm một khoá vào config", "Workspace chạy bản cũ ở máy khác có thể hỏng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thêm khoá vào config toàn cục có thể làm hỏng workspace bản cũ

**Bối cảnh:** Hướng dẫn cài TheHive cảnh báo rằng thêm khoá mới vào config toàn cục từng làm hỏng workspace chạy release cũ.
**Chuyện gì xảy ra:** Hướng dẫn yêu cầu cập nhật các máy khác trước rồi mới đổi config toàn cục. Agent không kiểm được workspace khác từ máy này nên để việc đó như một bước còn lại và báo người dùng.
**Bài học:** Đẩy cập nhật cho mọi máy và workspace trước khi đổi config dùng chung, không đổi trước rồi mới kiểm.
**Artefact:** Đoạn cảnh báo trích từ hướng dẫn, không kèm khoá.
