---
id: 2026-10-29-stop-hook-giu-goal-song-khoang-c455
code: M-5V42
aliases: [M-5V42]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2505", "claude:0faf0bb2#L2512", "claude:0faf0bb2#L2520", "claude:0faf0bb2#L2625", "claude:0faf0bb2#L2637", "claude:0faf0bb2#L2693", "claude:0faf0bb2#L2703", "claude:0faf0bb2#L2743", "claude:0faf0bb2#L2760"]
hook: "Chủ bảo bỏ goal, nhưng hook vẫn chặn dừng suốt 20 lượt"
tension: cam_ma_van_lot
sides: ["Chủ đã bảo bỏ goal", "Hook vẫn giữ goal sống khoảng 20 lượt"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook giữ goal sống khoảng 20 lượt sau khi chủ bảo bỏ

**Bối cảnh:** Goal 'setup một sample opc company' gắn stop hook của phiên. Sau đó chủ yêu cầu dọn Paperclip.
**Chuyện gì xảy ra:** Hook đánh giá điều kiện như một trạng thái phải còn đúng khi kết thúc phiên, nên khoảng 20 lượt phản hồi lặp lại đã chặn việc dừng. Agent không có lệnh để xoá goal, chỉ chờ chủ gõ /goal clear; một feedback loại missing_capability được xếp vào hàng đợi cục bộ.
**Bài học:** Điều kiện của goal nên là một kết quả kiểm được, và cần có cách thoát khi chủ đổi ý.
**Artefact:** Đoạn feedback đã rút gọn.
