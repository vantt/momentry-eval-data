---
id: 2026-11-02-mot-claude-code-agent-day-ca
date: 2026-11-02
repo: repo
status: raw
signals: [artefact, khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L477", "claude:2dfb5915#L1341", "claude:2dfb5915#L2147", "claude:2dfb5915#L2157", "claude:2dfb5915#L2801"]
hook: "17 phase Rust lên main với CI xanh, rồi hook chặn dừng hàng chục lần"
tension: hop_ma_tan
sides: ["17 phase port xong, parity 64/64, CI xanh", "hook chặn dừng hàng chục lần dù không còn việc làm được"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một Claude Code agent đẩy cả plan Rust lên `main` với CI xanh, rồi hook dừng không chịu cho dừng

**Bối cảnh:** Người dùng giao một mục tiêu lớn (hoàn tất plan port core sang Rust), bật các agent làm song song, mỗi mục xong thì update plan, commit, push. Hook `/goal` chặn dừng cho tới khi toàn bộ plan xong.
**Chuyện gì xảy ra:** Chỉ trong một phiên, các agent con port được 17 phase với 7 phase chạy song song trong các worktree riêng; mỗi lượt merge phải chạy parity so với bản Python và CI ba nền. Parity đạt 64/64 mục, 0 lệch trên bộ vault thử. Bản cài đầu (rc.1) được phát hành sau khi sửa các lỗi review tìm ra. Sau đó phần còn lại của plan nằm sau cổng do người dùng mở (kiểm trên Windows, một tuần dùng song song), nên hook chặn dừng hàng chục lần với cùng một lý do dù agent đã nói rõ không còn việc làm được trên máy.
**Bài học:** Đặt điều kiện hoàn tất của hook trùng với phạm vi thật sự còn làm được, nếu không agent sẽ bị kẹt trong vòng lặp báo cáo lặp lại.
**Artefact:** Bảng trạng thái phase (01–17) và bảng 64 mục parity. Che đường dẫn vault, tên note và câu hỏi golden set.
**Góc người ngoài:** cách làm phổ biến là Hoặc dừng lại, hoặc tự cắt xén mục tiêu cho đủ điều kiện, hoặc bịa việc để hook im; ở đây khác ở Cho thấy cách xử lý một ràng buộc không thoả được. Giữ nguyên mục tiêu, nói thẳng chặn ở đâu và ai mở được, rồi đợi người dùng sửa goal. Người đọc dùng goal dài hạn sẽ muốn biết cách này.
