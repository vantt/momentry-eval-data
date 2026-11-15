---
id: 2026-11-03-thu-init-trong-home-tam-lenh-d5ef
code: M-EQ2X
aliases: [M-EQ2X]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Chuyện vặt, nhưng cho thấy vì sao mọi lần thử trong sandbox phải chạy bằng bash."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1199", "claude:ab9a1dd8#L1217", "claude:ab9a1dd8#L1225", "claude:ab9a1dd8#L1226", "claude:ab9a1dd8#L1236", "claude:ab9a1dd8#L1239"]
hook: "Lần chạy đầu lỗi vì env -i trong zsh, đổi sang script bash"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử init trong HOME tạm: lệnh env -i và zsh làm lần chạy đầu lỗi, phải chuyển sang script bash

**Bối cảnh:** Kiểm lệnh init trong HOME tạm để không đụng cấu hình thật.
**Chuyện gì xảy ra:** Lần chạy đầu báo file cấu hình không tồn tại vì sandbox dùng env -i trong zsh. Agent viết script sbx.sh chạy bằng bash, rồi init liệt kê các bước sẽ làm.
**Bài học:** Script thử nghiệm nên chạy bằng bash cố định (bash -c), không phụ thuộc shell tương tác.
**Artefact:** Không có artefact đáng chụp.
