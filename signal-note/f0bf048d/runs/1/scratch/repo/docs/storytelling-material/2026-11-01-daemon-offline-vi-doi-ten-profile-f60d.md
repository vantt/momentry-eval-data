---
id: 2026-11-01-daemon-offline-vi-doi-ten-profile-f60d
code: M-EKRF
aliases: [M-EKRF]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2896", "claude:f0bf048d#L2906", "claude:f0bf048d#L2908", "claude:f0bf048d#L2932", "claude:f0bf048d#L2938", "claude:f0bf048d#L2947"]
hook: "Đổi tên profile một lần, daemon báo offline cả hai workspace"
tension: nho_ma_to
sides: ["chỉ đổi tên profile", "daemon không thấy lệnh và không kiểm lại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Daemon offline vì đổi tên profile trước khi có lệnh bọc

**Bối cảnh:** Ba runtime profile mới: Codex, Grok, Gemini, mỗi cái ở hai workspace.
**Chuyện gì xảy ra:** Profile được tạo tên pi-openai-codex, rồi đổi thành pi-openai-tetnu trước khi lệnh bọc tương ứng có trên máy. Daemon không tìm thấy lệnh nên đánh dấu offline. Daemon chỉ kiểm lại profile khi profile bị sửa. Tắt rồi bật profile thì runtime online ở cả hai workspace.
**Bài học:** Daemon chỉ kiểm lệnh khi profile thay đổi. Khi đổi tên profile, đổi luôn lệnh trên máy và sửa lại profile sau đó.
**Artefact:** Bảng runtime online/offline theo workspace (che ID).
