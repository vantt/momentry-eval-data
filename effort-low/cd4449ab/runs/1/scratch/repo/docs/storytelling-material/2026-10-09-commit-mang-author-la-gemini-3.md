---
id: 2026-10-09-commit-mang-author-la-gemini-3
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2354", "omp:cd4449ab#L2965"]
hook: "Repo của tôi, nhưng commit ghi tên 'gemini-3.8-flash'"
tension: tuong_ma_hoa_ra
sides: ["cấu hình author do chính người dùng đặt", "git log hiện tác giả là một model lạ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit mang author lạ 'gemini-3.8-flash'

**Bối cảnh:** Các commit do agent tạo có trường author không phải tài khoản của người dùng.
**Chuyện gì xảy ra:** Hai commit Phase 4 và Phase 3 hiển thị author 'gemini-3.8-flash' trong git log, dù cấu hình repo do người dùng đặt. Đây là chi tiết dễ bỏ qua khi duyệt commit nhưng ảnh hưởng đến truy vết.
**Bài học:** Kiểm tra git config của worktree trước khi để agent commit, để author đúng với người chịu trách nhiệm.
**Artefact:** Đầu ra git log --format cho các commit có author sai (che email).
