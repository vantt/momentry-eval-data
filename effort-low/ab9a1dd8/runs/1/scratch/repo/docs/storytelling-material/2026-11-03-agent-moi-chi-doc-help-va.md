---
id: 2026-11-03-agent-moi-chi-doc-help-va
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968", "claude:ab9a1dd8#L1969", "claude:ab9a1dd8#L1984", "claude:ab9a1dd8#L2230"]
hook: "Thông báo lỗi có lời sửa, nhưng agent không chạy được"
tension: giup_ma_hai
sides: ["lỗi đã kèm hướng dẫn sửa", "hướng dẫn là câu văn, agent không có lệnh để chạy"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent mới chỉ đọc --help và --json: lần đầu vướng vì lời sửa là câu văn, không phải lệnh

**Bối cảnh:** Mục tiêu: một agent mới, chỉ đọc --help và --json, tự cài và đưa doctor về ok mà không hỏi người.
**Chuyện gì xảy ra:** Vòng thử đầu tiên hỏng vì thông báo lỗi chỉ ghi câu hướng dẫn chỉnh sửa nguồn chặn riêng tư, không có lệnh chạy được. Agent thêm config privacy-add nhận tên làm đối số, và vòng thử hội tụ ngay lần đầu.
**Bài học:** Thông báo lỗi cho agent phải chứa lệnh chạy được nguyên văn; câu hướng dẫn bằng văn xuôi buộc agent đoán.
**Artefact:** Output của vòng thử cũ với câu hướng dẫn và output mới với lệnh. Che tên riêng nếu có.
