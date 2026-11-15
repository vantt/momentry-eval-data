---
id: 2026-10-21-chuoi-thay-the-quyet-dinh-7
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1212", "claude:9514b261#L1237", "claude:9514b261#L1317"]
hook: "Bảy cặp quyết định thay thế nhau, năm cặp chỉ thay một phần"
tension: tuong_ma_hoa_ra
sides: ["ghi 'thay thế' tưởng là bỏ hẳn quyết định cũ", "5 trong 7 cặp chỉ thay một phần, vài cái chỉ nằm trong câu chữ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuỗi thay thế quyết định: 7 cặp có quan hệ, 5 cặp chỉ thay một phần, ít nhất 4 quyết định chỉ nêu trong câu chữ

**Bối cảnh:** Muốn dựng reducer tính quyết định hiệu lực, cần biết chuỗi supersession đã ghi đủ chưa.
**Chuyện gì xảy ra:** Em đếm trực tiếp trong log sự kiện: 36 quyết định D-ADR và 18 sự kiện supersedes. Bảy cặp nền có khoá khớp đúng bản ghi, nhưng 5 trong 7 quan hệ chỉ thay một phần. Ít nhất 4 quyết định thay một điều khoản chỉ nêu trong câu chữ, không có quan hệ ghi lại.
**Bài học:** Quan hệ thay thế cần ghi ở cấp điều khoản; quyết định mới nhất thắng là không an toàn khi quyết định mới chỉ thay một vế.
**Artefact:** Bảng ba cột: có quan hệ, chỉ thay một phần, chỉ có trong câu chữ. Không ghi id quyết định nếu nhạy cảm.
