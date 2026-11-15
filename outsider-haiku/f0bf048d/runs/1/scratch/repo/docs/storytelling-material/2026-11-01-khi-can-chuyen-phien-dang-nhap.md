---
id: 2026-11-01-khi-can-chuyen-phien-dang-nhap
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L3505", "claude:f0bf048d#L3510", "claude:f0bf048d#L3516"]
hook: "Cách nhanh nhất để chuyển phiên đăng nhập lại gây lỗi 401 giữa chừng"
tension: giup_ma_hai
sides: ["chép file token sang user khác cho nhanh", "hai bản token tự làm mới đá nhau, lỗi 401 giữa lúc chạy việc"]
strength: 2
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi cần chuyển phiên đăng nhập Claude Code sang một user Linux khác, agent không chép file token. Nó giải thích rằng token OAuth tự làm mới, hai bản chép sẽ đá nhau và gây lỗi 401 giữa lúc chạy việc, rồi đưa phương án đăng nhập riêng cho từng user.

**Chuyện gì xảy ra:** Khi cần chuyển phiên đăng nhập Claude Code sang một user Linux khác, agent không chép file token. Nó giải thích rằng token OAuth tự làm mới, hai bản chép sẽ đá nhau và gây lỗi 401 giữa lúc chạy việc, rồi đưa phương án đăng nhập riêng cho từng user.
**Góc người ngoài:** cách làm phổ biến là Copy file ~/.claude/.credentials.json sang user khác là cách nhanh nhất, nhiều người làm mà không biết token sẽ xung đột; ở đây khác ở Đây là một hành vi kỹ thuật cụ thể và có lý do, agent cảnh báo trước khi người dùng làm theo. Người đọc muốn biết vì sao nên tách phiên đăng nhập theo user.
