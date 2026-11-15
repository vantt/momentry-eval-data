---
id: 2026-10-29-chi-dieu-phoi-khong-dung-ui
date: 2026-10-29
repo: repo
status: raw
signals: [đảo nhận định, điều tưởng đúng hoá sai]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1523", "claude:0faf0bb2#L1533", "claude:0faf0bb2#L1547", "claude:0faf0bb2#L1574"]
hook: "Paperclip tưởng chỉ điều phối, hoá ra có runtime Rust và coi OpenClaw là thuê ngoài"
tension: tuong_ma_hoa_ra
sides: ["Tưởng Paperclip chỉ điều phối", "Tự có Native Runner viết bằng Rust, ẩn adapter OpenClaw"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# 'Chỉ điều phối' không đúng: UI giấu adapter OpenClaw, Paperclip tự có runtime

**Bối cảnh:** Người dùng thấy form tạo agent không có lựa chọn OpenClaw, chỉ có các adapter khác.
**Chuyện gì xảy ra:** Code cho thấy adapter openclaw_gateway bị đánh dấu comingSoon và ẩn khỏi danh sách chọn. Các khả năng như skill, model và instruction đều ALL_FALSE. Paperclip còn có Native Runner viết bằng Rust để chạy CLI agent trên máy, cùng các agent dựng sẵn. Nghĩa là OpenClaw bị coi như nhân viên thuê ngoài, và mô tả 'chỉ điều phối' phải được sửa lại.
**Bài học:** Đọc danh sách lựa chọn trong UI và cờ capability trong code trước khi tin mô tả kiến trúc trong README.
**Artefact:** Đoạn code registry có comingSoon: true và hideFromVisualSelection: true. Đường dẫn đã che.
