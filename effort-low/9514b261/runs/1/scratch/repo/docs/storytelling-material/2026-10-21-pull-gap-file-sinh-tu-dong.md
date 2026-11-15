---
id: 2026-10-21-pull-gap-file-sinh-tu-dong
date: 2026-10-21
repo: repo
status: raw
signals: ["gốc nhỏ, lỗi to", vòng lặp người với máy]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L692", "claude:9514b261#L710", "claude:9514b261#L722", "claude:9514b261#L1657", "claude:9514b261#L1675", "claude:9514b261#L1715"]
hook: "Pull xong, restore có thể xoá sạch phần sửa chưa commit của bạn"
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

# Pull gặp file sinh tự động xung đột, và restore làm mất sửa chưa commit

**Bối cảnh:** Repo có nhiều file dirty của người dùng, remote đi trước 28 đến 30 commit. Agent cần pull và rebase mà không mất việc của ai.
**Chuyện gì xảy ra:** Một digest file sinh tự động xung đột. Agent lấy bản remote vì nó được sinh lại, còn bản local giữ trong stash. Trước khi restore board, agent lưu patch vào scratchpad, rồi sau pull ghi lại các mục log theo đúng thứ tự thời gian.
**Bài học:** Lưu patch ra file trước khi restore hoặc reset. File sinh tự động thì lấy bản nguồn, không merge tay.
**Artefact:** Danh sách file dirty phân theo chủ (người dùng hay agent) và trạng thái sau pull.
