---
id: 2026-10-21-fgos-list-mac-dinh-an-viec
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L487", "claude:9514b261#L513", "claude:9514b261#L542", "claude:9514b261#L1467"]
hook: "Lệnh liệt kê 269 việc, nhưng việc quan trọng nhất lại ẩn"
tension: cam_ma_van_lot
sides: ["liệt kê đủ 269 việc đang mở", "việc quan trọng nhất đã xong nên bị ẩn, có 1195 nếu thêm --all"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# fgos list mặc định ẩn việc đã xong, nên tìm thiếu

**Bối cảnh:** Tìm work item liên quan đến quản lý quyết định bằng lệnh fgos list.
**Chuyện gì xảy ra:** Lệnh mặc định trả 269 item đang mở, nên item quan trọng nhất đã xong không xuất hiện. Dùng --all thì có 1195 item. Lần parse đầu cũng hỏng vì cấu trúc JSON là dict chứ không phải list.
**Bài học:** Khi tìm xem việc đã làm chưa, dùng cờ hiện cả việc đã xong. Đừng tin danh sách mặc định.
**Artefact:** Hai con số 269 và 1195 trên cùng một bảng.
