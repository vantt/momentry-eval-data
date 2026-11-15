---
id: 2026-11-02-tools-call-treo-vo-han-khi
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1777", "claude:2dfb5915#L1780", "claude:2dfb5915#L1950"]
hook: "Một lần panic khi build index, server treo mãi không thoát"
tension: nho_ma_to
sides: ["một lần build index đầu tiên bị panic", "mọi tools/call chờ vô hạn, server không thoát"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# tools/call treo vô hạn khi build index panic

**Bối cảnh:** Review phần server MCP tìm ra hai lỗi có thể làm treo server.
**Chuyện gì xảy ra:** Nếu build index lần đầu panic, cờ ready không bao giờ được đặt. tools/call chờ không giới hạn nên treo mãi, và server cũng không thoát. Lỗi thứ hai: paths và loops nhận max_len không trần, từ khoảng 8 đến 10 cạnh có thể bùng nổ tổ hợp. Đã thêm catch_unwind, timeout cho tools/call, trần max_len là 12 và timeout truy vấn 10 giây.
**Bài học:** Mọi thao tác chờ phải có trần thời gian. Mọi tham số đến từ mô hình phải có trần.
**Artefact:** Không có.
