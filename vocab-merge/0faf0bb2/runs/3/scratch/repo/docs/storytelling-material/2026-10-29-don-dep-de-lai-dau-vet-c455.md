---
id: 2026-10-29-don-dep-de-lai-dau-vet-c455
code: M-TWXN
aliases: [M-TWXN]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, lỗi quy trình]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:0faf0bb2#L2460", "claude:0faf0bb2#L2469", "claude:0faf0bb2#L2482", "claude:0faf0bb2#L2548", "claude:0faf0bb2#L2556", "claude:0faf0bb2#L2564", "claude:0faf0bb2#L2590", "claude:0faf0bb2#L2612", "claude:0faf0bb2#L2624"]
hook: "Xoá thư mục chính rồi, grep vẫn thấy 6 cache và 2 transcript ở bốn nơi"
tension: tuong_ma_hoa_ra
sides: ["Tưởng đã dọn sạch", "Còn dấu vết ở bốn nơi"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn dẹp để lại dấu vết ở bốn nơi: thư mục chính đã xoá, nhưng cache và index trong AICoworker vẫn còn

**Bối cảnh:** Sau khi gỡ CLI và xoá thư mục dữ liệu khoảng 2,4 GB, agent vẫn còn tìm thấy dấu vết ở chỗ khác.
**Chuyện gì xảy ra:** Lệnh uninstall chỉ gỡ CLI và giữ lại dữ liệu. Sau khi xoá thư mục chính, grep vẫn tìm thấy 6 file cache, 2 transcript đã đánh dấu xoá, và mục trong ba file index. Mỗi nơi cần một bước riêng. Chỉ khi quét lại toàn bộ thì kết quả mới sạch.
**Bài học:** Dọn một công cụ phải tìm theo tên trong toàn bộ thư mục dữ liệu, không chỉ xoá thư mục cài đặt.
**Artefact:** Kết quả grep theo tên công cụ trước và sau khi dọn. Đường dẫn đã che.
**Góc người ngoài:** cách làm phổ biến là Đa số người xoá thư mục cài đặt rồi thôi; dấu vết trong cache và file index thường còn lại mà không ai biết; ở đây khác ở Agent phát hiện 6 file cache và 3 file index còn giữ dấu vết của session đã xoá, và dọn nốt. Người đọc sẽ hỏi làm sao để không bỏ sót dữ liệu khi gỡ một công cụ.
