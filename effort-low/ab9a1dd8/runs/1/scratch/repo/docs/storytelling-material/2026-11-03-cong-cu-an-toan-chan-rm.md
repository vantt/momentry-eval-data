---
id: 2026-11-03-cong-cu-an-toan-chan-rm
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1396", "claude:ab9a1dd8#L1399"]
hook: "Bị chặn rm -rf vì biến rỗng, agent không cần xoá nữa"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Công cụ an toàn chặn rm -rf với biến shell; agent chạy lại bằng node

**Bối cảnh:** Agent muốn xoá thư mục tạm của lần kiểm release bằng rm -rf trên một đường dẫn lấy từ biến shell.
**Chuyện gì xảy ra:** Lệnh bị chặn vì biến có thể rỗng và biến thành rm -rf trên thư mục gốc. Agent không lặp lại lệnh bị chặn; nó dùng node để tạo thư mục đầu ra mới, không cần xoá.
**Bài học:** Thay vì xoá thư mục tạm có đường dẫn từ biến, tạo đường dẫn mới với tên duy nhất; cơ chế an toàn đã bắt đúng rủi ro này.
**Artefact:** Thông báo chặn của công cụ. Không cần che gì.
