---
id: 2026-11-02-git-va-husky-push-bi-chan-40f9
code: M-MMK0
aliases: [M-MMK0]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L204", "claude:c4caee3c#L209", "claude:c4caee3c#L800", "claude:c4caee3c#L1314", "claude:c4caee3c#L2929", "claude:c4caee3c#L3520"]
hook: "Husky chặn push, cây làm việc dơ chặn pull và merge"
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

# Git và husky: push bị chặn, pull và merge từ chối vì cây làm việc dơ

**Bối cảnh:** Repo fork kế thừa husky pre-push hook của upstream. Nhiều agent cùng làm nên cây làm việc thường có thay đổi chưa commit.
**Chuyện gì xảy ra:** Push đầu tiên thất bại vì hook, agent đặt HUSKY=0 cho lệnh push. Pull --rebase bị từ chối khi có thay đổi chưa commit, sửa bằng --autostash. Merge bị từ chối vì cây dơ, phải commit trước. Một lệnh git nhận nhiều đường dẫn gộp trong một chuỗi gây lỗi pathspec.
**Bài học:** Bỏ qua hook là quyết định có ý thức và phải ghi rõ; luôn dùng pull --rebase --autostash và truyền đường dẫn dạng mảng khi chạy nhiều agent.
