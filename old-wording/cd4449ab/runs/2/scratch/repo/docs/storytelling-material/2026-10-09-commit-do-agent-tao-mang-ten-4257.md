---
id: 2026-10-09-commit-do-agent-tao-mang-ten-4257
code: M-3JTF
aliases: [M-3JTF]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965", "omp:cd4449ab#L3370", "omp:cd4449ab#L3959"]
hook: "Commit của agent mang tên model, không phải tên chủ repo"
tension: nho_ma_to
sides: ["commit trông bình thường, test xanh", "git log lộ tác giả là tên model, chưa rõ nguyên nhân"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit do agent tạo mang tên tác giả khác với chủ repo

**Bối cảnh:** Repo dùng danh tính commit của chủ dự án. Các commit do agent tạo trong worktree lại ghi tác giả là tên một model.
**Chuyện gì xảy ra:** Một số commit, gồm checkpoint Phase 4 lần hai, migration v4, và commit xoá revision package, có tác giả là tên model thay vì chủ repo. Lỗi này chỉ lộ ra khi đọc git log có tác giả. Nguyên nhân chưa được kiểm trong phiên.
**Bài học:** Sau mỗi đợt commit tự động, hãy kiểm tác giả bằng git log. Đừng giả định cấu hình danh tính đang đúng.
**Artefact:** Đầu ra git log có tác giả, che tên người.
