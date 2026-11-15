---
id: 2026-11-02-do-tren-vault-that-ma-khong
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, Artefact nhìn được]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2644", "claude:c4caee3c#L2656", "claude:c4caee3c#L3633", "claude:c4caee3c#L3653", "claude:c4caee3c#L3816", "claude:c4caee3c#L3842"]
hook: "Đo trên vault thật: tổng tăng 0,600 lên 0,698 nhưng vi-iy tụt 0,260"
tension: hop_ma_tan
sides: ["điểm tổng tăng từ 0,600 lên 0,698", "vi-iy tụt 0,260, vi-synonym tụt 0,167"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đo trên vault thật mà không đưa nội dung vault ra repo

**Bối cảnh:** Golden set 61 câu và vault thật nằm trên máy người dùng. Repo chỉ được giữ số tổng hợp.
**Chuyện gì xảy ra:** Chế độ chi tiết ghi file quyền 0600 ngoài repo, script từ chối nếu đường dẫn nằm trong repo hoặc đi qua symlink. Kết quả tổng: nDCG@5 từ 0,600 lên 0,698. Hạng mục vi-iy tụt 0,260 vì một câu rơi khỏi top 5, vi-synonym tụt 0,167 vì vault chưa có lexicon. Người duyệt chọn dùng gói cho bộ cài và sửa các hạng mục tụt.
**Bài học:** Thiết kế đo riêng tư ngay từ đầu: script từ chối ghi vào repo và chỉ in số tổng hợp.
**Artefact:** Bảng hạng mục tổng hợp, không có câu hỏi hay tên note.
