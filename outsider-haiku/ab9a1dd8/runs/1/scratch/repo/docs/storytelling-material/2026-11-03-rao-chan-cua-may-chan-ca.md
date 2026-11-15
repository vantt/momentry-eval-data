---
id: 2026-11-03-rao-chan-cua-may-chan-ca
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L1388", "claude:ab9a1dd8#L1396", "claude:ab9a1dd8#L1604", "claude:ab9a1dd8#L1613", "claude:ab9a1dd8#L3367"]
hook: "Rào chắn máy chặn cả lệnh xoá lẫn chữ \"dist\" trong workflow"
tension: cam_ma_van_lot
sides: ["rào chắn chặn lệnh nguy hiểm", "cả chữ vô hại cũng bị chặn, phải đổi cách làm"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Rào chắn của máy chặn cả lệnh xoá lẫn chữ dist

**Bối cảnh:** Môi trường làm việc có lớp chặn lệnh bash. Một lệnh xoá có biến có thể rỗng bị từ chối, và chuỗi dist bị chặn khi tạo workflow CI.
**Chuyện gì xảy ra:** Lệnh rm -rf với biến chưa chắc có giá trị bị chặn, agent chạy lại bằng script Node. Lệnh tạo workflow có chữ dist bị hook chặn, agent chuyển sang tool ghi file. Một lệnh chỉnh test có chuỗi !.git cũng bị chặn. Các chặn này buộc đổi cách làm ở nhiều bước.
**Bài học:** Khi rào chắn chặn, đọc lý do trước; lệnh xoá nên dùng đường dẫn cứng, không dùng biến có thể rỗng.
**Artefact:** Thông báo chặn, che đường dẫn tuyệt đối.
