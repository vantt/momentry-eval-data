---
id: 2026-10-31-daemon-ops-tat-ma-ke-hoach-f60d
code: M-WEY4
aliases: [M-WEY4]
date: 2026-10-31
repo: repo
status: raw
signals: [đảo quyết định có lý do, nguyên nhân gốc nhỏ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1987", "claude:f0bf048d#L3221", "claude:f0bf048d#L3237"]
hook: "Kế hoạch có hai điều kiện bật lại daemon, cái nào cũng đúng"
tension: khac
sides: ["Bật lại khi xong bước 4", "Bật lại khi operator rời user vantt"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Daemon ops tắt mà kế hoạch có hai điều kiện bật lại mâu thuẫn

**Bối cảnh:** Người dùng hỏi vì sao daemon ops chưa bật lại dù bước 4 đã xong.
**Chuyện gì xảy ra:** Kế hoạch ghi hai điều kiện: giai đoạn 0 bước 2 nói đến khi xong bước 4, giai đoạn 2 bước 7 nói khi System Operator đã ra khỏi user vantt. Daemon đang ở trạng thái disabled; bật được bằng một lệnh không cần sudo, nhưng là chấp nhận rủi ro. Unit của spike là transient nên không bật lại được bằng lệnh.
**Bài học:** Mỗi bước dừng và bật lại trong kế hoạch chỉ nên có đúng một điều kiện; hai điều kiện là dấu hiệu chưa nghĩ kỹ.
**Artefact:** Bảng trạng thái các giai đoạn.
