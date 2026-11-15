---
id: 2026-11-02-hook-pre-push-cua-upstream-chan
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L204", "claude:c4caee3c#L209", "claude:c4caee3c#L211"]
hook: "Hook của upstream chặn push; agent đặt HUSKY=0 cho mọi lệnh"
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

# Hook pre-push của upstream chặn push vì HUSKY chưa tắt

**Bối cảnh:** Commit đã vào nhưng git push bị hook husky của upstream chặn.
**Chuyện gì xảy ra:** Agent push lại với HUSKY=0 và từ đó đặt biến này cho mọi lệnh push. Lỗi vặt, sửa trong một lượt.
**Bài học:** Ghi rõ biến bỏ hook trong quy trình khi repo có hook chặn push.
**Artefact:** Không cần.
