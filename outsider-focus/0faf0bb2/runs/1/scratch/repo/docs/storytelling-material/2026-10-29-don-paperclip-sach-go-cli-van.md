---
id: 2026-10-29-don-paperclip-sach-go-cli-van
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, khác]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L2418", "claude:0faf0bb2#L2460", "claude:0faf0bb2#L2469", "claude:0faf0bb2#L2504", "claude:0faf0bb2#L2556", "claude:0faf0bb2#L2572", "claude:0faf0bb2#L2590", "claude:0faf0bb2#L2612", "claude:0faf0bb2#L2624"]
hook: "Gỡ CLI, xoá ~/.paperclip xong vẫn còn 6 file cache"
tension: cam_ma_van_lot
sides: ["Đã gỡ CLI và xoá thư mục cấu hình", "Cache, transcript và file index vẫn còn sót"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dọn Paperclip sạch: gỡ CLI vẫn để lại transcript, cache và file index

**Bối cảnh:** Người dùng yêu cầu dọn hết Paperclip sau spike. Lần đầu quét thấy đã xoá thư mục dữ liệu 2,4 GB nhưng chưa sạch.
**Chuyện gì xảy ra:** Gỡ CLI và xoá ~/.paperclip xong, lần quét thứ hai còn 6 file cache trong context-captures và keepalive-captures. Thêm nữa, hai transcript đã xoá nằm trong thùng rác dạng *.jsonl.deleted, cùng mục trong ba file index của AICoworker. Mình xoá nốt và quét lại đến khi grep không còn kết quả nào.
**Bài học:** Dọn một hệ thống đã chạy cần lập bảng hoàn tác ngay từ lúc cài, rồi quét lại sau khi dọn vì dữ liệu phụ như cache và transcript thường còn sót.
**Artefact:** Kết quả grep trước và sau khi dọn, đếm file còn sót.
**Góc người ngoài:** cách làm phổ biến là Dev thử công cụ xong thường gỡ qua uninstall, hoặc bỏ đó. Ít ai ghi lại để người khác làm lại được, và lúc dọn thì không biết còn sót gì; ở đây khác ở Người đọc hay cài thử công cụ AI rồi để lại rác hoặc thay đổi cấu hình khó nhớ. Cách này cho phép làm lại thí nghiệm trong khoảng 15 phút và dọn sạch có kiểm chứng. Phiên cho thấy uninstall chưa đủ: session đã xoá vẫn nằm trong thùng rác và cache.
