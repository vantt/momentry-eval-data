---
id: 2026-10-21-bang-ghe-hoi-dong-mo-phong-fd46
code: M-WV9V
aliases: [M-WV9V]
date: 2026-10-21
repo: repo
status: raw
signals: [đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L2612", "claude:9514b261#L2630", "claude:9514b261#L2795", "claude:9514b261#L2920", "claude:9514b261#L2966", "claude:9514b261#L3966"]
hook: "Mô phỏng chạy 11/11 ghế hội đồng, nhưng ban đầu thiếu một cờ nên gán sai ghế"
tension: tuong_ma_hoa_ra
sides: ["Tin trần flagship áp cho mọi ghế, mô phỏng đã đúng", "Thiếu cờ herdr nên gán sai family; ghế critical thực ra chạy tầng frontier"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bảng ghế hội đồng mô phỏng sai vì thiếu cờ herdr, và giả định trần model cũng sai

**Bối cảnh:** Người dùng muốn mở hội đồng kiến trúc gồm nhiều model khác nhà cung cấp. Agent cần biết mỗi ghế được gán family và model nào trước khi chạy.
**Chuyện gì xảy ra:** Ban đầu agent chạy bộ mô phỏng không có herdr, nên gán ghế cho một family khác. Agent cũng tin trần flagship áp cho mọi ghế. Lệnh dispatch explain (có herdr) cho thấy ghế critical chạy tầng frontier. Walk còn thiếu deepseek và z-ai nên mất dự phòng. Sau khi sửa cấu hình, mô phỏng đạt 11 trên 11 ghế có gán được. Khi chạy thật, bước shaping trả execution-failure ở một ghế.
**Bài học:** Mô phỏng phân công phải chạy đúng môi trường thật, gồm cả session. Nếu không, bảng ghế trông đúng mà sai.
**Artefact:** Bảng hai cột: ghế theo mô phỏng cũ so với ghế theo explain.
