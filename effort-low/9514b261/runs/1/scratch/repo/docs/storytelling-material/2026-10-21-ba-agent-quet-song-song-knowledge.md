---
id: 2026-10-21-ba-agent-quet-song-song-knowledge
date: 2026-10-21
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1384", "claude:9514b261#L1417", "claude:9514b261#L1457", "claude:9514b261#L1572"]
hook: "Ba agent quét song song: 'engine mới' chỉ còn sáu thứ chưa có mã"
tension: tuong_ma_hoa_ra
sides: ["Tưởng cần xây cả engine quản lý tri thức mới", "Registry đã chạy với 479 doc, phần mới chỉ còn sáu thứ"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ba agent quét song song: Knowledge Registry đã chạy, KDE gần như trùng

**Bối cảnh:** Người dùng nghi một engine tài liệu mới trùng với hệ đã có. Agent bật ba researcher song song, mỗi người quét plans/reports, history/journals, work items/code/specs.
**Chuyện gì xảy ra:** Registry đã chạy thật: 479 topic, 479 doc, chiếm khoảng 15% trong 3146 file .md. Có 332 doc provisional và 147 active, 365 role khác nhau trên 479 doc, và ba chỉ mục song song (492, 479, 0 mục). Agent chính đã kiểm lại các con số bằng lệnh trước khi đưa tổng hợp. Phần thật sự mới của engine chỉ còn sáu thứ, chưa có mã.
**Bài học:** Khi nhiều agent đưa số liệu, kiểm lại vài con số bằng lệnh trước khi ra kết luận; số sai thường nằm ở phép đếm thô.
**Artefact:** Bảng ba chỉ mục song song và số doc theo trạng thái (không có đường dẫn nội bộ).
