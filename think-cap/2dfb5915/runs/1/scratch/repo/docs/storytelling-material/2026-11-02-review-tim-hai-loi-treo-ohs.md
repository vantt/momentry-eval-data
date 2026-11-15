---
id: 2026-11-02-review-tim-hai-loi-treo-ohs
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L591", "claude:2dfb5915#L607", "claude:2dfb5915#L631"]
hook: "Một byte lạ làm OHS treo, search timeout đúng 60 giây"
tension: nho_ma_to
sides: ["Một byte không phải UTF-8 trên stderr", "Toàn bộ OHS treo, search timeout 60 giây"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Review tìm hai lỗi treo OHS: stderr dừng khi gặp byte lạ

**Bối cảnh:** Wrapper chạy OHS qua stdio trong pkm, đọc stderr và ghi stdin.
**Chuyện gì xảy ra:** Reviewer đọc mã (không chạy) và thấy: stderr reader thoát khi gặp byte không phải UTF-8, ví dụ code page tiếng Việt trên Windows. Pipe đầy làm mọi console.error của OHS bị chặn, search timeout 60 s, trạng thái kẹt ở starting. Lỗi thứ hai: stdin giữ mutex không timeout, close() chờ cùng mutex nên pkm không thoát. Sửa bằng luồng ghi riêng, đọc tới EOF, và test fake server phát 0xFF rồi hơn 64 KB.
**Bài học:** Lỗi treo không có thông báo nên thường chỉ review đọc mã mới bắt được; test đường lỗi bằng fake server phát dữ liệu xấu.
**Artefact:** Sơ đồ hai luồng đọc và ghi vẽ tay. Không có ảnh mã.
