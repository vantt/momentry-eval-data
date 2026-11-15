---
id: 2026-11-02-bo-so-khop-voi-ban-python-3c6e
code: M-358V
aliases: [M-358V]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, artefact_nhin_duoc]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L474", "claude:2dfb5915#L1859"]
hook: "0 lệch trên 64 mục, chạy lại trên cả ba nền tảng"
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

# Bộ so khớp với bản Python: 0 trên 64 mục là một con số có ý nghĩa

**Bối cảnh:** Golden được dựng từ bản Python đã ghim sha. Rust phải tạo ra cùng các bảng và cùng kết quả để chứng minh là đã chuyển đúng.
**Chuyện gì xảy ra:** Tới khi phase 10 xong, bộ so khớp chạy trên vault thử kg-solo cho ra 64 mục khớp, 0 lệch chưa có tên, 0 mục chưa có. Số này được chạy lại trên CI cả ba nền tảng.
**Bài học:** Đóng băng đầu ra của bản cũ thành golden có sha ghim, rồi so từng bảng; điều này biến 'đã port đúng' thành một con số kiểm được.
**Artefact:** Dòng tổng kết bộ so khớp: 64 mục, 0 lệch chưa có tên, 0 mục chưa có. Không đưa nội dung golden ra ngoài.
**Góc người ngoài:** cách làm phổ biến là Viết test đơn vị cho chính code mới, xem nó chạy đúng là đủ, hiếm khi có một phiên bản chuẩn để so từng byte; ở đây khác ở Người đọc sẽ hỏi làm sao biết port đúng: câu trả lời là một golden đóng băng từ bản gốc, và mọi lệch được ghi có tên, có lý do, không bị bỏ qua lặng lẽ.
