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
hook: "Commit của tôi mang tên model, không phải tên tôi"
tension: khac
sides: ["Repo của chủ dự án, commit do agent làm hộ", "Tác giả ghi là tên model, chưa rõ vì sao"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Dự án mcp-skill-hub; một agent làm trong worktree riêng để hoàn tất Phase 4 rồi rebase lên main.
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Commit thay đổi, rebase lên main và chạy make check xanh."
spine_want_lines: ["omp:cd4449ab#L2345"]
spine_obstacle: Main đã đi trước; cần rebase lên main.
spine_obstacle_lines: ["omp:cd4449ab#L2345"]
spine_action: Commit các thay đổi trong worktree bằng git commit -m.
spine_action_lines: ["omp:cd4449ab#L2352", "omp:cd4449ab#L2963", "omp:cd4449ab#L3368", "omp:cd4449ab#L3957"]
spine_outcome: Các commit trong worktree mang tác giả là tên một model; commit trên main mang tên chủ repo. Nguyên nhân chưa kiểm.
spine_outcome_lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2357", "omp:cd4449ab#L3370", "omp:cd4449ab#L3959"]
completeness: 5
---

# Commit do agent tạo mang tên tác giả khác với chủ repo

**Bối cảnh:** Repo dùng danh tính commit của chủ dự án. Các commit do agent tạo trong worktree lại ghi tác giả là tên một model.
**Chuyện gì xảy ra:** Một số commit, gồm checkpoint Phase 4 lần hai, migration v4, và commit xoá revision package, có tác giả là tên model thay vì chủ repo. Lỗi này chỉ lộ ra khi đọc git log có tác giả. Nguyên nhân chưa được kiểm trong phiên.
**Bài học:** Sau mỗi đợt commit tự động, hãy kiểm tác giả bằng git log. Đừng giả định cấu hình danh tính đang đúng.
**Artefact:** Đầu ra git log có tác giả, che tên người.
