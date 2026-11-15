---
id: 2026-11-03-test-xanh-tren-clone-sach-do
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L146", "claude:ab9a1dd8#L149", "claude:ab9a1dd8#L156", "claude:ab9a1dd8#L170"]
hook: "Test qua 205/205 trên clone sạch, nhưng đỏ trong bản làm việc"
tension: tuong_ma_hoa_ra
sides: ["clone sạch qua 205 trên 205 test", "bản làm việc trượt vì test quét thư mục chưa track"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test xanh trên clone sạch, đỏ trong bản làm việc: test quét cả thư mục chưa git

**Bối cảnh:** Bộ test kiểm import quét mọi file .mjs trong repo, kể cả thư mục chưa commit. Chạy trên bản làm việc và trên clone sạch cho hai kết quả khác nhau.
**Chuyện gì xảy ra:** Trên bản làm việc, 202 trên 203 test qua, vì test đọc cả thư mục công cụ agent chưa được track. Trên clone sạch, 205 trên 205 qua. Sau khi loại thư mục không thuộc gói, số test tăng dần: 230, 232, 247 khi thêm module mới.
**Bài học:** Test quét cả cây thư mục phải chạy trên clone sạch, không chỉ trên bản đang làm, vì file chưa track có thể làm đỏ test.
**Artefact:** Hai dòng đầu ra 'ℹ pass' của node --test, một cho bản làm việc và một cho clone. Che đường dẫn.
