---
id: 2026-10-09-cat-17-mcp-tool-cu-boundary
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, người duyệt]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3473", "omp:cd4449ab#L3485", "omp:cd4449ab#L3500", "omp:cd4449ab#L3520", "omp:cd4449ab#L3956", "omp:cd4449ab#L3959"]
hook: "Xoá 1.650 dòng code cũ, test ranh giới vẫn đỏ 5 lần"
tension: tuong_ma_hoa_ra
sides: ["xoá code thì tưởng gọn và sạch", "danh sách tool và annotation còn lệch, sửa 5 lần"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cắt 17 MCP tool cũ: boundary test đỏ 5 lần

**Bối cảnh:** Theo bảng contract, nhiều tool MCP cũ phải bị bỏ. Boundary test của curator kiểm tra mọi tool trong danh sách có tồn tại.
**Chuyện gì xảy ra:** Xoá 17 tool cũ. Boundary test vẫn đỏ vì danh sách compatible tool và annotation chưa khớp, phải sửa 5 lần. Commit c75baca thay đổi 19 file, +350 −1650 dòng.
**Bài học:** Khi thu hẹp bề mặt API, cập nhật danh sách tool được phép trước rồi mới xoá code, để test chỉ ra chỗ lệch.
**Artefact:** Danh sách tool MCP trước và sau khi cắt (che tên tool nội bộ nếu cần).
