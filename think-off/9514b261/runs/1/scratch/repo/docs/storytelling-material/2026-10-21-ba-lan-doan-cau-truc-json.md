---
id: 2026-10-21-ba-lan-doan-cau-truc-json
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L492", "claude:9514b261#L502", "claude:9514b261#L508", "claude:9514b261#L513"]
hook: "Lọc mặc định chỉ thấy 269 mục, thêm --all ra 1195"
tension: tuong_ma_hoa_ra
sides: ["tưởng danh sách mặc định là toàn bộ", "thật ra giấu hơn 900 mục đã done"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba lần đoán cấu trúc JSON của CLI: 269 mục mở, còn 1195 khi thêm --all

**Bối cảnh:** Cần lọc work item liên quan đến quyết định và tài liệu từ lệnh list của fgos.
**Chuyện gì xảy ra:** Script lọc lỗi ba lần vì đoán sai cấu trúc JSON (dict với khoá data và work). Lần lọc mặc định chỉ thấy 269 mục đang mở, nên các mục đã done như tsk-1lv không xuất hiện. Thêm --all thì có 1195 mục.
**Bài học:** Đọc schema trước khi viết script lọc, và kiểm xem lệnh mặc định có cắt bớt dữ liệu không.
**Artefact:** Hai con số 269 và 1195 cạnh nhau, kèm cờ --all.
