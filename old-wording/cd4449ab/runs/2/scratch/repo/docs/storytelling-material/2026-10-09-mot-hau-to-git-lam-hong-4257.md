---
id: 2026-10-09-mot-hau-to-git-lam-hong-4257
code: M-2D0H
aliases: [M-2D0H]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1627", "omp:cd4449ab#L1794", "omp:cd4449ab#L1803", "omp:cd4449ab#L1815", "omp:cd4449ab#L1845"]
hook: "Hai URL chỉ khác đuôi .git, nguồn vẫn không gộp được"
tension: nho_ma_to
sides: ["hai URL trỏ cùng một repo", "đuôi .git khiến matches=false, nguồn không gộp"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một hậu tố .git làm hỏng việc gộp nguồn; key repo và repository lệch nhau

**Bối cảnh:** File Phase 0 dùng key repo trong sources, còn schema v3 chỉ nhận repository. Cùng một repo lại xuất hiện lúc có .git, lúc không.
**Chuyện gì xảy ra:** Test migration báo 'invalid source entry: unknown field repo'. Sau khi sửa key, việc gộp nguồn vẫn không khớp: debug in ra matches=false cho hai URL chỉ khác đuôi .git. Hàm chuẩn hoá bỏ .git và dấu / cuối rồi đưa host về chữ thường, sau đó hai URL cho cùng kết quả và nguồn được gộp thành một với hai role.
**Bài học:** Khoá so sánh định danh như URL phải có hàm chuẩn hoá riêng và có test cho biến thể .git, đừng so chuỗi thô.
**Artefact:** Bảng ba dòng: URL gốc, URL đã chuẩn hoá, kết quả so khớp.
