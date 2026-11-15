---
id: 2026-11-03-agent-chi-doc-help-ket-o-d5ef
code: M-XXVP
aliases: [M-XXVP]
date: 2026-11-03
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968", "claude:ab9a1dd8#L1984"]
hook: "Lỗi bảo 'hãy sửa' bằng câu văn, agent không có lệnh để chạy"
tension: giup_ma_hai
sides: ["Thông báo lỗi có hướng dẫn sửa", "Hướng dẫn là câu văn, agent kẹt 2 vòng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent chỉ đọc --help kẹt ở nguồn chặn riêng tư: hướng dẫn bằng câu văn không chạy được

**Bối cảnh:** Vòng kiểm agent-native: một agent mới chỉ đọc --help và --json, tự cài và đưa doctor về ok.
**Chuyện gì xảy ra:** Vòng đầu hội tụ sau 2 vòng vì thông báo lỗi bảo sửa bằng câu văn chứ không có lệnh chạy được. Agent thêm lệnh config privacy-add và viết lệnh sửa dưới dạng chạy được. Vòng sau hội tụ ngay ở vòng đầu.
**Bài học:** Thông báo lỗi phải chứa lệnh chạy được nguyên văn. Đo bằng một agent không có ngữ cảnh là cách bắt lỗi này.
**Artefact:** Log hai lần chạy vòng agent-native: 2 vòng rồi 1 vòng.
