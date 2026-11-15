---
id: 2026-10-31-cong-cu-tra-phi-lot-vao-f60d
code: M-J6W5
aliases: [M-J6W5]
date: 2026-10-31
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1601", "claude:f0bf048d#L1620", "claude:f0bf048d#L1633", "claude:f0bf048d#L1635"]
hook: "Khách chưa mua add-on, vậy mà plan định tạo công cụ trả phí"
tension: cam_ma_van_lot
sides: ["Bộ lọc add-on đã chặn công cụ trả phí khi khách chưa mua", "Nhánh workspace chưa tồn tại bỏ qua bộ lọc, công cụ trả phí vẫn lọt vào plan"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Công cụ trả phí lọt vào plan khi khách chưa mua

**Bối cảnh:** Sau khi thêm add-on DataForSEO, plan cho một khách chưa mua vẫn tạo server dataforseo.
**Chuyện gì xảy ra:** Plan có một nhánh riêng cho workspace chưa tồn tại và nhánh đó bỏ qua bộ lọc add-on. Agent tìm ra nhánh này, lọc add-on chưa mua ở cả hai nhánh, rồi kiểm plan trên ba trường hợp: có add-on, không có, và workspace đã tồn tại. Kết quả đúng như mong đợi: PageSpeed được gắn, DataForSEO không được tạo.
**Bài học:** Mọi nhánh của plan phải dùng cùng một bộ lọc. Kiểm từng nhánh riêng.
**Artefact:** Kết quả plan hai lần: có và không có add-on.
