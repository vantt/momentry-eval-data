---
id: 2026-11-03-dat-mot-dieu-kien-dung-cho-d5ef
code: M-0KGD
aliases: [M-0KGD]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L674", "claude:ab9a1dd8#L2240", "claude:ab9a1dd8#L2962"]
hook: "Một điều kiện dừng khiến agent tự làm hết nhiều phase"
tension: it_ma_nhieu
sides: ["Một điều kiện dừng duy nhất cho phiên", "Agent tự làm qua nhiều phase, chỉ hỏi khi push hay phát hành"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đặt một điều kiện dừng cho phiên (Stop hook) là hoàn tất plan, rồi agent tự làm tiếp qua nhiều phase. Agent chỉ dừng hỏi khi gặp việc ra ngoài như push hoặc phát hành công khai.

**Chuyện gì xảy ra:** Đặt một điều kiện dừng cho phiên (Stop hook) là hoàn tất plan, rồi agent tự làm tiếp qua nhiều phase. Agent chỉ dừng hỏi khi gặp việc ra ngoài như push hoặc phát hành công khai.
**Góc người ngoài:** cách làm phổ biến là Agent thường dừng sau mỗi lượt, rồi chờ người dùng gõ 'tiếp tục'. Người dùng phải theo dõi từng bước; ở đây khác ở Người dùng giao một mục tiêu rõ ràng rồi đi làm việc khác. Agent không hỏi lại những quyết định nó tự làm được, chỉ hỏi đúng ba việc khó đảo ngược. Người đọc sẽ hỏi làm sao để agent không dừng giữa chừng và vẫn biết khi nào nên hỏi.
