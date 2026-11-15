---
id: 2026-10-29-khi-kiem-ke-nhieu-repo-cung-c455
code: M-YBB8
aliases: [M-YBB8]
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L519", "claude:0faf0bb2#L521", "claude:0faf0bb2#L523", "claude:0faf0bb2#L1585", "claude:0faf0bb2#L1587", "claude:0faf0bb2#L1723", "claude:0faf0bb2#L1725", "claude:0faf0bb2#L1727", "claude:0faf0bb2#L1774", "claude:0faf0bb2#L1886"]
hook: "Sub-agent chạy song song, nhưng agent chính vẫn kiểm lại từng trích dẫn"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi kiểm kê nhiều repo cùng lúc, agent chạy song song các sub-agent, mỗi cái một mảng, rồi agent chính đối chiếu lại các trích dẫn (đường dẫn, số dòng) trước khi ghi vào tài liệu.

**Chuyện gì xảy ra:** Khi kiểm kê nhiều repo cùng lúc, agent chạy song song các sub-agent, mỗi cái một mảng, rồi agent chính đối chiếu lại các trích dẫn (đường dẫn, số dòng) trước khi ghi vào tài liệu.
**Góc người ngoài:** cách làm phổ biến là Đọc từng repo tuần tự, rồi tóm tắt theo trí nhớ hoặc kết quả tìm kiếm web, ít khi kiểm lại từng trích dẫn trước khi lưu; ở đây khác ở Kết quả nhanh hơn và có bằng chứng kiểm được. Người đọc sẽ muốn biết vì sao không tin bản tóm tắt đầu tiên và cách chạy đối chiếu.
