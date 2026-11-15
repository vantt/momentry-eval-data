---
id: 2026-10-25-doi-ten-42-anh-chup-theo-63a6
code: M-GPYM
aliases: [M-GPYM]
date: 2026-10-25
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c03"
sessions: ["claude:5a1e7c03"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c03#L2", "claude:5a1e7c03#L3", "claude:5a1e7c03#L4", "claude:5a1e7c03#L5", "claude:5a1e7c03#L6", "claude:5a1e7c03#L7", "claude:5a1e7c03#L8"]
hook: "Đổi tên 42 ảnh chỉ dựa vào lời hứa thứ tự khớp sổ"
tension: nho_ma_to
sides: ["Một giả định chưa kiểm tra, không thử vài tờ trước", "Nếu thứ tự lệch, cả 42 bài gắn nhầm tên học sinh"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi tên 42 ảnh chụp theo sổ lớp bằng script, chạy trước khi kiểm tra thứ tự

**Bối cảnh:** 42 bài scan là ảnh chụp điện thoại tên IMG_..., không đối chiếu được với sổ điểm. Giáo viên xác nhận đã chụp theo đúng thứ tự trong sổ.
**Chuyện gì xảy ra:** Agent dùng script đổi 42 file từ tên ảnh sang dạng số thứ tự và tên học sinh theo danh sách lớp, rồi báo đã xong. Việc đổi tên dựa hoàn toàn vào lời giáo viên rằng thứ tự chụp khớp sổ, và chưa có bước kiểm tra mẫu vài tờ trước khi đổi hàng loạt. Nếu thứ tự lệch, toàn bộ bài sẽ gắn nhầm tên.
**Bài học:** Với thao tác đổi tên hàng loạt có tính đối chiếu, mở thử 2–3 file đầu và cuối để xác nhận trước khi chạy cho cả lô.
**Artefact:** Danh sách tên file trước và sau đổi (che tên học sinh).
