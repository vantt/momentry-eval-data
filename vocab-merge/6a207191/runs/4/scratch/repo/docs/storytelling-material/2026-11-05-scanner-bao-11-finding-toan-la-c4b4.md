---
id: 2026-11-05-scanner-bao-11-finding-toan-la-c4b4
code: M-C2ZR
aliases: [M-C2ZR]
date: 2026-11-05
repo: repo
status: raw
signals: [người duyệt máy soạn, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1318", "claude:6a207191#L1324", "claude:6a207191#L2372", "claude:6a207191#L2375"]
hook: "Scanner báo 11 lỗi, toàn là chữ trong tài liệu về curl | sh"
tension: cam_ma_van_lot
sides: ["Scanner báo 11 finding, trong đó 7 mức critical", "Cả 11 chỉ là chữ mô tả trong tài liệu, không phải lệnh chạy thật"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Scanner báo 11 finding, toàn là chữ trong tài liệu về curl | sh

**Bối cảnh:** Trước khi gửi lên hub, skillstation scan đã chạy và chặn việc gửi với 7 finding critical.
**Chuyện gì xảy ra:** Scanner báo rce.pipe-to-shell 7 lần (critical), persist.autostart 1 lần (high) và privesc.command 3 lần (medium). Agent đọc lại từng vị trí và xác nhận đó là mô tả installer, chú thích và ví dụ mẫu, không phải lệnh skill tự chạy; các chỗ sudo đều khuyên tránh. Người dùng chọn gửi dù còn 11 finding, và các lần gửi sau vẫn báo đúng 11 finding.
**Bài học:** Skill viết về cài đặt bằng curl | sh sẽ luôn bị scanner RCE bắt; cần có ghi chú để người duyệt biết đó là tài liệu, không phải lệnh.
**Artefact:** Bảng 3 nhóm rule, vị trí và đánh giá (L1304-L1324). Cần che đường dẫn cá nhân nếu có.
