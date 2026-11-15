---
id: 2026-10-21-file-digest-sinh-tu-dong-xung
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, git đảo hướng]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L692", "claude:9514b261#L710", "claude:9514b261#L722", "claude:9514b261#L902"]
hook: "File digest tự sinh có năm dấu xung đột: lấy bản remote, cất bản chủ vào stash"
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

# File digest sinh tự động xung đột khi pull: lấy bản đã sinh lại, giữ bản chủ trong stash

**Bối cảnh:** Agent pull remote có 92 commit mới trong khi cây làm việc có thay đổi chưa commit của chủ repo, dùng autostash.
**Chuyện gì xảy ra:** File mutation-census là digest sinh tự động và có năm dấu xung đột. Bản của chủ sinh từ nguồn cũ, bản remote đã sinh lại. Agent lấy bản remote và để bản của chủ trong stash, kèm lệnh xem và lệnh xoá nếu không cần.
**Bài học:** File sinh tự động không nên giữ bản sửa tay; sau pull hãy sinh lại thay vì giải xung đột bằng tay.
**Artefact:** Kết quả stash list với nhãn mô tả (không in nội dung).
