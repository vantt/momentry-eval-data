---
id: 2026-11-03-doi-ma-thoat-ma-1-va
date: 2026-11-03
repo: repo
status: raw
signals: ["3"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L2230"]
hook: "Sửa mã thoát theo chuẩn lại thành thay đổi phá vỡ"
tension: giup_ma_hai
sides: ["đổi mã thoát cho đúng chuẩn", "mã 1 và 2 đảo nghĩa, thành Breaking trong CHANGELOG"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi mã thoát: mã 1 và 2 đảo nghĩa, thành thay đổi hợp đồng công khai

**Bối cảnh:** Trước đây mã 1 là gõ sai lệnh và mã 2 là check thấy vi phạm riêng tư. Chuẩn của skill đổi ngược hai mã này.
**Chuyện gì xảy ra:** Người dùng chọn theo chuẩn. Mã mới là 0 xong, 1 có lỗi, 2 sai cú pháp; mã 3, 4, 5 giữ nghĩa riêng. Các test kiểm mã thoát phải sửa, và CHANGELOG có mục Breaking.
**Bài học:** Đổi mã thoát làm script pre-commit hiểu sai mà không báo lỗi. Khi mã thoát được dùng làm cổng kiểm riêng tư, đây là kiểu sai nguy hiểm nhất, nên phải ghi vào CHANGELOG.
**Artefact:** Bảng mã thoát cũ và mới cạnh nhau.
