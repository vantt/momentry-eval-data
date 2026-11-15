---
id: 2026-11-03-doi-ma-thoat-theo-chuan-205
date: 2026-11-03
repo: repo
status: raw
signals: [số trước số sau, đảo quyết định có lý do]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L256", "claude:ab9a1dd8#L889", "claude:ab9a1dd8#L908", "claude:ab9a1dd8#L911", "claude:ab9a1dd8#L1253", "claude:ab9a1dd8#L1259"]
hook: "Đổi mã thoát cho đúng chuẩn, hai lỗi khác nhau thành cùng mã"
tension: giup_ma_hai
sides: ["đổi mã thoát cho đúng chuẩn", "vi phạm riêng tư và lỗi thường trùng mã 1, phải sửa cả hợp đồng công khai"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi mã thoát theo chuẩn: 205 test xanh, sau đổi thì 204 qua 1 hỏng và phải sửa cả hợp đồng công khai

**Bối cảnh:** Mã thoát cũ là 1 cho gõ sai lệnh và 2 cho check thấy vi phạm riêng tư. Chuẩn mới là 1 cho có lỗi và 2 cho sai cú pháp. Script pre-commit của người dùng có thể dựa vào mã cũ.
**Chuyện gì xảy ra:** Sau khi đổi, 204 test qua và 1 hỏng. Agent phải sửa nhiều assert mã thoát trong bốn file test. Mã 2 cũ (vi phạm riêng tư) và mã 1 mới thành cùng một mã, nên vi phạm riêng tư phải tách qua đầu ra khác. Bảng mã thoát được ghi vào CHANGELOG như thay đổi phá tương thích.
**Bài học:** Đổi mã thoát là đổi hợp đồng với mọi script đang dựa vào nó; hãy liệt kê mọi chỗ dùng mã trước khi đổi, và ghi mục Breaking vào changelog.
**Artefact:** Bảng mã thoát trước và sau, cạnh nhau. Không cần che gì.
