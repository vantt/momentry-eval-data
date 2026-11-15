---
id: 2026-11-02-reviewer-agent-tim-lenh-duong-di-3c6e
code: M-S1VW
aliases: [M-S1VW]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1777", "claude:2dfb5915#L1950"]
hook: "Một lệnh tìm đường đi làm treo cả server, ping cũng không trả lời"
tension: nho_ma_to
sides: ["Chỉ là tham số max_len từ 8 đến 10", "Số đường đi nổ theo cấp số nhân, server treo mọi request"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Reviewer agent tìm lệnh đường đi có thể làm treo server MCP

**Bối cảnh:** Các tool paths, loops và all_loops nhận max_len từ model mà không có trần.
**Chuyện gì xảy ra:** Với max_len 8 đến 10 trên vault dày liên kết, số đường đi tăng theo cấp số nhân, CPU 100% và RAM tăng cho tới khi bị OS giết. Server đơn luồng giữ khoá state nên mọi request sau đó, kể cả ping, đều treo. Fix: max_len tối đa 12, và tự dừng sau 10 giây.
**Bài học:** Mọi truy vấn đệ quy mà đầu vào đến từ model đều cần trần độ sâu và thời gian chạy.
**Góc người ngoài:** cách làm phổ biến là Nhận kết quả 'đã xong' từ agent và tin, hoặc đọc lướt tóm tắt; ở đây khác ở Phiên yêu cầu agent ghi số cụ thể, rồi một agent review khác đọc code và tìm lỗi (ví dụ treo khi stderr lỗi UTF-8, alias bomb 1,45 GB). Người đọc muốn biết vì sao review độc lập bắt được lỗi mà agent viết không thấy.
