---
id: 2026-11-02-agent-khong-dung-o-viec-kho
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L52", "claude:2dfb5915#L73", "claude:2dfb5915#L1426", "claude:2dfb5915#L1859", "claude:2dfb5915#L1969", "claude:2dfb5915#L2254"]
hook: "Agent không tin test của mình, so từng byte với bản Python gốc"
tension: tuong_ma_hoa_ra
sides: ["Test đơn vị pass là yên tâm", "Chỉ so từng byte với bản gốc mới biết có lệch"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent không dừng ở việc khó, mà tự tìm cách kiểm chứng ngay trên máy: so sánh từng byte đầu ra với bản Python gốc (bộ parity), thay vì chỉ tin test của chính mình.

**Chuyện gì xảy ra:** Agent không dừng ở việc khó, mà tự tìm cách kiểm chứng ngay trên máy: so sánh từng byte đầu ra với bản Python gốc (bộ parity), thay vì chỉ tin test của chính mình.
**Góc người ngoài:** cách làm phổ biến là Phần lớn người viết test đơn vị theo kỳ vọng của mình, và so với chuẩn cũ bằng vài ví dụ tay; ở đây khác ở Người đọc sẽ muốn biết cách có một bản tham chiếu chạy được (golden dump từ Python ở sha ghim) và so khớp tự động, vì nó bắt được lệch mà test đơn vị bỏ sót.
