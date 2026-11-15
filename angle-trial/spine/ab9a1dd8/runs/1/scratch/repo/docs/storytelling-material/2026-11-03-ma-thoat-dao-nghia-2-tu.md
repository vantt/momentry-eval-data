---
id: 2026-11-03-ma-thoat-dao-nghia-2-tu
date: 2026-11-03
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L616", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L1253"]
hook: "Mã thoát 2 từng là vi phạm riêng tư, nay là sai cú pháp"
tension: cam_ma_van_lot
sides: ["Script cũ canh vi phạm riêng tư bằng mã 2", "Mã 2 đổi nghĩa nên chính chỗ kiểm riêng tư bị hiểu sai im lặng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, và đang chuẩn bị phát hành. Người làm định đưa mã thoát về chuẩn chung (0 xong, 1 có lỗi, 2 sai cú pháp), nhưng mã 2 hiện đang báo vi phạm riêng tư và có thể có script đang dựa vào nó. Đổi nghĩa âm thầm sẽ làm các script đó hiểu sai đúng ở chỗ kiểm riêng tư. Dev viết pre-commit hook hay script quanh CLI nên quan tâm, vì mã thoát là hợp đồng công khai."
audience: dev viết script hoặc pre-commit hook quanh CLI
spine_context: "Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, đang chuẩn bị phát hành bản có phần phân phối rõ ràng."
spine_context_lines: [profile, "claude:ab9a1dd8#L236"]
spine_want: "Đưa mã thoát về chuẩn chung CMD-08: 0 là xong, 1 là có lỗi, 2 là sai cú pháp."
spine_want_lines: ["claude:ab9a1dd8#L264", "claude:ab9a1dd8#L616"]
spine_obstacle: "Mã 2 hiện đang báo vi phạm riêng tư, và có thể có script đang đọc mã này để chặn commit."
spine_obstacle_lines: ["claude:ab9a1dd8#L256"]
spine_turn: "Tưởng đổi mã thoát chỉ là dọn theo chuẩn; hoá ra mã 2 có thể là hợp đồng công khai với các script kiểm riêng tư, và các test vẫn kỳ vọng mã 2 cho vi phạm."
spine_turn_lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L1253"]
spine_action: Đổi bảng mã thoát và sửa các test đang kiểm mã 2 sang mã 1.
spine_action_lines: ["claude:ab9a1dd8#L616", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908"]
spine_outcome: "Sau khi sửa, suite còn 204 test qua và 1 test hỏng."
spine_outcome_lines: ["claude:ab9a1dd8#L911"]
spine_takeaway: "Đổi mã thoát là đổi hợp đồng công khai: liệt kê script nào có thể đang đọc mã đó và ghi vào changelog."
spine_takeaway_lines: ["claude:ab9a1dd8#L256"]
completeness: 7
---

# Mã thoát đảo nghĩa: 2 từ 'vi phạm riêng tư' thành 'sai cú pháp'

**Góc kể:** Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent, và đang chuẩn bị phát hành. Người làm định đưa mã thoát về chuẩn chung (0 xong, 1 có lỗi, 2 sai cú pháp), nhưng mã 2 hiện đang báo vi phạm riêng tư và có thể có script đang dựa vào nó. Đổi nghĩa âm thầm sẽ làm các script đó hiểu sai đúng ở chỗ kiểm riêng tư. Dev viết pre-commit hook hay script quanh CLI nên quan tâm, vì mã thoát là hợp đồng công khai.
**Bối cảnh:** Mã thoát cũ: 1 là gõ sai lệnh, 2 là check thấy lỗi khuôn hoặc vi phạm riêng tư. Người dùng có thể đã dùng `momentry check` làm pre-commit hook.
**Chuyện gì xảy ra:** Chuẩn mới chuyển thành 0 là xong, 1 là có lỗi (gồm cả vi phạm), 2 là sai cú pháp. Agent sửa ba bộ test cũ đang kiểm mã 2 và cập nhật CHANGELOG với mục Breaking. Nếu không sửa, script cũ sẽ hiểu sai im lặng đúng ở chỗ kiểm riêng tư.
**Bài học:** Đổi mã thoát là đổi hợp đồng công khai. Hãy liệt kê script nào có thể đang đọc mã đó, và ghi vào changelog.
**Artefact:** Bảng mã thoát cũ và mới cạnh nhau. Không cần che.
