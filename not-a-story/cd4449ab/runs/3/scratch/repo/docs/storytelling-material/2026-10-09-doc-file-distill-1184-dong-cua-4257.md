---
id: 2026-10-09-doc-file-distill-1184-dong-cua-4257
code: M-YTC6
aliases: [M-YTC6]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke, artefact_nhin_duoc]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["omp:cd4449ab#L2414", "omp:cd4449ab#L2416", "omp:cd4449ab#L2456", "omp:cd4449ab#L2458", "omp:cd4449ab#L2461", "omp:cd4449ab#L2489", "omp:cd4449ab#L2513", "omp:cd4449ab#L2515", "omp:cd4449ab#L2527"]
hook: "77 hash rút gọn phải nở thành đủ 40 ký tự"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc file distill 1184 dòng của hub thật: 77 hash rút gọn cần nở ra đầy đủ

**Bối cảnh:** Để chứng minh migration distill chạy được, cần đọc file distill thật của hub ở chế độ chỉ đọc. File có 1184 dòng, 42 lesson và cursor của hai nguồn.
**Chuyện gì xảy ra:** Đếm được 77 mục commit rút gọn. Mỗi hash rút gọn phải nở ra bằng git rev-parse trên mirror, ví dụ một hash ngắn ra đúng 40 ký tự. Phân loại cho thấy 39 lesson đang ở trạng thái candidate và 3 ở trạng thái planned. Độ phủ của một nguồn là 15 mục đã đọc và 7 chưa đọc, nguồn kia là 6 và 4.
**Bài học:** Hash rút gọn không đủ để định danh chắc chắn, nên hãy nở ra đầy đủ trước khi dùng làm bằng chứng.
**Artefact:** Bảng đếm lesson theo trạng thái và số hash đã nở.
**Góc người ngoài:** cách làm phổ biến là Dev thường viết migration theo schema đã thiết kế, rồi chỉ thử bằng fixture giả; ở đây khác ở Đọc dữ liệu thật trước giúp phát hiện các dạng không khớp thiết kế (77 hash rút gọn, block scalar), nên người đọc hiểu vì sao fixture phải là bản sao byte-for-byte.
