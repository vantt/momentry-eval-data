---
id: 2026-10-09-commit-mang-tac-gia-la-mot
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965", "omp:cd4449ab#L3370", "omp:cd4449ab#L3959"]
hook: "Commit của tôi mang tên tác giả là một model AI khác"
tension: tuong_ma_hoa_ra
sides: ["Agent đang chạy là model này", "Lịch sử commit ghi tác giả gemini-3.8-flash"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit mang tác giả là một model AI khác

**Bối cảnh:** Các commit trong worktree này có tác giả hiển thị là một model AI khác.
**Chuyện gì xảy ra:** Output git commit ở các commit wave 3 hiện dòng Author là gemini-3.8-flash, trong khi agent đang chạy không phải model đó. Không có chủ ý đổi config git, nên tác giả phụ thuộc môi trường. Chuyện nhỏ nhưng dễ gây hiểu nhầm khi đọc lịch sử commit.
**Bài học:** Kiểm git config user trước khi commit trong môi trường agent, để lịch sử không gán nhầm tác giả.
**Artefact:** Dòng Author trong git log, che email nếu có.
