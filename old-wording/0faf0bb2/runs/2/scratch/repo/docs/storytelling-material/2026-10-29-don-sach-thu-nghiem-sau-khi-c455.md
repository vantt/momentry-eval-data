---
id: 2026-10-29-don-sach-thu-nghiem-sau-khi-c455
code: M-SGTS
aliases: [M-SGTS]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L2431", "claude:0faf0bb2#L2452", "claude:0faf0bb2#L2504", "claude:0faf0bb2#L2547", "claude:0faf0bb2#L2572", "claude:0faf0bb2#L2591", "claude:0faf0bb2#L2613", "claude:0faf0bb2#L2624", "claude:0faf0bb2#L3182", "claude:0faf0bb2#L3198"]
hook: "Xoá thư mục chính chưa phải sạch: phải quét cả cache và cổng"
tension: none
sides: []
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn sạch thử nghiệm sau khi xong: gỡ CLI, container, volume, thư mục dữ liệu, và các session/cache do thử nghiệm sinh ra, rồi kiểm lại bằng grep và kiểm tra cổng

**Chuyện gì xảy ra:** Dọn sạch thử nghiệm sau khi xong: gỡ CLI, container, volume, thư mục dữ liệu, và các session/cache do thử nghiệm sinh ra, rồi kiểm lại bằng grep và kiểm tra cổng
**Góc người ngoài:** cách làm phổ biến là Dọn bằng cách xoá thư mục chính và bỏ qua cache hay bản ghi phụ; hiếm khi quét lại toàn máy để tìm dấu vết; ở đây khác ở Người đọc sẽ hỏi làm sao biết đã sạch, vì phiên này còn tìm ra transcript đã xoá, file cache và bản ghi phụ, và lập bảng hoàn tác trong runbook để người khác làm lại được.
