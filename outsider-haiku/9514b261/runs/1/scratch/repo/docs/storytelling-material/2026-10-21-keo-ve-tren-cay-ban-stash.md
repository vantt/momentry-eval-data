---
id: 2026-10-21-keo-ve-tren-cay-ban-stash
date: 2026-10-21
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L692", "claude:9514b261#L710", "claude:9514b261#L722", "claude:9514b261#L1675", "claude:9514b261#L1743", "claude:9514b261#L1765"]
hook: "Pull một lệnh, file tự sinh xung đột, bản của chủ nằm trong stash"
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

# Kéo về trên cây bẩn: stash, file sinh tự động xung đột, và ghi lại log

**Bối cảnh:** Nhiều phiên cùng sửa một repo. Remote đổi cả file log của board lẫn một file digest sinh tự động.
**Chuyện gì xảy ra:** Khi pull --rebase --autostash, file digest sinh tự động xung đột. Agent lấy bản remote vì bản local sinh từ nguồn cũ, còn bản của owner được giữ trong stash. Board đổi cấu trúc trên remote nên agent hoàn lại phần sửa, pull, rồi ghi lại các mục log theo thứ tự thời gian. Khi commit chỉ stage file của mình, một pathspec lỗi vì thư mục chưa được git theo dõi.
**Bài học:** Tách thay đổi của mình thành patch riêng trước khi pull. Ghi lại mục log bằng script theo mốc thời gian, không sửa tay.
**Artefact:** Sơ đồ ba commit với phạm vi file của từng commit.
