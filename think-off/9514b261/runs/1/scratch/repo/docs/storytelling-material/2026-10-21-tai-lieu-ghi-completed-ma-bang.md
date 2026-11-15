---
id: 2026-10-21-tai-lieu-ghi-completed-ma-bang
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1402", "claude:9514b261#L1417"]
hook: "Plan ghi phase 12 đã xong, nhưng file spec nó trỏ tới không tồn tại"
tension: tuong_ma_hoa_ra
sides: ["plan ghi phase 12 completed", "spec không tồn tại, quy tắc cũ vẫn còn nguyên"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tài liệu ghi completed mà bằng chứng không khớp: phase 12 trỏ tới spec không tồn tại

**Bối cảnh:** Plan 260825 đã lưu trữ, và plan 260925 vẫn trỏ tới đường dẫn cũ.
**Chuyện gì xảy ra:** Plan 260825 ghi phase 12 là completed, nhưng file spec knowledge không tồn tại và tài liệu enduser vẫn giữ quy tắc R4 và R5. Chỉ phần deprecated của lệnh compound là có thật. Con trỏ trong plan 260925 thành con trỏ chết sau khi lưu trữ.
**Bài học:** Đánh dấu completed phải kèm bằng chứng kiểm được; sau khi lưu trữ, kiểm lại mọi con trỏ.
**Artefact:** Bảng ba dòng: trạng thái ghi, bằng chứng tìm thấy, bằng chứng thiếu.
**Góc người ngoài:** cách làm phổ biến là Tin dòng 'completed' hoặc 'done' trong tài liệu kế hoạch; ở đây khác ở Người đọc sẽ muốn có cách phát hiện sớm kế hoạch ghi xong mà bằng chứng không khớp. Phiên này phát hiện được một phase ghi hoàn thành nhưng spec không tồn tại.
