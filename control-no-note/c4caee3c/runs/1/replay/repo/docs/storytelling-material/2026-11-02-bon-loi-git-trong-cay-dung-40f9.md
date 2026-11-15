---
id: 2026-11-02-bon-loi-git-trong-cay-dung-40f9
code: M-DFRS
aliases: [M-DFRS]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L800", "claude:c4caee3c#L1295", "claude:c4caee3c#L1314", "claude:c4caee3c#L2929", "claude:c4caee3c#L3520"]
hook: "Bốn lỗi git trong một cây dùng chung, vẫn chưa có bước kiểm"
tension: khac
sides: ["Mỗi lỗi đều được sửa ngay", "Vẫn chưa có bước kiểm git status trước khi đổi lịch sử"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bốn lỗi git trong cây dùng chung: pull, commit rỗng, merge bị huỷ, quoting

**Bối cảnh:** Nhiều agent và lead cùng làm trên một cây git, với nhiều thay đổi chưa commit.
**Chuyện gì xảy ra:** Pull --rebase bị từ chối vì còn thay đổi chưa commit. Một commit chỉ có file untracked nên thất bại. Merge bị huỷ vì cây còn thay đổi. Một lệnh git diff nhận chuỗi đường dẫn gộp làm 'pathspec không tồn tại'. Mỗi lần lead sửa bằng --autostash hoặc tách lệnh, nhưng chưa có bước kiểm git status trước mỗi lệnh đổi lịch sử.
**Bài học:** Đặt quy tắc chạy git status trước mỗi lệnh đổi lịch sử trong cây dùng chung.
