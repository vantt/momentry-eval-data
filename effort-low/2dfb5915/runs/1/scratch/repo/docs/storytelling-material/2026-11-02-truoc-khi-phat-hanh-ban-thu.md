---
id: 2026-11-02-truoc-khi-phat-hanh-ban-thu
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:2dfb5915#L2112", "claude:2dfb5915#L2536", "claude:2dfb5915#L3684", "claude:2dfb5915#L3917", "claude:2dfb5915#L3929"]
hook: "CI xanh rồi, agent vẫn tải bản phát hành về kiểm sha256 từng file"
tension: cam_ma_van_lot
sides: ["CI đã xanh, tag đã đẩy, ai cũng coi là xong", "Agent vẫn tải từng file về kiểm checksum và chạy thử binary"]
strength: 1
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi phát hành bản thử, agent đưa bản đó qua một vòng kiểm tra độc lập: tải file phát hành về, kiểm sha256 từng file, chạy thử binary, rồi mới báo xong.

**Chuyện gì xảy ra:** Trước khi phát hành bản thử, agent đưa bản đó qua một vòng kiểm tra độc lập: tải file phát hành về, kiểm sha256 từng file, chạy thử binary, rồi mới báo xong.
**Góc người ngoài:** cách làm phổ biến là Dev thường đẩy tag rồi tin CI là đủ, ít khi tự tải file về để kiểm lại checksum; ở đây khác ở Mỗi bản phát hành đều được tải lại và kiểm checksum trước khi ghi là xong. Người đọc sẽ muốn biết vì sao bước này đáng bỏ công.
