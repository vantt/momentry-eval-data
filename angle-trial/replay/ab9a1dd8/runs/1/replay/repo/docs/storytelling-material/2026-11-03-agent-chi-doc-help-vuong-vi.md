---
id: 2026-11-03-agent-chi-doc-help-vuong-vi
date: 2026-11-03
repo: repo
status: raw
signals: [người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968"]
hook: "Agent kẹt 2 vòng vì lỗi là câu văn, không phải lệnh"
tension: nho_ma_to
sides: ["Thông báo lỗi chỉ là một câu gợi ý", "Agent mất 2 vòng, thêm một lệnh là hội tụ ngay"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent chỉ đọc --help vướng vì lỗi là câu văn, không phải lệnh

**Bối cảnh:** Có một vòng kiểm agent-native: agent mới chỉ được đọc --help và --json, rồi phải cài và đưa momentry doctor về trạng thái ok.
**Chuyện gì xảy ra:** Lần đầu vòng hội tụ sau 2 vòng. Agent kẹt vì thông báo lỗi gợi ý sửa bằng một câu văn, không phải lệnh chạy được. Agent thêm lệnh `config privacy-add` và vòng sau hội tụ ngay lần đầu.
**Bài học:** Mỗi thông báo lỗi nên kèm lệnh chạy được nguyên văn. Vòng agent giả lập là cách bắt lỗi này.
**Artefact:** So sánh thông báo lỗi cũ và mới. Che tên nguồn chặn riêng tư.
