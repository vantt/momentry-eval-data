---
id: 2026-11-03-truoc-khi-bao-hoan-tat-agent-d5ef
code: M-5DTQ
aliases: [M-5DTQ]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L167", "claude:ab9a1dd8#L170", "claude:ab9a1dd8#L2312", "claude:ab9a1dd8#L2315"]
hook: "Test xanh trên máy dev chưa đủ, chạy lại bản clone sạch và CI"
tension: none
sides: []
strength: 0
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi báo hoàn tất, agent chạy lại toàn bộ kiểm tra trong một bản clone sạch và trên CI nhiều hệ điều hành, thay vì chỉ tin vào máy đang làm việc.

**Chuyện gì xảy ra:** Trước khi báo hoàn tất, agent chạy lại toàn bộ kiểm tra trong một bản clone sạch và trên CI nhiều hệ điều hành, thay vì chỉ tin vào máy đang làm việc.
**Góc người ngoài:** cách làm phổ biến là Chạy test trên máy dev, thấy xanh là báo xong; ở đây khác ở Lỗi chỉ lộ ra trên macOS và Windows, và nhiều lỗi nằm ở chỗ máy dev không có (symlink, đường dẫn ngắn, quyền). Người đọc sẽ hỏi vì sao agent không tin máy của mình.
