---
id: 2026-10-21-canh-bao-nam-o-cuoi-huong
date: 2026-10-21
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3609", "claude:9514b261#L3620", "claude:9514b261#L3949"]
hook: "Rủi ro được ghi lại, nhưng chỉ nằm ở dòng cuối hướng dẫn"
tension: khac
sides: ["Rủi ro đã được nhận ra", "Người đọc chỉ biết khi đã gần xong"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cảnh báo nằm ở cuối hướng dẫn, và việc kiểm tra còn để dở

**Bối cảnh:** Hướng dẫn cài đặt TheHive cho máy mới có một cảnh báo ở đoạn cuối: thêm khoá mới vào config toàn cục từng làm hỏng workspace chạy release cũ.
**Chuyện gì xảy ra:** Pool thehive đã được khai sẵn nên agent không sửa config toàn cục. Việc kiểm tra các workspace cũ bằng doctor vẫn để dở và được ghi là việc chưa làm. Đây không phải lỗi đã xảy ra, mà là rủi ro được đưa tới người đọc muộn.
**Bài học:** Đọc hết hướng dẫn trước khi làm, nhất là đoạn cảnh báo cuối. Ghi rõ những việc chưa làm thành mục riêng.
**Artefact:** Không có.
