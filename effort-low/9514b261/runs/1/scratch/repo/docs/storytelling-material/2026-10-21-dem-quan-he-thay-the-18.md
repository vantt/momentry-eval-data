---
id: 2026-10-21-dem-quan-he-thay-the-18
date: 2026-10-21
repo: repo
status: raw
signals: [số trước/sau, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1212", "claude:9514b261#L1237"]
hook: "18 quan hệ 'thay thế' nhưng chỉ 7 cặp được ghi thành quan hệ thật"
tension: tuong_ma_hoa_ra
sides: ["36 quyết định ADR có 18 quan hệ supersedes", "Chỉ 7 cặp ghi bằng relation, còn lại nằm trong câu chữ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đếm quan hệ thay thế: 18 quan hệ, chỉ 7 cặp ghi được bằng quan hệ

**Bối cảnh:** Trước khi thiết kế bộ đọc quyết định hiệu lực, agent đếm dữ liệu quyết định thật trong event log thay vì tin tài liệu.
**Chuyện gì xảy ra:** Trong 36 quyết định ADR có 18 quan hệ supersedes, nhưng chỉ 7 cặp có quan hệ được ghi bằng cơ chế relation. Trong 7 cặp đó 5 cặp chỉ thay một phần. Ít nhất 4 quyết định thay thế nhau chỉ trong câu chữ, không có quan hệ. Có đích thay thế không phải quyết định.
**Bài học:** Đếm dữ liệu thật trước khi thiết kế lớp đọc; giả định 'chuỗi thay thế đầy đủ' thường sai.
**Artefact:** Bảng: loại quan hệ, số cặp, số cặp chỉ thay một phần, số quyết định chỉ nêu trong câu chữ.
