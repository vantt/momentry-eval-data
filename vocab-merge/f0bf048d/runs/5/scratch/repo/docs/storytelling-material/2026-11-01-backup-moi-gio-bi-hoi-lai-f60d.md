---
id: 2026-11-01-backup-moi-gio-bi-hoi-lai-f60d
code: M-ZN4M
aliases: [M-ZN4M]
date: 2026-11-01
repo: repo
status: raw
signals: [số trước/sau, đảo quyết định có lý do]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2582", "claude:f0bf048d#L2592", "claude:f0bf048d#L2593", "claude:f0bf048d#L2595"]
hook: "Backup mỗi giờ cho database 27 MB và uploads chỉ 4 KB"
tension: giup_ma_hai
sides: ["Backup dày cho yên tâm", "Dữ liệu bé tí, mỗi ngày một lần là đủ"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Backup mỗi giờ bị hỏi lại: database 27 MB, uploads gần rỗng

**Bối cảnh:** Kế hoạch ghi backup mỗi giờ cho an toàn; người vận hành hỏi vì sao nhiều quá.
**Chuyện gì xảy ra:** Đo thực tế: database 27 MB, thư mục uploads 4 KB. Lập luận lại theo câu hỏi mất tối đa bao nhiêu việc thay vì kích thước. Đề xuất: mỗi ngày một lần giữ 14 bản ngày và 8 bản tuần, cộng backup ngay trước thao tác rủi ro, chỉ chuyển sang mỗi giờ khi có khách trả tiền. Người vận hành tạm hoãn bước backup.
**Bài học:** Chọn tần suất backup theo lượng việc chấp nhận được mất, và thêm backup ngay trước thao tác rủi ro; kích thước dữ liệu chỉ là chi phí.
**Artefact:** Kết quả pg_size_pretty và du -sh của volume uploads.
