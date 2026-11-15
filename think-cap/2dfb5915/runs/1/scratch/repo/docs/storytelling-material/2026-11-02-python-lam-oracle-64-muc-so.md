---
id: 2026-11-02-python-lam-oracle-64-muc-so
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, artefact]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L474", "claude:2dfb5915#L1452", "claude:2dfb5915#L1859"]
hook: "64 mục so khớp với Python, 0 lệch trên ba hệ điều hành"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Python làm oracle: 64 mục so khớp, 0 lệch

**Bối cảnh:** Port core Rust từ bản Python đã ghim sha. Thước đo là bộ so khớp (parity) chạy cả hai bên trên vault mẫu sinh tổng hợp.
**Chuyện gì xảy ra:** Bộ so khớp có 64 mục: 17 bảng index, 81 câu đáp án, 712 lời gọi tool, 21 lệnh CLI. Sau khi nối đủ lớp tool và related, kết quả là 64/64 khớp, 0 lệch chưa đặt tên, 0 mục thiếu. CI chạy cùng bộ kiểm trên Linux, macOS và Windows.
**Bài học:** Đặt thước đo là so khớp với bản cũ theo từng byte; câu chạy được chưa đủ để nói là xong.
**Artefact:** Bảng 64 mục chia nhóm (index, đáp án, tool, CLI). Che tên note và đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Phần lớn dự án khi port code sang ngôn ngữ khác chỉ viết unit test theo hành vi mong muốn, rồi kiểm bằng mắt hoặc vài ví dụ; ở đây khác ở Phiên này dựng một bộ so khớp chạy cả hai bản trên cùng vault, so từng bảng SQL, từng câu đáp án và từng lời gọi tool, và báo số lệch chưa có tên. Người đọc sẽ muốn biết vì sao đây là cách đáng tin hơn và cách dựng nó.
