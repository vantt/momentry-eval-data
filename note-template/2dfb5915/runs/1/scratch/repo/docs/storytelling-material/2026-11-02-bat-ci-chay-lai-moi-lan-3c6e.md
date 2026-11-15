---
id: 2026-11-02-bat-ci-chay-lai-moi-lan-3c6e
code: M-DCKF
aliases: [M-DCKF]
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L1459", "claude:2dfb5915#L2536", "claude:2dfb5915#L3658", "claude:2dfb5915#L3896", "claude:2dfb5915#L3917"]
hook: "Bắt AI theo dõi CI sau mỗi lần đẩy mã, kể cả bản thử"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bắt CI chạy lại mỗi lần đẩy mã và theo dõi cả đường phát hành thử trước khi báo xong

**Chuyện gì xảy ra:** Bắt CI chạy lại mỗi lần đẩy mã và theo dõi cả đường phát hành thử trước khi báo xong
**Góc người ngoài:** cách làm phổ biến là Thường đẩy mã rồi quên, hoặc chỉ kiểm tra CI một lần khi có lỗi; ở đây khác ở Agent theo dõi từng commit đến khi mọi job xanh, tải file phát hành về, kiểm sha256 từng file, và ghi kết quả vào plan. Người đọc sẽ hỏi làm sao biết bản phát hành thật sự chạy được.
