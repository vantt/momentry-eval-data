---
id: 2026-11-03-guardrail-chan-rm-rf-vi-bien-d5ef
code: M-QT55
aliases: [M-QT55]
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1396"]
hook: "Lệnh xoá bị chặn vì một biến có thể rỗng"
tension: nho_ma_to
sides: ["một biến có thể rỗng", "biến thành rm -rf trên thư mục gốc"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Guardrail chặn rm -rf vì biến không resolve

**Bối cảnh:** Agent định chạy lệnh xoá thư mục tạm trong một script có biến shell.
**Chuyện gì xảy ra:** Hệ thống từ chối lệnh vì biến có thể rỗng và biến lệnh thành rm -rf trên thư mục gốc. Agent không cố vượt qua, mà chạy lại đúng phần không cần xoá để lấy kết quả.
**Bài học:** Khi guardrail chặn một lệnh xoá, đừng tìm cách lách. Đưa đường dẫn về giá trị cố định hoặc bỏ bước xoá.
**Artefact:** Không có.
