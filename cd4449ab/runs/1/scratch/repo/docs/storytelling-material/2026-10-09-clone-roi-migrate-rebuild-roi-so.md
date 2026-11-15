---
id: 2026-10-09-clone-roi-migrate-rebuild-roi-so
date: 2026-10-09
repo: repo
status: raw
signals: ["1", "6"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1679", "omp:cd4449ab#L1682", "omp:cd4449ab#L1828", "omp:cd4449ab#L1831", "omp:cd4449ab#L1870", "omp:cd4449ab#L1876", "omp:cd4449ab#L1879", "omp:cd4449ab#L1882", "omp:cd4449ab#L1885", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890", "omp:cd4449ab#L1891"]
hook: "So before/after trên hub thật, baseline phải rebuild về schema 2"
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

# Clone rồi migrate, rebuild rồi so sánh before/after bằng skill show --json

**Bối cảnh:** Kiểm tra migration trên bản clone, không chạm hub đang chạy.
**Chuyện gì xảy ra:** Agent clone hub vào thư mục tạm, build hai binary, main và nhánh hiện tại, rồi chạy skill show --json trước và sau cho 3 skill. Lần đầu fail vì pointer.json chưa tồn tại, nên phải rebuild về schema 2 để có baseline. Sau đó diff cho thấy name của test-audit giữ nguyên.
**Bài học:** Diff trước và sau trên bản clone bằng hai binary là cách rẻ nhất để bắt regression mà test không thấy.
**Artefact:** Bảng diff skill show trước và sau theo từng trường, che nội dung skill.
