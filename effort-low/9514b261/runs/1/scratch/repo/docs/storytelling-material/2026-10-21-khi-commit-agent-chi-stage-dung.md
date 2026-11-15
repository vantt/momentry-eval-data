---
id: 2026-10-21-khi-commit-agent-chi-stage-dung
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:9514b261#L1675", "claude:9514b261#L1687", "claude:9514b261#L1760", "claude:9514b261#L1772", "claude:9514b261#L3365", "claude:9514b261#L3383", "claude:9514b261#L3407"]
hook: "Commit chỉ đúng file mình sửa, không cuốn theo việc dở của bạn"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi commit, agent chỉ stage đúng các file do chính mình sửa bằng pathspec, giữ nguyên các thay đổi đang dở của người dùng (chưa commit), và kiểm trước xem remote có đụng file đó không rồi mới rebase hoặc push.

**Chuyện gì xảy ra:** Khi commit, agent chỉ stage đúng các file do chính mình sửa bằng pathspec, giữ nguyên các thay đổi đang dở của người dùng (chưa commit), và kiểm trước xem remote có đụng file đó không rồi mới rebase hoặc push.
**Góc người ngoài:** cách làm phổ biến là Thường dùng git add -A hoặc git stash cho tất cả, rồi commit gộp, dễ kéo theo thay đổi không liên quan; ở đây khác ở Lịch sử commit sạch và chỉ chứa phần của một việc, nên người khác đọc được và dễ hoàn tác từng commit.
