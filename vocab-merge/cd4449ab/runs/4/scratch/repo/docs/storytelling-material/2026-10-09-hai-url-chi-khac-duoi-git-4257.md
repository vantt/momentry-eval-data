---
id: 2026-10-09-hai-url-chi-khac-duoi-git-4257
code: M-P4AV
aliases: [M-P4AV]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1594", "omp:cd4449ab#L1792", "omp:cd4449ab#L1794", "omp:cd4449ab#L1801", "omp:cd4449ab#L1803", "omp:cd4449ab#L1818", "omp:cd4449ab#L1822", "omp:cd4449ab#L1827"]
hook: "Hai URL chỉ khác đuôi '.git' bị coi là hai nguồn"
tension: nho_ma_to
sides: ["hai URL chỉ khác bốn ký tự .git", "hệ thống tưởng là hai nguồn khác nhau"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai URL chỉ khác đuôi .git bị coi là hai nguồn khác nhau

**Bối cảnh:** Khi gộp provenance.origin với Phase 0 sources, cần khớp theo repo. Upstream ghi URL có đuôi .git, file Phase 0 thì không.
**Chuyện gì xảy ra:** So sánh chuỗi thô cho ra matches=false dù hai URL cùng một repo. Thử normalize bằng Python thì cả hai bản cho cùng một giá trị. Viết normalizeRepoURL: bỏ khoảng trắng, dấu / cuối, đuôi .git, và hạ chữ host. Sau đó gộp thành một source với roles [upstream, learning], giữ cả commit lẫn learn_paths.
**Bài học:** Khóa so sánh nguồn phải được chuẩn hoá trước khi so; so chuỗi thô tạo bản sao trùng lặp mà không báo lỗi.
**Artefact:** Bảng ba cặp URL đầu vào và đầu ra sau normalize. Không ghi URL thật nếu nhạy cảm.
