---
id: 2026-10-29-stop-hook-ket-vong-lap-sau-c455
code: M-BCBY
aliases: [M-BCBY]
date: 2026-10-29
repo: repo
status: raw
signals: [lỗi quy trình, số]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2505", "claude:0faf0bb2#L2520", "claude:0faf0bb2#L2637", "claude:0faf0bb2#L2693", "claude:0faf0bb2#L2760"]
hook: "Bỏ mục tiêu rồi, hook vẫn chặn agent khoảng 20 lượt"
tension: cam_ma_van_lot
sides: ["Người dùng đã bỏ mục tiêu", "Hook cứ chặn 20 lượt, mô hình không có công cụ xoá goal"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Stop hook kẹt vòng lặp: sau khi người dùng bỏ mục tiêu, mô hình không tự xoá được goal

**Bối cảnh:** Mục tiêu đặt điều kiện trạng thái: một công ty mẫu phải còn tồn tại khi kết thúc phiên.
**Chuyện gì xảy ra:** Sau khi công ty mẫu bị xoá theo yêu cầu, stop hook tiếp tục chặn khoảng 20 lượt, mỗi lần đánh giá lại cùng một điều kiện. Mô hình không có công cụ để xoá goal và phải chờ người dùng gõ /goal clear. Agent đã gửi phản hồi về khả năng còn thiếu này. Cuối cùng người dùng trả lời bằng AskUserQuestion.
**Bài học:** Điều kiện dừng dạng trạng thái cần có lối thoát mà mô hình tự dùng được khi người dùng đổi ý.
**Artefact:** Chuỗi phản hồi hook lặp lại trong transcript. Không cần chụp.
