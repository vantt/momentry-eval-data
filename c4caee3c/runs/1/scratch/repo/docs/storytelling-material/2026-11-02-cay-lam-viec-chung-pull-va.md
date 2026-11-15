---
id: 2026-11-02-cay-lam-viec-chung-pull-va
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L800", "claude:c4caee3c#L2929", "claude:c4caee3c#L2939"]
hook: "Nhánh sửa xong vẫn phải chờ vì agent khác chưa commit"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cây làm việc chung: pull và merge bị chặn bởi thay đổi dở của agent khác

**Bối cảnh:** Nhiều agent cùng ghi vào một cây repo chung.
**Chuyện gì xảy ra:** Lệnh pull --rebase và merge bị từ chối vì có thay đổi chưa commit của agent khác, cụ thể là file review-upstream. Nhánh vi-snippet-fix phải chờ thêm một vòng vì phải đợi agent kia commit trước.
**Bài học:** Mỗi agent đang sửa file chung nên có worktree riêng; đừng để chung một cây.
**Artefact:** Thông báo lỗi git đã rút gọn.
