---
id: 2026-10-09-checkpoint-agent-dung-cho-lead-merge-4257
code: M-EES8
aliases: [M-EES8]
date: 2026-10-09
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, rang_buoc_thiet_ke]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713", "omp:cd4449ab#L2025", "omp:cd4449ab#L2123", "omp:cd4449ab#L2345", "omp:cd4449ab#L2374"]
hook: "Ba vòng review, mỗi vòng agent sửa xong rồi dừng chờ"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Checkpoint: agent dừng chờ lead merge rồi mới làm Phase 3

**Bối cảnh:** Quy trình chia Phase 4 thành các checkpoint. Lead review và merge từng cái trước khi agent sang Phase 3.
**Chuyện gì xảy ra:** Có ba vòng review lớn cho Phase 4, mỗi vòng agent sửa rồi báo hash và dừng. Lead merge fast-forward sau checkpoint đã kiểm. Sau đó Phase 3 được chia thành ba commit a, b, c, mỗi commit có báo cáo riêng.
**Bài học:** Chia việc theo checkpoint giúp người review thấy rõ từng thay đổi. Điều kiện là mỗi lần dừng phải kèm hash và kết quả kiểm.
**Artefact:** Bảng hash của các checkpoint.
**Góc người ngoài:** cách làm phổ biến là Người dùng AI thường muốn agent làm xong hết trong một lượt, không chia nhịp duyệt; ở đây khác ở Phiên này chia công việc thành các mốc có hash và chờ duyệt. Điều này làm người đọc hiểu vì sao một việc lớn được chia nhỏ và ai là người quyết định merge.
