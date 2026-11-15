---
id: 2026-11-01-backup-hourly-bi-hoi-lai-doi-f60d
code: M-2F87
aliases: [M-2F87]
date: 2026-11-01
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2582", "claude:f0bf048d#L2595", "claude:f0bf048d#L2601", "claude:f0bf048d#L2606"]
hook: "Backup mỗi giờ cho 27 MB dữ liệu: chắc ăn hay thừa?"
tension: chon_mot_mat_mot
sides: ["Mỗi ngày đã đủ cho database 27 MB", "Backup dày là thứ cho agent tự làm việc đảo ngược được mà không hỏi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Backup hourly bị hỏi lại: đổi từ chắc ăn sang agent tự làm được

**Bối cảnh:** Kế hoạch backup đề xuất mỗi giờ. Người vận hành hỏi tại sao nhiều thế.
**Chuyện gì xảy ra:** Database chỉ 27 MB, uploads gần như rỗng, restic chỉ thêm vài trăm KB mỗi lần. Agent đề xuất đổi thành mỗi ngày kèm backup ngay trước thao tác rủi ro, và chỉ mỗi giờ khi có khách trả tiền. Người vận hành hỏi lại mục tiêu có phải để chắc ăn không. Agent trả lời backup còn là thứ cho phép agent tự làm nhiều việc mà không phải hỏi, vì việc đảo ngược được thì agent tự làm được. Hiện tạm hoãn.
**Bài học:** Backup không chỉ để phòng sự cố mà còn quyết định việc nào agent được tự làm. Tần suất chỉ quyết định mất tối đa bao nhiêu việc.
**Artefact:** Kích thước database và uploads trước khi quyết định tần suất.
