---
id: 2026-10-29-khi-can-khao-sat-nhieu-codebase
date: 2026-10-29
repo: repo
status: raw
signals: []
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:0faf0bb2#L1584", "claude:0faf0bb2#L1589", "claude:0faf0bb2#L1722", "claude:0faf0bb2#L1727", "claude:0faf0bb2#L1837", "claude:0faf0bb2#L1843", "claude:0faf0bb2#L1969", "claude:0faf0bb2#L1972"]
hook: "Khảo sát nhiều repo thì chia mỗi tác vụ con một mảng, đừng đọc tuần tự"
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

# Khi cần khảo sát nhiều codebase hoặc nhiều nguồn cùng lúc, agent chạy song song các tác vụ con, mỗi tác vụ một mảng, rồi tổng hợp kết quả trong một lượt.

**Chuyện gì xảy ra:** Khi cần khảo sát nhiều codebase hoặc nhiều nguồn cùng lúc, agent chạy song song các tác vụ con, mỗi tác vụ một mảng, rồi tổng hợp kết quả trong một lượt.
**Góc người ngoài:** cách làm phổ biến là Đọc tuần tự từng repo trong một cuộc hội thoại dài, dễ tràn ngữ cảnh và trộn lẫn các nguồn với nhau; ở đây khác ở Mỗi nhánh có báo cáo riêng có cấu trúc, agent chính đối chiếu lại trước khi dùng, nên khối lượng lớn vẫn gọn và có thể kiểm tra.
