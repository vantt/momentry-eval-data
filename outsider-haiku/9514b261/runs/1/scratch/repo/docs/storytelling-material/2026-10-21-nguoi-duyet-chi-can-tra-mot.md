---
id: 2026-10-21-nguoi-duyet-chi-can-tra-mot
date: 2026-10-21
repo: repo
status: raw
signals: [người duyệt]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L2645", "claude:9514b261#L3362", "claude:9514b261#L3579"]
hook: "Hàng chục quyết định chốt bằng đúng một chữ: '3'"
tension: it_ma_nhieu
sides: ["Người duyệt chỉ trả một chữ hoặc một số", "Agent nhận đủ quyết định để làm ngay"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Người duyệt chỉ cần trả một chữ

**Bối cảnh:** Agent cần người dùng quyết nhiều điểm trong một lượt làm việc dài.
**Chuyện gì xảy ra:** Thay vì hỏi rải rác, agent gom các câu cần quyết định thành bộ câu hỏi đánh số, mỗi câu có khuyến nghị. Người dùng trả lời bằng 'đồng ý' hoặc một số, và agent làm ngay. Nhiều quyết định trong phiên kết thúc chỉ bằng một chữ như '3' hoặc 'đồng ý'.
**Bài học:** Gom câu hỏi thành bảng có khuyến nghị đánh số. Người duyệt trả lời nhanh, và agent không phải dừng giữa chừng.
**Artefact:** Mẫu bộ câu hỏi, nội dung đã che.
