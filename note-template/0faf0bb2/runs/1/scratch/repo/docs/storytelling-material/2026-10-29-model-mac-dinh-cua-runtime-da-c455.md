---
id: 2026-10-29-model-mac-dinh-cua-runtime-da-c455
code: M-2XD4
aliases: [M-2XD4]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1079", "claude:0faf0bb2#L1080", "claude:0faf0bb2#L1115", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1129", "claude:0faf0bb2#L1137"]
hook: "Model mặc định đã ngừng, nhưng chỉ sửa được session của công cụ"
tension: chon_mot_mat_mot
sides: ["Sửa riêng session điều phối sang bản flash cho chạy được", "Agent chính vẫn hỏng với mọi việc khác cho tới khi đổi model mặc định"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model mặc định của runtime đã ngừng, làm hỏng agent chính

**Bối cảnh:** Runtime AICoworker dùng một model mặc định là bản thử của nhà cung cấp. Model này đã bị ngừng.
**Chuyện gì xảy ra:** Lỗi 'model không còn khả dụng' khiến agent chính của runtime không trả lời được, dù lỗi không nằm ở công cụ điều phối. Thay vì sửa file cấu hình gốc, chỉ đặt model cho session riêng của công cụ điều phối sang bản flash, rồi comment để đánh thức lại. Lỗi vẫn còn nguyên với mọi việc khác của người dùng cho tới khi họ đổi model mặc định.
**Bài học:** Khi nền tảng đổi danh mục model, kiểm tra model mặc định trước. Đổi theo từng session giúp tránh ảnh hưởng diện rộng, nhưng vẫn phải sửa gốc.
**Artefact:** Ảnh đoạn cấu hình model mặc định, che khoá API. Hoặc dòng thông báo lỗi model.
