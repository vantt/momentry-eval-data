---
id: 2026-10-29-agent-doan-bua-endpoint-khi-chua-c455
code: M-DN5R
aliases: [M-DN5R]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1264", "claude:0faf0bb2#L1279", "claude:0faf0bb2#L1285", "claude:0faf0bb2#L1519"]
hook: "Agent thiếu skill nên đoán bừa đường dẫn API; cài skill là hết"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent đoán bừa endpoint khi chưa có skill; cài skill vào workspace là xong

**Bối cảnh:** Agent không gọi được API đúng để đóng task.
**Chuyện gì xảy ra:** Agent không có skill paperclip nên tự đoán đường dẫn API. Skill được lấy từ bản server đã cài, đọc nội dung trước khi chép, rồi đặt vào workspace. Sau đó interaction được xác nhận thành công. Cách này mất vài lượt thử sai.
**Bài học:** Agent không có skill sẽ tự đoán API. Cung cấp skill là cách rẻ nhất để chặn lỗi này.
**Artefact:** Cấu trúc thư mục skill trong workspace. Đường dẫn đã che.
