---
id: 2026-10-21-khi-commit-chi-stage-dung-file
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, outsider]
lines: ["claude:9514b261#L1675", "claude:9514b261#L1760", "claude:9514b261#L3396", "claude:9514b261#L3407"]
hook: "Một lệnh git add -A nuốt cả file đang dở của chủ repo"
tension: giup_ma_hai
sides: ["Commit nhanh bằng add -A cho tiện", "Kéo theo file dở của người khác"]
strength: 1
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi commit, chỉ stage đúng file của mình bằng pathspec, để yên các file đang dirty của chủ repo. Trước khi rebase, kiểm xem remote có đụng các file đó không.

**Chuyện gì xảy ra:** Khi commit, chỉ stage đúng file của mình bằng pathspec, để yên các file đang dirty của chủ repo. Trước khi rebase, kiểm xem remote có đụng các file đó không.
**Góc người ngoài:** cách làm phổ biến là Chạy `git add -A` hoặc `git commit -am`, rồi pull hoặc push mà không xem remote đổi gì; ở đây khác ở Người dùng nhận được các commit chỉ chứa phần việc của mình, còn thay đổi chưa commit của họ vẫn nguyên, không bị gộp vào. Người đọc làm nhiều việc trên một repo chung sẽ muốn cách này.
