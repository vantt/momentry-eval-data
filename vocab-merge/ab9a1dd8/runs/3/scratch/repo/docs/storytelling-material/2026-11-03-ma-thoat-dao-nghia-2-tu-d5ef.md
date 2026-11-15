---
id: 2026-11-03-ma-thoat-dao-nghia-2-tu-d5ef
code: M-ANTX
aliases: [M-ANTX]
date: 2026-11-03
repo: repo
status: raw
signals: [đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L616", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L1253"]
hook: "Mã thoát 2 từng nghĩa 'vi phạm riêng tư', nay thành 'sai cú pháp'"
tension: cam_ma_van_lot
sides: ["Chuẩn mới: mã 2 là sai cú pháp", "Script cũ hiểu sai im lặng đúng chỗ kiểm riêng tư"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mã thoát đảo nghĩa: 2 từ 'vi phạm riêng tư' thành 'sai cú pháp'

**Bối cảnh:** Mã thoát cũ: 1 là gõ sai lệnh, 2 là check thấy lỗi khuôn hoặc vi phạm riêng tư. Người dùng có thể đã dùng `momentry check` làm pre-commit hook.
**Chuyện gì xảy ra:** Chuẩn mới chuyển thành 0 là xong, 1 là có lỗi (gồm cả vi phạm), 2 là sai cú pháp. Agent sửa ba bộ test cũ đang kiểm mã 2 và cập nhật CHANGELOG với mục Breaking. Nếu không sửa, script cũ sẽ hiểu sai im lặng đúng ở chỗ kiểm riêng tư.
**Bài học:** Đổi mã thoát là đổi hợp đồng công khai. Hãy liệt kê script nào có thể đang đọc mã đó, và ghi vào changelog.
**Artefact:** Bảng mã thoát cũ và mới cạnh nhau. Không cần che.
