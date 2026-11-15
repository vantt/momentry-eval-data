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
angle: none
spine_context: "Một công cụ dòng lệnh đọc transcript phiên làm việc với coding agent và nhặt khoảnh khắc làm chất liệu kể chuyện, đang chuẩn bị phát hành."
spine_context_lines: [profile, "claude:ab9a1dd8#L236"]
spine_want: "Đưa công cụ tới trạng thái người mới cài và chạy được thành công, với bảng mã thoát khớp chuẩn đã chốt."
spine_want_lines: ["claude:ab9a1dd8#L251", "claude:ab9a1dd8#L264"]
spine_obstacle: "Mã 2 đang nghĩa là vi phạm riêng tư. Nếu có script dựa vào nghĩa đó, đổi mã sẽ làm nó hiểu sai mà không báo lỗi."
spine_obstacle_lines: ["claude:ab9a1dd8#L256"]
spine_action: "Đổi mã thoát theo chuẩn: 1 là có lỗi, 2 là sai cú pháp. Cập nhật các test đang kiểm mã 2."
spine_action_lines: ["claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908"]
spine_outcome: "Chạy lại test: 204 qua, 1 hỏng."
spine_outcome_lines: ["claude:ab9a1dd8#L911"]
spine_takeaway: Đổi mã thoát là đổi hợp đồng công khai. Script nào dựa vào mã cũ sẽ hiểu sai im lặng.
spine_takeaway_lines: ["claude:ab9a1dd8#L256"]
completeness: 6
---

# Mã thoát đảo nghĩa: 2 từ 'vi phạm riêng tư' thành 'sai cú pháp'

**Bối cảnh:** Mã thoát cũ: 1 là gõ sai lệnh, 2 là check thấy lỗi khuôn hoặc vi phạm riêng tư. Người dùng có thể đã dùng `momentry check` làm pre-commit hook.
**Chuyện gì xảy ra:** Chuẩn mới chuyển thành 0 là xong, 1 là có lỗi (gồm cả vi phạm), 2 là sai cú pháp. Agent sửa ba bộ test cũ đang kiểm mã 2 và cập nhật CHANGELOG với mục Breaking. Nếu không sửa, script cũ sẽ hiểu sai im lặng đúng ở chỗ kiểm riêng tư.
**Bài học:** Đổi mã thoát là đổi hợp đồng công khai. Hãy liệt kê script nào có thể đang đọc mã đó, và ghi vào changelog.
**Artefact:** Bảng mã thoát cũ và mới cạnh nhau. Không cần che.
