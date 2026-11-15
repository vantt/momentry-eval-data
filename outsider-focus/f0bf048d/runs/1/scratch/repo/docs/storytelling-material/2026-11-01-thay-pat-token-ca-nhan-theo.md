---
id: 2026-11-01-thay-pat-token-ca-nhan-theo
date: 2026-11-01
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L2548", "claude:f0bf048d#L2549", "claude:f0bf048d#L2550", "claude:f0bf048d#L2555", "claude:f0bf048d#L2556"]
hook: "Thu hồi token cũ trước khi sửa chỗ dùng nó là cách làm gãy hệ thống"
tension: giup_ma_hai
sides: ["Thu hồi token cũ ngay cho an toàn", "Mọi nơi còn dùng token cũ đều gãy"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thay PAT (token cá nhân) theo thứ tự an toàn: tạo token mới, cập nhật mọi nơi dùng, kiểm token mới chạy, rồi mới thu hồi token cũ và xác nhận token cũ hết hiệu lực

**Chuyện gì xảy ra:** Thay PAT (token cá nhân) theo thứ tự an toàn: tạo token mới, cập nhật mọi nơi dùng, kiểm token mới chạy, rồi mới thu hồi token cũ và xác nhận token cũ hết hiệu lực
**Góc người ngoài:** cách làm phổ biến là Thường thu hồi/đổi token rồi mới đi sửa chỗ hỏng, hoặc để token cũ nằm đó vì sợ gãy hệ thống; ở đây khác ở Xoay khoá không gây gián đoạn: kiểm cả hai chiều (cũ không dùng được, mới dùng được), rồi chạy lại plan/CLI để chắc mọi công cụ vẫn sống. Dev một mình hay bỏ qua việc thu hồi vì sợ gãy.
