---
id: 2026-11-05-hub-bao-active-khi-ban-moi
date: 2026-11-05
repo: repo
status: raw
signals: [người duyệt, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:6a207191#L1331", "claude:6a207191#L1336", "claude:6a207191#L1479", "claude:6a207191#L1483", "claude:6a207191#L1489", "claude:6a207191#L1500", "claude:6a207191#L1503", "claude:6a207191#L1515"]
hook: "Hub báo 'active' trong khi ba bản mới nằm chờ, không ai thấy"
tension: cam_ma_van_lot
sides: ["Trang skill hiện trạng thái active, có vẻ ổn", "Ba bản gửi đang chờ duyệt ở nơi khác, không cảnh báo"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hub báo 'active' khi bản mới đang chờ: ba bản gửi cho một skill, trang skill không báo

**Bối cảnh:** Trong một buổi, agent gửi cùng một skill ba lần, mỗi lần thay thế bản trước. Người dùng hỏi sao hub đã để active khi chưa thấy ai duyệt.
**Chuyện gì xảy ra:** Agent so bản hub đang phục vụ với thư mục local: giống hệt, chỉ khác một dòng trống hub chèn sau frontmatter. Bản active là kết quả của một lần duyệt trước đó, không khớp với mã nào trong danh sách đã gửi. Trang skill trên web chỉ hiện bản active, còn bản chờ nằm riêng ở Waiting for review, nên không có cảnh báo nào.
**Bài học:** Trạng thái đang chạy và đang chờ của cùng một đối tượng phải hiện cùng nhau. Đừng để người duyệt tự đi tìm hàng chờ.
**Artefact:** Hai ảnh: trang skill (chỉ có active) và mục Waiting for review (bản chờ), đã che tên máy và mã gửi.
**Góc người ngoài:** cách làm phổ biến là Người dùng thường tin trạng thái hiển thị trên giao diện là bản mới nhất; ở đây khác ở Agent không tin trạng thái bề mặt mà so bằng diff và nguồn dữ liệu thật, nên phát hiện được bản đang dùng không phải bản vừa gửi. Người đọc sẽ muốn có thói quen này khi làm việc với hệ thống nhiều nguồn.
