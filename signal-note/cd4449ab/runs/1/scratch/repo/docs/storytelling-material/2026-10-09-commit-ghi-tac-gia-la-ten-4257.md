---
id: 2026-10-09-commit-ghi-tac-gia-la-ten-4257
code: M-2KP6
aliases: [M-2KP6]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Tác giả commit hiển thị tên một model AI, không phải người điều phối; đáng nói về cách git ghi nhận công việc của agent."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2963", "omp:cd4449ab#L2965", "omp:cd4449ab#L3368", "omp:cd4449ab#L3370", "omp:cd4449ab#L3957", "omp:cd4449ab#L3959"]
hook: "Cả lịch sử commit Phase 3 đứng tên một model"
tension: khac
sides: ["code đúng, test xanh", "git log không cho biết ai làm gì"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit ghi tác giả là tên model

**Bối cảnh:** Các commit do agent tạo mang tác giả là một tên model, trong khi các commit khác trên nhánh mang tên người dùng.
**Chuyện gì xảy ra:** Git log của các commit Phase 3 ghi tác giả là một tên model. Đây không phải lỗi code, nhưng làm lịch sử khó đọc: ai làm gì không rõ. Cần quyết định có đặt git user riêng cho worktree hay không.
**Bài học:** Đặt git user rõ cho từng worktree hoặc agent để lịch sử nói đúng ai làm gì.
**Artefact:** Đoạn git log có tác giả, che email.
