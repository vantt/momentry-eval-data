---
id: 2026-10-29-go-paperclip-xong-van-con-dau
date: 2026-10-29
repo: repo
status: raw
signals: [số trước/sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L2440", "claude:0faf0bb2#L2452", "claude:0faf0bb2#L2460", "claude:0faf0bb2#L2469", "claude:0faf0bb2#L2556", "claude:0faf0bb2#L2572", "claude:0faf0bb2#L2590", "claude:0faf0bb2#L2612", "claude:0faf0bb2#L2624"]
hook: "Gỡ Paperclip rồi, nhưng 4 chỗ trong agent vẫn nhớ nó; quét 3 lần mới sạch"
tension: cam_ma_van_lot
sides: ["Đã xoá CLI và thư mục dữ liệu", "Dấu vết vẫn nằm trong transcript, index và cache, phải quét 3 lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gỡ Paperclip xong vẫn còn dấu vết trong 4 chỗ của agent, phải quét 3 lần mới sạch

**Bối cảnh:** Dọn sau spike Paperclip, sau khi đã gỡ CLI và xoá ~/.paperclip (khoảng 2,4 GB).
**Chuyện gì xảy ra:** Lần quét đầu chỉ thấy CLI và thư mục dữ liệu. Sau đó phát hiện 2 transcript phiên đã xoá còn trong thư mục sessions, 2 mục trong index sessions.deleted.json, 2 mục trong system-prompt-reports.json, 3 mục trong advisor-sessions.json, và 6 file cache. Sau khi dọn từng chỗ, grep -ri trên thư mục state của agent không còn kết quả.
**Bài học:** Agent giữ lịch sử ở nhiều index phụ; sau khi xoá phiên, phải grep toàn bộ thư mục state chứ không chỉ xoá file chính.
**Artefact:** Kết quả grep trả về rỗng sau khi dọn.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ xóa thư mục cài đặt chính, để sót cache, session và file phụ; ở đây khác ở Phiên này phát hiện sót dấu vết ở 4 chỗ khác (session đã xóa, system-prompt-reports, advisor-sessions, cache capture) và chỉ dừng khi grep sạch; người đọc muốn có checklist để không sót khi tự gỡ công cụ.
