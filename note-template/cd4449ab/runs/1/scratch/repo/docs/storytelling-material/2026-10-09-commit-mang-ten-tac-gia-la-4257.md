---
id: 2026-10-09-commit-mang-ten-tac-gia-la-4257
code: M-75G0
aliases: [M-75G0]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
signal_note: "Commit mang tên tác giả là tên model thay vì tên người dùng, lịch sử git sai nếu không kiểm lại."
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965", "omp:cd4449ab#L3370", "omp:cd4449ab#L3959"]
hook: "4 commit ghi tác giả là tên model, không phải chủ dự án"
tension: nho_ma_to
sides: ["Git user của phiên là chủ dự án", "4 commit mang tên model, không ai thấy trước khi báo cáo"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit mang tên tác giả là model

**Bối cảnh:** Các commit tạo trong phiên có trường Author lấy từ cấu hình của worktree, không phải từ git user của chủ.
**Chuyện gì xảy ra:** Bốn commit (L2354, L2965, L3370, L3959) ghi Author là tên model, trong khi git user của phiên là chủ dự án. Không ai trong phiên nhận thấy trước khi báo cáo commit.
**Bài học:** Kiểm tra git config của worktree trước khi tạo chuỗi commit, và xem Author trong git log sau mỗi lần commit.
**Artefact:** Output git log --format có che email và tên.
