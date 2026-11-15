---
id: 2026-11-03-chay-installer-that-tu-github-trong-d5ef
code: M-MJFZ
aliases: [M-MJFZ]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L3022", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
hook: "Sau release, tự chạy lệnh cài đúng như người dùng sẽ gõ"
tension: tuong_ma_hoa_ra
sides: ["Trang Release có file nên tưởng đã ổn", "Chỉ tải về chạy lệnh trong README mới biết cài được không"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy installer thật từ GitHub trong HOME tạm sau khi phát hành, để kiểm lệnh cài một dòng đúng như người dùng sẽ gõ

**Chuyện gì xảy ra:** Chạy installer thật từ GitHub trong HOME tạm sau khi phát hành, để kiểm lệnh cài một dòng đúng như người dùng sẽ gõ
**Góc người ngoài:** cách làm phổ biến là Sau khi release, dev thường chỉ kiểm bằng cách nhìn trang Release có file hay không, không tự tải lại và chạy lệnh cài trong README; ở đây khác ở Agent tách HOME để không đụng cấu hình thật, rồi chạy đúng dòng curl | sh trong README để xác nhận cài được, init sẵn sàng, uninstall giữ dữ liệu. Người đọc sẽ hỏi vì sao làm vậy thay vì tin CI đã xanh.
