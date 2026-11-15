---
id: 2026-11-02-dung-hay-tiep-tuc-hook-goal-3c6e
code: M-3J03
aliases: [M-3J03]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L2147", "claude:2dfb5915#L2157", "claude:2dfb5915#L2539", "claude:2dfb5915#L2549", "claude:2dfb5915#L2562", "claude:2dfb5915#L2581", "claude:2dfb5915#L2602", "claude:2dfb5915#L2633", "claude:2dfb5915#L2680", "claude:2dfb5915#L2803", "claude:2dfb5915#L2858"]
hook: "Hook chặn agent dừng hơn chục lần, lần nào cũng cùng một lý do"
tension: giup_ma_hai
sides: ["Hook chặn dừng để agent làm cho xong việc", "Agent chỉ lặp lại câu 'chờ anh' và kiểm git fetch vô ích"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dừng hay tiếp tục: hook 'goal' chặn phiên bảy lần liên tiếp bằng cùng một lý do

**Bối cảnh:** Người dùng đặt mục tiêu hoàn tất toàn bộ plan, sau đó thu hẹp phạm vi xuống 'tới khi cài được'. Hook dừng phiên vẫn yêu cầu hoàn tất toàn bộ plan.
**Chuyện gì xảy ra:** Hook chặn dừng hơn chục lần, mỗi lần với cùng lý do. Agent lặp lại câu trả lời 'chờ Windows / chờ anh' và thử kiểm git fetch mỗi vòng mà không có gì mới. Cuối cùng người dùng phải tự hỏi 'giờ thì còn việc gì?'.
**Bài học:** Điều kiện dừng phải khớp với phạm vi mà người dùng đã chốt; nếu không, agent chỉ lặp lại trạng thái chờ và tốn lượt.
**Artefact:** Trích một lần chặn và câu trả lời lặp lại; không cần che.
**Góc người ngoài:** cách làm phổ biến là Người dùng tự quyết khi nào dừng; agent dừng khi báo xong và không bị giữ lại; ở đây khác ở Hook bị kích hoạt lặp lại nhiều lần với cùng một lý do, mục tiêu không đổi theo phạm vi user đã thu hẹp. Người đọc sẽ hỏi làm sao thoát được, và tại sao không sửa hook khi scope đổi.
