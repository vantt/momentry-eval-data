---
id: 2026-11-02-git-chan-bon-lan-pre-push
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L204", "claude:c4caee3c#L800", "claude:c4caee3c#L1295", "claude:c4caee3c#L2929"]
hook: "Git chặn agent bốn lần, lần nào cũng chỉ vì thay đổi chưa commit"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Git chặn bốn lần: pre-push hook, rebase, merge và commit rỗng

**Bối cảnh:** Repo fork có hook husky pre-push kế thừa từ upstream, và agent làm việc trên nhiều nhánh cùng lúc.
**Chuyện gì xảy ra:** Lần push đầu bị hook pre-push của upstream chặn, nên agent đặt HUSKY=0 cho lệnh push và từ đó áp dụng cho mọi lần push. Ba lỗi khác là pull --rebase khi còn thay đổi chưa commit, commit khi chỉ có file chưa theo dõi, và merge bị từ chối vì còn thay đổi. Mỗi lỗi đều được xử lý bằng cách commit hoặc stash trước rồi chạy lại.
**Bài học:** Bypass hook bằng biến môi trường nên ghi rõ trong plan, vì nó tắt kiểm tra cho cả lần push; thứ tự commit trước khi pull, merge là nguyên nhân phổ biến nhất.
**Artefact:** Thông báo lỗi git rút gọn. Không cần che.
