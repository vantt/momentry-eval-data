---
id: 2026-10-21-git-giua-luc-lam-remote-sua
date: 2026-10-21
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L692", "claude:9514b261#L710", "claude:9514b261#L722", "claude:9514b261#L1657", "claude:9514b261#L1675", "claude:9514b261#L1680", "claude:9514b261#L1760"]
hook: "Remote sửa board giữa lúc làm: lưu patch trước, rồi ba commit sạch được push"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Git giữa lúc làm: remote sửa board, lưu patch trước khi restore, digest sinh lại gây xung đột

**Bối cảnh:** Remote có commit mới trong lúc agent đang sửa board và plan, còn repo có nhiều file dirty của owner.
**Chuyện gì xảy ra:** Trước khi pull, remote đã đổi file board và file digest mutation-census. Agent lưu patch board trước khi restore, đưa thay đổi của owner vào stash và chọn bản remote cho file digest sinh tự động. Lần commit đầu lỗi pathspec vì thư mục plan chưa được track; em làm lại sau khi kiểm đường dẫn. Sau đó ba commit sạch được push.
**Bài học:** Lưu patch trước khi restore; với file sinh tự động, lấy bản sinh lại thay vì merge tay; kiểm đường dẫn đã được track trước khi commit bằng pathspec.
**Artefact:** Danh sách commit trước và sau khi rebase, không kèm hash nếu không cần.
