---
id: 2026-11-01-backup-theo-gio-hay-theo-ngay
date: 2026-11-01
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước số sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2582", "claude:f0bf048d#L2595", "claude:f0bf048d#L2601", "claude:f0bf048d#L2606"]
hook: "Database 27 MB, mỗi lần backup chỉ vài trăm KB, vậy backup để làm gì?"
tension: khac
sides: ["Dữ liệu bé tí, backup rẻ, tưởng để chống hỏng máy", "Thật ra để agent dám làm nhiều việc vì đảo ngược được"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Backup theo giờ hay theo ngày: quyết định theo câu hỏi mất tối đa bao nhiêu việc

**Bối cảnh:** Kế hoạch đầu viết backup mỗi giờ; chủ hỏi vì sao nhiều quá.
**Chuyện gì xảy ra:** Database chỉ 27 MB, uploads gần như rỗng, nên mỗi lần restic thêm vài trăm KB. Phiên đề xuất mỗi ngày một lần, giữ 14 bản ngày và 8 tuần, cộng backup ngay trước thao tác rủi ro. Giữa chừng chủ hỏi lại mục tiêu, và kết luận: backup để agent tự làm được nhiều việc đảo ngược được, không phải chỉ để chống sự cố máy.
**Bài học:** Tần suất backup là câu hỏi về lượng việc tối đa có thể mất; nhưng giá trị lớn nhất của backup là cho phép tự động hoá.
**Artefact:** Bảng 'rủi ro → mất tối đa bao nhiêu việc → tần suất'.
