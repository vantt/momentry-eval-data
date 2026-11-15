---
id: 2026-11-03-push-bi-tu-choi-doc-commit-d5ef
code: M-T3KQ
aliases: [M-T3KQ]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Quy trình an toàn khi remote có commit không có ở máy: đọc trước, rebase, không force."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2282", "claude:ab9a1dd8#L2288", "claude:ab9a1dd8#L2290", "claude:ab9a1dd8#L2300", "claude:ab9a1dd8#L2305"]
hook: "Push bị từ chối: agent đọc commit lạ trước, không force"
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

# Push bị từ chối: đọc commit lạ rồi rebase, không force

**Bối cảnh:** Push lên main bị từ chối vì GitHub có hai commit tài liệu đặt tên mà máy chưa có.
**Chuyện gì xảy ra:** Agent đọc diff của hai commit lạ trước, không force, rồi rebase ba commit của mình lên trên. Sau rebase chạy lại 230 test qua, rồi push thành công.
**Bài học:** Khi push bị từ chối, xem commit lạ trước; nếu rebase sạch thì không cần force.
