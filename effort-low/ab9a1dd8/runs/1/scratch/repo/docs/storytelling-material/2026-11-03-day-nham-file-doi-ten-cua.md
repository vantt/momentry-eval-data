---
id: 2026-11-03-day-nham-file-doi-ten-cua
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2769", "claude:ab9a1dd8#L2777"]
hook: "Đẩy một commit đổi tên lên main, CI đỏ toàn bộ vì thiếu README"
tension: nho_ma_to
sides: ["một file README tiếng Anh chưa commit", "main thiếu README, CI đỏ toàn bộ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đẩy nhầm file đổi tên của phiên khác lên main: CI đỏ toàn bộ

**Bối cảnh:** Một phiên làm việc khác đã stage sẵn việc đổi tên README.md thành README.vi.md trong cùng index. Commit của agent kéo theo cả thay đổi này.
**Chuyện gì xảy ra:** Commit e78f3ab đẩy lên main cả việc đổi tên, nhưng README.md tiếng Anh chưa được commit, nên main thiếu README và CI đỏ. Người dùng chọn commit README song ngữ đang có để sửa. CI xanh lại. Từ đó agent chỉ stage đúng file của mình và kiểm git diff --cached trước khi commit.
**Bài học:** Trước mỗi commit, kiểm git diff --cached để chắc index chỉ chứa file của mình; index dùng chung giữa các phiên dễ mang theo thay đổi lạ.
**Artefact:** Đoạn output git diff --cached --stat trước và sau khi sửa. Không cần che gì.
**Góc người ngoài:** cách làm phổ biến là Nhiều người dùng "git add -A" cho nhanh, dễ kéo theo file người khác đang sửa dở; ở đây khác ở Sau khi một commit vô tình kéo theo đổi tên README, agent rút ra quy tắc stage có chọn lọc và báo rõ phần nào đang bị phiên khác chạm, nên người đọc sẽ muốn áp dụng ngay.
