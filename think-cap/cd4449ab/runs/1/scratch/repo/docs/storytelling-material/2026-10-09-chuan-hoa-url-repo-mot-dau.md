---
id: 2026-10-09-chuan-hoa-url-repo-mot-dau
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1794", "omp:cd4449ab#L1801", "omp:cd4449ab#L1803", "omp:cd4449ab#L1809", "omp:cd4449ab#L1812", "omp:cd4449ab#L1815", "omp:cd4449ab#L1818", "omp:cd4449ab#L1822", "omp:cd4449ab#L1827"]
hook: "Một dấu .git cuối URL biến một nguồn thành hai"
tension: nho_ma_to
sides: ["Hai URL trông giống hệt nhau", "Máy so chuỗi thô nên coi là hai nguồn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuẩn hoá URL repo: một dấu .git làm hai nguồn thành hai

**Bối cảnh:** Gộp source từ metadata cũ với source từ origin của cùng một repo trên GitHub.
**Chuyện gì xảy ra:** Dòng debug in matches=false cho hai URL giống nhau nhưng một bản có .git cuối. Hàm so sánh đang dùng chuỗi thô. Sau khi đưa về một hàm normalizeRepoURL (bỏ khoảng trắng, dấu / cuối, .git cuối, hạ chữ host), kiểm tra độc lập cho ra cùng một chuỗi và hai nguồn gộp thành một, giữ cả synced/commit lẫn learn_paths.
**Bài học:** Chuẩn hoá khóa so sánh ở một chỗ duy nhất và viết test với cả hai dạng có và không có .git.
**Artefact:** Dòng debug matches=false trước và sau, che URL.
