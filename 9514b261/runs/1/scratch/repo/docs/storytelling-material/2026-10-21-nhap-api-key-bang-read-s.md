---
id: 2026-10-21-nhap-api-key-bang-read-s
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3895", "claude:9514b261#L3906", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Nhập API key mà không để lộ một ký tự nào"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhập API key bằng 'read -s' vào ô ẩn rồi ghi thẳng vào file, sau đó kiểm tính hợp lệ chỉ bằng độ dài, thống kê loại ký tự và một lệnh curl trả mã HTTP, không bao giờ in khoá ra màn hình hay vào chat.

**Chuyện gì xảy ra:** Nhập API key bằng 'read -s' vào ô ẩn rồi ghi thẳng vào file, sau đó kiểm tính hợp lệ chỉ bằng độ dài, thống kê loại ký tự và một lệnh curl trả mã HTTP, không bao giờ in khoá ra màn hình hay vào chat.
**Góc người ngoài:** cách làm phổ biến là Thường dán key vào lệnh echo/export hoặc vào chat, để lại trong history; khi lỗi 401 thì đoán mò hoặc dán lại; ở đây khác ở Người đọc muốn cách chẩn đoán key hỏng mà không lộ key: phiên chứng minh được khoá thừa một ký tự (25 so với 24) và xác nhận sửa xong bằng mã 200, mà agent không từng đọc nội dung khoá.
