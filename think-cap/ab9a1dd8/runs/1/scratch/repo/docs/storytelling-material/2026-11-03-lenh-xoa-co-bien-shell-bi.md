---
id: 2026-11-03-lenh-xoa-co-bien-shell-bi
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1396", "claude:ab9a1dd8#L1399"]
hook: "Lệnh rm -rf bị chặn chỉ vì một biến có thể rỗng"
tension: nho_ma_to
sides: ["một biến shell có thể rỗng", "lệnh xoá có thể vượt phạm vi nên bị chặn"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệnh xoá có biến shell bị Claude Code chặn, agent viết lại đường dẫn đầy đủ

**Bối cảnh:** Agent chạy lệnh dọn thư mục tạm có biến shell SP trong đường dẫn xoá.
**Chuyện gì xảy ra:** Chặn an toàn của Claude Code từ chối lệnh rm -rf vì biến có thể rỗng và khiến lệnh xoá vượt phạm vi. Thao tác này không bị chặn ở người dùng. Agent viết lại lệnh, thay biến bằng đường dẫn cụ thể.
**Bài học:** Lệnh xoá có biến là chỗ hệ thống an toàn chặn. Viết đường dẫn đầy đủ thay vì cố vượt qua chặn.
**Artefact:** Không có artefact.
