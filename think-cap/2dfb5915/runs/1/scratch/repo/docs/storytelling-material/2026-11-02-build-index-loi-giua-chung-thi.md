---
id: 2026-11-02-build-index-loi-giua-chung-thi
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, người duyệt]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1091"]
hook: "Build index lỗi một lần, link cũ ở lại mãi không ai thấy"
tension: cam_ma_van_lot
sides: ["Lần build sau chạy bình thường", "Link cũ ở lại vì không thấy note đổi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Build index lỗi giữa chừng thì link cũ ở lại mãi

**Bối cảnh:** Index SQLite ghi note, edge và meta trong ba transaction riêng, Python cũng làm vậy.
**Chuyện gì xảy ra:** Review thấy: nếu derive lỗi sau transaction đầu, lần build sau không thấy note đổi nên không tính lại edge, link cũ ở mãi. Lỗi này nằm trong spec Python nên parity không bắt được. Sửa bằng cờ dirty trong meta. Thêm lock file, transaction IMMEDIATE, busy timeout 30 s, chờ tối đa 5 phút. Build song song còn có thể tranh khoá ghi, nên đọc file trước khi mở transaction.
**Bài học:** So khớp với bản cũ không chứng minh bản cũ đúng; còn phải kiểm đường lỗi và build đồng thời.
**Artefact:** Sơ đồ ba transaction trước và sau, vẽ tay.
