---
id: 2026-10-29-model-mac-dinh-cua-aicoworker-da-c455
code: M-PRK1
aliases: [M-PRK1]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, lỗi to gốc nhỏ]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1079", "claude:0faf0bb2#L1115", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1129", "claude:0faf0bb2#L1137"]
hook: "Model mặc định đã ngừng hoạt động, ngay cả agent chính cũng hỏng"
tension: nho_ma_to
sides: ["Lỗi không nằm ở Paperclip", "Một model ngừng khả dụng làm hỏng cả agent chính"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model mặc định của AICoworker đã ngừng khả dụng, nên agent chính cũng hỏng

**Bối cảnh:** Trong spike Paperclip, một task không chạy. Điều tra cấu hình model cho thấy model mặc định đã chết.
**Chuyện gì xảy ra:** openclaw.json đặt model mặc định là gemini-3-pro-low, và model này đã ngừng khả dụng. Agent dùng model này báo lỗi. Agent sửa riêng một session bằng lệnh patch model, không đổi cấu hình chung. Agent chính của AICoworker cũng bị ảnh hưởng khi dùng thường ngày, dù lỗi không nằm ở Paperclip.
**Bài học:** Khi agent lỗi, kiểm tra model mặc định trước vì nó có thể làm hỏng mọi agent, không chỉ phần thử nghiệm.
**Artefact:** Đoạn cấu hình models với provider local và model primary. Khoá đã che.
