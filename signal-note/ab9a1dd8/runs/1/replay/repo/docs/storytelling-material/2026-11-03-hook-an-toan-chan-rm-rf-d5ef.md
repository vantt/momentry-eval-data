---
id: 2026-11-03-hook-an-toan-chan-rm-rf-d5ef
code: M-NMC7
aliases: [M-NMC7]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1385", "claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1396", "claude:ab9a1dd8#L1399"]
hook: "Hook chặn rm -rf vì biến có thể rỗng, agent đổi cách làm"
tension: cam_ma_van_lot
sides: ["Hook chặn lệnh xoá nguy hiểm vì biến có thể rỗng", "Agent không thử lại, chạy trực tiếp bằng node"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook an toàn chặn rm -rf vì biến shell có thể rỗng; agent không cố lại mà đổi cách làm

**Bối cảnh:** Kiểm bản cập nhật v0.1.1 cần tạo thư mục dist mới trong sandbox.
**Chuyện gì xảy ra:** Lệnh có rm -rf dựa trên biến chưa chắc có giá trị bị kiểm tra an toàn chặn. Agent không thử lại lệnh đó, mà chạy trực tiếp bằng node để tạo bản 0.1.1.
**Bài học:** Khi công cụ an toàn chặn rm -rf với biến, đừng vòng qua. Tạo thư mục mới với tên cố định, hoặc để người dùng xoá.
**Artefact:** Không có artefact đáng chụp.
