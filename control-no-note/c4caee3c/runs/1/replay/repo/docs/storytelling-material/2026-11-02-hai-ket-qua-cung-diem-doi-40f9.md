---
id: 2026-11-02-hai-ket-qua-cung-diem-doi-40f9
code: M-W7VN
aliases: [M-W7VN]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2663", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247"]
hook: "Hai kết quả cùng điểm đổi chỗ, CI đỏ hai lần"
tension: nho_ma_to
sides: ["Mã tìm kiếm không hề đổi", "Thứ tự các kết quả bằng điểm làm test đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
unverified: [agent_only]
privacy: unchecked
links: []
threads: []
---

# Hai kết quả cùng điểm đổi chỗ, test snapshot chập chờn trên CI

**Bối cảnh:** Snapshot của pack so thứ tự tuyệt đối từng kết quả. Trên máy khác, hai note có điểm hybrid bằng hệt nhau nên thứ tự đổi theo thứ tự index.
**Chuyện gì xảy ra:** CI catchup đỏ hai lần ở cùng một test. Agent sửa phép so sánh: các kết quả cùng điểm được coi là một nhóm không có thứ tự, phần còn lại vẫn so khớp tuyệt đối, và mã tìm kiếm không đổi. Một test khác cũng được sửa vì nó phụ thuộc biến môi trường do file test khác để lại.
**Bài học:** Khi so kết quả xếp hạng, xử lý hoà điểm một cách tường minh. Test không được phụ thuộc thứ tự chạy file.
