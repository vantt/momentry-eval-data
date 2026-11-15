---
id: 2026-10-30-hai-phien-cung-mot-repo-commit-f60d
code: M-8EXN
aliases: [M-8EXN]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L291", "claude:f0bf048d#L688", "claude:f0bf048d#L1152"]
hook: "Hai phiên cùng một repo: commit từng file, không đụng file dở"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai phiên cùng một repo: commit từng file, không đụng file đang dở

**Bối cảnh:** Một phiên khác đang làm song song trên cùng repo.
**Chuyện gì xảy ra:** Agent kiểm git status trước khi sửa, commit đúng các file của mình và để nguyên file của phiên kia. Có lần git add lỗi vì đường dẫn đã đổi, phải kiểm lại và amend. Phiên kia sau đó chuyển sang cài theo khách, khớp với mô hình mới.
**Bài học:** Với repo dùng chung giữa nhiều phiên, add theo tên file và kiểm git show --stat sau mỗi commit.
**Artefact:** Output git status trước và sau commit.
