---
id: 2026-10-31-truoc-khi-lam-thao-tac-rui
date: 2026-10-31
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1980", "claude:f0bf048d#L1983", "claude:f0bf048d#L2543", "claude:f0bf048d#L2550", "claude:f0bf048d#L3049"]
hook: "Agent đếm lại 3 chỗ chứa PAT thay vì tin kế hoạch viết sẵn"
tension: tuong_ma_hoa_ra
sides: ["Có kế hoạch rồi thì cứ làm theo là đủ", "Kiểm trạng thái thật mới biết có việc đang chạy"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi làm thao tác rủi ro, agent kiểm trạng thái thật trên máy và xác nhận bằng số liệu (đếm chỗ chứa PAT, kiểm daemon có task đang chạy trước khi dừng).

**Chuyện gì xảy ra:** Trước khi làm thao tác rủi ro, agent kiểm trạng thái thật trên máy và xác nhận bằng số liệu (đếm chỗ chứa PAT, kiểm daemon có task đang chạy trước khi dừng).
**Góc người ngoài:** cách làm phổ biến là Thường làm theo kế hoạch đã viết, không kiểm lại; dừng dịch vụ mà không biết có việc đang chạy hay không; ở đây khác ở Đối chiếu từng giả định với máy (grep chỗ chứa token, kiểm task đang chạy, kiểm runtime online sau khi đổi) trước và sau mỗi bước. Người đọc muốn biết cách tránh làm hỏng việc đang chạy.
