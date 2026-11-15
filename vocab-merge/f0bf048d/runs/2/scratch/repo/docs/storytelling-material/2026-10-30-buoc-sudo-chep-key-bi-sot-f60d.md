---
id: 2026-10-30-buoc-sudo-chep-key-bi-sot-f60d
code: M-C0ZF
aliases: [M-C0ZF]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ, người duyệt máy]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L480", "claude:f0bf048d#L955", "claude:f0bf048d#L963", "claude:f0bf048d#L968"]
hook: "Quên một bước sudo, agent tự báo blocked sau 20 giây"
tension: nho_ma_to
sides: ["Một bước chép key nằm ngoài công cụ", "Agent tự phát hiện và dừng sau 20 giây"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bước sudo chép key bị sót: agent kiểm thử báo blocked sau 20 giây

**Bối cảnh:** Thử nghiệm đầu tiên: giao issue SEO cho agent đã cài MCP nhưng chưa có file key.
**Chuyện gì xảy ra:** Agent khởi động được cả hai MCP server, gọi được list_sites, rồi tự phát hiện thiếu file key dưới user daemon và chuyển issue sang blocked sau 20 giây. Nguyên nhân là bước sudo install chép key nằm ngoài công cụ đóng gói nên bị bỏ sót. Sau đó đưa khai báo files vào manifest và kiểm MCP dưới đúng user daemon.
**Bài học:** Bước đặt bí mật lên máy phải nằm trong công cụ đóng gói, và việc kiểm phải chạy bằng đúng user sẽ chạy agent chứ không bằng user người triển khai.
**Artefact:** Comment blocked của agent (che đường dẫn home).
