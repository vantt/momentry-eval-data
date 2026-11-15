---
id: 2026-10-30-agent-seo-bi-chan-vi-file-f60d
code: M-0ZG8
aliases: [M-0ZG8]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L955", "claude:f0bf048d#L963"]
hook: "Agent SEO chạy được hai server nhưng thiếu một file key"
tension: nho_ma_to
sides: ["hai MCP server khởi động và gọi được", "một bước sudo bị sót nên file key không tới nơi"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent SEO bị chặn vì file key không tới được user daemon

**Bối cảnh:** Chạy thử issue đầu tiên giao cho agent SEO để kiểm tra cả chuỗi từ giao việc đến công cụ.
**Chuyện gì xảy ra:** Hai MCP server khởi động được dưới user daemon và agent gọi được list_sites. Nhưng file key không có ở thư mục của user daemon, vì bước sudo install ở lần triển khai trước đã bị sót. Agent tự tìm ra nguyên nhân, chuyển issue sang blocked và ghi rõ chủ cần làm gì, không bịa số liệu.
**Bài học:** Bước copy file bí mật bằng tay là điểm dễ sót. Đưa nó vào công cụ đóng gói và kiểm bằng đúng user chạy agent.
**Artefact:** Comment blocked của agent (che đường dẫn và tên file).
