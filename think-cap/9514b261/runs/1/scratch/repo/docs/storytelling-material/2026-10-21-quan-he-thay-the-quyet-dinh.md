---
id: 2026-10-21-quan-he-thay-the-quyet-dinh
date: 2026-10-21
repo: repo
status: raw
signals: [số trước/sau, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1116", "claude:9514b261#L1121", "claude:9514b261#L1212", "claude:9514b261#L1237"]
hook: "36 quyết định, chỉ 7 cặp thay thế được ghi trong dữ liệu"
tension: tuong_ma_hoa_ra
sides: ["Tưởng quan hệ thay thế đã nằm trong dữ liệu", "Chỉ 7/36 cặp ghi lại, số còn lại nằm trong câu chữ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quan hệ thay thế quyết định: 7 cặp ghi được, phần còn lại chỉ nằm trong câu chữ

**Bối cảnh:** Đề xuất kiến trúc có một reducer tính tập quyết định hiệu lực. Agent kiểm xem dữ liệu quan hệ thay thế đã đủ để reducer dùng chưa.
**Chuyện gì xảy ra:** Có 36 quyết định ADR, trong đó 7 cặp có quan hệ thay thế ghi trong dữ liệu. Năm trong bảy cặp chỉ thay một phần. Ít nhất 4 quyết định chỉ nói “thay thế” trong câu chữ và 1 đích thay thế không phải quyết định. Agent từng nói đề xuất “không nhắc state.decisions”, sau đó phải đính chính là đề xuất có ý nhập kho này vào.
**Bài học:** Quan hệ thay thế ở cấp quyết định không đủ khi thay đổi thường chỉ áp dụng cho một điều khoản; cần kiểm dữ liệu thật thay vì đếm theo tài liệu.
**Artefact:** Bảng 7 cặp (quyết định mới → quyết định cũ) với cột “thay toàn bộ hay một phần”, đánh số, không kèm nội dung quyết định.
