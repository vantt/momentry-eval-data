---
id: 2026-10-21-chuoi-thay-the-quyet-dinh-36-fd46
code: M-2E8X
aliases: [M-2E8X]
date: 2026-10-21
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1163", "claude:9514b261#L1212", "claude:9514b261#L1237"]
hook: "36 quyết định, 18 quan hệ thay thế, mà 4 cái chỉ nằm trong câu chữ"
tension: tuong_ma_hoa_ra
sides: ["Có 18 quan hệ thay thế ghi sẵn, tưởng tính được quyết định nào còn hiệu lực", "5 trên 7 chỉ thay một phần, có cái trỏ tới mã băm tài liệu"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi thay thế quyết định: 36 ADR, 18 quan hệ, và ít nhất 4 quyết định chỉ nói trong câu chữ

**Bối cảnh:** Chủ hỏi reducer 'tập quyết định hiệu lực' có đủ dữ liệu chưa. Agent đếm trực tiếp trong event log.
**Chuyện gì xảy ra:** Trong 4679 sự kiện decision, 37 có scope. Trong 36 ADR có 8 quyết định mang quan hệ supersedes, tổng cộng 18 quan hệ. Với 7 cặp quyết định nền tảng, id khớp được nhưng 5 trên 7 chỉ thay một phần. Ít nhất 4 quyết định thay điều khoản chỉ được ghi trong câu chữ, và có đích thay thế không phải quyết định mà là một mã băm tài liệu. Dữ liệu vì vậy chưa đủ để tính tập hiệu lực.
**Bài học:** Muốn máy tính được cái nào còn hiệu lực, quan hệ thay thế phải là dữ liệu có cấu trúc, không được để trong văn bản.
**Artefact:** Bảng phân loại 7 cặp quan hệ, chỉ có số liệu. Không cần ảnh.
