---
id: 2026-10-29-goal-khong-tat-duoc-stop-hook
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L2505", "claude:0faf0bb2#L2513", "claude:0faf0bb2#L2521", "claude:0faf0bb2#L2533", "claude:0faf0bb2#L2637", "claude:0faf0bb2#L2685", "claude:0faf0bb2#L2693", "claude:0faf0bb2#L2716", "claude:0faf0bb2#L2760"]
hook: "Tôi bảo bỏ goal, hook vẫn chặn khoảng 20 lần vì agent không có nút xoá"
tension: cam_ma_van_lot
sides: ["Người dùng đã bảo bỏ goal, agent đã dọn hết", "Hook vẫn chặn ~20 lần, chỉ người dùng gõ /goal clear mới dừng"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# /goal không tắt được: stop hook lặp khoảng 20 lần sau khi người dùng bảo bỏ

**Bối cảnh:** Phiên đặt goal 'thử paperclip, setup sample company' dưới dạng stop hook: không cho dừng cho tới khi điều kiện đúng.
**Chuyện gì xảy ra:** Điều kiện được hook đánh giá như trạng thái phải còn đúng khi kết thúc. Sau khi người dùng trả lời 'bỏ goal, dọn hết paperclip', agent đã gỡ mọi thứ, nhưng hook vẫn chặn khoảng 20 lần vì agent không có công cụ để xoá goal; chỉ người dùng gõ /goal clear. Agent cũng gửi feedback về lỗi này qua công cụ của skill.
**Bài học:** Đừng viết goal dạng 'trạng thái phải còn đúng' cùng lúc cho phép dọn dẹp; viết điều kiện là sự kiện đã xảy ra, hoặc cho agent công cụ tự huỷ goal.
**Artefact:** Chuỗi thông báo 'Stop hook feedback' lặp lại, có thể chụp một đoạn để minh hoạ vòng lặp.
