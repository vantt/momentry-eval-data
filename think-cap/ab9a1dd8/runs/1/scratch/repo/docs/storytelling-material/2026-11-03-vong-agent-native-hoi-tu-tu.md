---
id: 2026-11-03-vong-agent-native-hoi-tu-tu
date: 2026-11-03
repo: repo
status: raw
signals: ["4"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968", "claude:ab9a1dd8#L2230"]
hook: "Thêm một lệnh thật thay cho câu hướng dẫn, hai vòng còn một"
tension: it_ma_nhieu
sides: ["chỉ thêm lệnh config privacy-add", "vòng kiểm thử agent-native giảm từ hai xuống một"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng agent-native hội tụ từ hai vòng xuống một: thêm lệnh thật thay cho câu hướng dẫn

**Bối cảnh:** Một agent mới, chỉ đọc --help và --json, được yêu cầu tự cài và đưa doctor về ok.
**Chuyện gì xảy ra:** Vòng đầu, agent vướng vì lệnh sửa cho nguồn chặn riêng tư chỉ là câu văn trong thông báo, không chạy được. Agent thêm lệnh config privacy-add. Vòng sau, agent hội tụ ngay ở lần đầu, từ hai vòng xuống một.
**Bài học:** Nếu thông báo lỗi chỉ đưa lệnh dạng văn bản, agent không chạy được. Thêm một lệnh thật để sửa.
**Artefact:** Đầu ra vòng agent qua hai vòng, không có đường dẫn người dùng.
