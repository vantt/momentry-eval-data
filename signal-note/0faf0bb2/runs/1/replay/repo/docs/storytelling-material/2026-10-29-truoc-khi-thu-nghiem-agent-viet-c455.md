---
id: 2026-10-29-truoc-khi-thu-nghiem-agent-viet-c455
code: M-WHWW
aliases: [M-WHWW]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L2784", "claude:0faf0bb2#L3150", "claude:0faf0bb2#L3404", "claude:0faf0bb2#L3747"]
hook: "Viết sẵn tiêu chí đạt/trượt trước khi chạy, thất bại vẫn biết vì sao"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi thử nghiệm, agent viết sẵn bộ tiêu chí đạt/trượt đánh số (a, b, c, d...). Sau khi chạy, báo từng tiêu chí đạt hay trượt, kể cả khi cả lần thử đó thất bại, và ghi nguyên nhân gốc vào báo cáo.

**Chuyện gì xảy ra:** Trước khi thử nghiệm, agent viết sẵn bộ tiêu chí đạt/trượt đánh số (a, b, c, d...). Sau khi chạy, báo từng tiêu chí đạt hay trượt, kể cả khi cả lần thử đó thất bại, và ghi nguyên nhân gốc vào báo cáo.
**Góc người ngoài:** cách làm phổ biến là Thử theo cảm tính, rồi kết luận 'chạy được' hoặc 'không được' mà không có danh sách tiêu chí rõ ràng và không tách nguyên nhân; ở đây khác ở Người đọc thấy kết quả 'đạt 5/5' hay 'trượt' có căn cứ, và biết chính xác phần nào còn chưa kiểm. Họ sẽ hỏi làm sao để không tự thuyết phục mình là thử nghiệm đã thành công.
