---
id: 2026-11-02-parity-harness-so-muc-chua-co-3c6e
code: M-YBD6
aliases: [M-YBD6]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L860", "claude:2dfb5915#L866", "claude:2dfb5915#L1094", "claude:2dfb5915#L1209", "claude:2dfb5915#L1445", "claude:2dfb5915#L1859"]
hook: "Số mục «chưa có» giảm từ 47 về 0 qua từng merge"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Parity harness: số mục «chưa có» từ 47 giảm về 0 qua từng merge

**Bối cảnh:** Bộ so khớp chạy cùng vault thử kg-solo, so kết quả Rust với golden lấy từ Python ở một commit đã ghim.
**Chuyện gì xảy ra:** Sau khi merge phase 08, 17 mục khớp và 47 mục còn «chưa có». Các phase 09, 10, 11 và 12 lần lượt làm giảm số này: 44, 34, 15 rồi 0 trên 64 mục. Golden được commit và CI chạy được mà không cần Python.
**Bài học:** Viết bộ so khớp với đầu ra của bản gốc trước khi port, và ghi golden vào repo để CI chạy được không cần bản gốc.
**Artefact:** Bảng «Tổng: 64 mục, 0 lệch» qua các lần chạy (chụp terminal).
**Góc người ngoài:** cách làm phổ biến là So sánh thủ công hoặc viết test đơn vị cho từng hàm, không có bộ đo tiến độ 0/64 mục; ở đây khác ở Số 'chưa có' đi từ 47 xuống 0 qua từng merge và được CI kiểm mỗi lần push. Người đọc muốn biết cách biến 'port xong chưa' thành một con số.
