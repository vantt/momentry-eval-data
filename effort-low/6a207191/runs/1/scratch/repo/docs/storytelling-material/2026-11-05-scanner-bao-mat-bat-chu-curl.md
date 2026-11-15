---
id: 2026-11-05-scanner-bao-mat-bat-chu-curl
date: 2026-11-05
repo: repo
status: raw
signals: [khác, nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1304", "claude:6a207191#L1318", "claude:6a207191#L1324", "claude:6a207191#L2372", "claude:6a207191#L2375"]
hook: "Scanner báo 7 lỗi critical, mà chỉ là chữ 'curl | sh' trong tài liệu"
tension: tuong_ma_hoa_ra
sides: ["11 cảnh báo, 7 mức critical", "Không script nào tự tải hay chạy gì, chỉ là chữ trong tài liệu"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Scanner bảo mật bắt chữ 'curl | sh' trong tài liệu: 11 cảnh báo

**Bối cảnh:** Skill cần qua quét bảo mật trước khi gửi lên hub.
**Chuyện gì xảy ra:** Scanner chạy 26 rule và báo 11 phát hiện: 7 critical về pipe-to-shell, 1 high về persist.autostart, 3 medium về privesc. Agent đọc lại hai script kiểm tra và xác nhận không có chỗ nào tự tải hay chạy thứ gì. Tất cả phát hiện là chữ trong tài liệu, mẫu installer, hoặc câu khuyên tránh sudo. User cho gửi dù còn cảnh báo. Lần quét sau vẫn ra đúng 11.
**Bài học:** Scanner chưa phân biệt được chữ trong văn bản với lệnh thật. Hãy ghi sẵn lời giải thích cho người duyệt để họ không hiểu nhầm.
**Artefact:** Bảng 11 phát hiện gồm rule, vị trí và đánh giá. Không đưa đường dẫn người dùng vào.
