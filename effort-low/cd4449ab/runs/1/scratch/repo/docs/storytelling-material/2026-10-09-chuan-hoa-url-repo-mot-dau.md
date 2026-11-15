---
id: 2026-10-09-chuan-hoa-url-repo-mot-dau
date: 2026-10-09
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L1794", "omp:cd4449ab#L1801", "omp:cd4449ab#L1803", "omp:cd4449ab#L1818", "omp:cd4449ab#L1827"]
hook: "Thêm đúng 4 ký tự '.git', hai nguồn thành hai repo khác nhau"
tension: nho_ma_to
sides: ["một đuôi .git", "cùng repo bị coi là hai nguồn không khớp"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuẩn hoá URL repo: một dấu .git làm hai nguồn không khớp

**Bối cảnh:** Metadata có hai nguồn cùng một upstream: một bản ghi có đuôi .git, bản kia không. Migration cần gộp thành một source.
**Chuyện gì xảy ra:** Log debug in ra 'matches=false' với một URL có .git và một URL không. Sau khi viết hàm chuẩn hoá (bỏ khoảng trắng, dấu / cuối, đuôi .git, hạ chữ host), hai URL đều thành cùng một giá trị và test qua. Repo upstream đã được gộp thành một source với roles [upstream, learning].
**Bài học:** Khoá so sánh nguồn phải được chuẩn hoá trước khi so, đừng so chuỗi thô.
**Artefact:** Bảng hai URL thô và hai URL sau chuẩn hoá (đã che tên repo).
