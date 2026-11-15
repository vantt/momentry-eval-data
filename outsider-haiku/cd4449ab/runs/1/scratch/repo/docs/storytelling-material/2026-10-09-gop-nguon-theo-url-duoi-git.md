---
id: 2026-10-09-gop-nguon-theo-url-duoi-git
date: 2026-10-09
repo: repo
status: raw
signals: ["2"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1792", "omp:cd4449ab#L1801", "omp:cd4449ab#L1803", "omp:cd4449ab#L1815", "omp:cd4449ab#L1818", "omp:cd4449ab#L1822", "omp:cd4449ab#L1827"]
hook: "Hai URL chỉ khác đuôi .git bị coi là hai nguồn khác nhau"
tension: nho_ma_to
sides: ["khác nhau đúng 4 ký tự .git", "một nguồn bị tách thành hai dòng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gộp nguồn theo URL: đuôi .git và dấu / cuối làm hai dòng thành một nguồn

**Bối cảnh:** Migration phải gộp hai nguồn cùng một repo: một từ provenance.origin và một từ sources của Phase 0.
**Chuyện gì xảy ra:** Hai URL khác nhau chỉ ở đuôi .git. Log debug cho thấy matches=false. Agent kiểm chuẩn hoá bằng hai cách, hàm Go và script Python, và cả hai ra cùng một chuỗi. Sau khi sửa normalizeRepoURL để trim khoảng trắng và đuôi, hai entry thành một source với roles [upstream, learning], giữ commit và learn_paths.
**Bài học:** Khoá so sánh phải được chuẩn hoá ở cả hai vế trước khi so; khi debug, in ra chính khoá đang được so.
**Artefact:** Bảng hai URL đầu vào và một source đầu ra. Che tên repo nếu là nội bộ.
