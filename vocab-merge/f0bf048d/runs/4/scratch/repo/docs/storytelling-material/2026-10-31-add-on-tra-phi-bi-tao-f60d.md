---
id: 2026-10-31-add-on-tra-phi-bi-tao-f60d
code: M-YERB
aliases: [M-YERB]
date: 2026-10-31
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1601", "claude:f0bf048d#L1604", "claude:f0bf048d#L1619", "claude:f0bf048d#L1620", "claude:f0bf048d#L1635"]
hook: "Khách chưa mua add-on vẫn bị tạo add-on trả phí"
tension: cam_ma_van_lot
sides: ["Kiểm tra add-on đã có ở nhánh workspace sẵn có", "Nhánh workspace chưa tồn tại bỏ qua kiểm tra nên vẫn lọt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Add-on trả phí bị tạo dù khách chưa mua: nhánh workspace chưa tồn tại bỏ qua kiểm tra

**Bối cảnh:** Thêm bộ kiểm add-on để chỉ tạo công cụ trả phí cho khách đã mua; plan khi workspace chưa có vẫn tạo server.
**Chuyện gì xảy ra:** Plan có hai nhánh: workspace có sẵn và workspace chưa tồn tại. Kiểm add-on chỉ có ở nhánh thứ nhất. Sửa danh sách MCP ở nhánh thứ hai để lọc add-on chưa mua. Kiểm lại bằng ba trường hợp: khách chưa mua, khách đã mua, workspace đã có sẵn.
**Bài học:** Khi công cụ có hai đường thực thi, kiểm điều kiện ở cả hai và có kiểm thử cho từng nhánh.
**Artefact:** Đầu ra plan có và không có dòng add-on.
