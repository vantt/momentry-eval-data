---
id: 2026-11-02-agent-tu-chay-doi-chieu-voi
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L111", "claude:2dfb5915#L212", "claude:2dfb5915#L372", "claude:2dfb5915#L460", "claude:2dfb5915#L1152", "claude:2dfb5915#L1459"]
hook: "Viết lại sang Rust, agent không tin test: so với bản Python từng byte"
tension: tuong_ma_hoa_ra
sides: ["Vài unit test xanh thường được coi là đủ", "Agent so từng bảng, từng lệnh đến cấp byte với golden file ghim theo commit"]
strength: 1
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent tự chạy đối chiếu với bản gốc (Python) và coi kết quả so khớp là bằng chứng: so sánh từng bảng, từng câu trả lời, từng lệnh CLI, đến cấp byte, và dùng golden file đã ghim theo commit để so.

**Chuyện gì xảy ra:** Agent tự chạy đối chiếu với bản gốc (Python) và coi kết quả so khớp là bằng chứng: so sánh từng bảng, từng câu trả lời, từng lệnh CLI, đến cấp byte, và dùng golden file đã ghim theo commit để so.
**Góc người ngoài:** cách làm phổ biến là Dev thường viết vài unit test rồi tin kết quả. Khi chuyển ngôn ngữ, phần lớn chỉ kiểm vài ví dụ tay, không có bộ so khớp tự động trên dữ liệu thật ở cấp từng byte; ở đây khác ở Mọi bước sau đó đều dựa vào một bộ so khớp chạy được trong CI mà không cần Python hay token, nên agent có thể nói 'khớp 64/64, 0 lệch' với độ tin cậy cao. Người đọc sẽ muốn biết cách dựng được một bộ như vậy.
