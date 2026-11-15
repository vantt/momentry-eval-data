---
id: 2026-11-02-gop-7-nhanh-song-song-vao-3c6e
code: M-XA5V
aliases: [M-XA5V]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L1599", "claude:2dfb5915#L1696", "claude:2dfb5915#L1715"]
hook: "Gộp 7 nhánh, PORTING.md lặp tới 4 bản của cùng một mục"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gộp 7 nhánh song song vào main, PORTING.md bị lặp hai lần

**Bối cảnh:** Mỗi nhánh song song đều sửa spec/PORTING.md, nên merge liên tiếp gây xung đột.
**Chuyện gì xảy ra:** Mỗi lần merge sinh xung đột ở cùng một file. Có lần mục MCP server bị lặp hai bản, phải xoá bản cũ. Có lần đến 4 bản lặp của mục khác. Agent chốt quy trình: giải xung đột bằng script, rồi kiểm lại số mục trước khi commit.
**Bài học:** File tài liệu dùng chung là điểm nghẽn khi làm song song. Nên tách mỗi nhánh một file riêng.
**Góc người ngoài:** cách làm phổ biến là Thường một người làm tuần tự, hoặc chạy vài tác vụ song song trong cùng một thư mục làm việc và tự gỡ xung đột khi gộp; ở đây khác ở Mỗi agent làm trong nhánh riêng, không đụng nhau; controller merge từng nhánh khi xong, chạy lại gate và push. Người đọc muốn biết vì sao cách này tránh được xung đột và việc agent này không làm hỏng việc agent kia.
