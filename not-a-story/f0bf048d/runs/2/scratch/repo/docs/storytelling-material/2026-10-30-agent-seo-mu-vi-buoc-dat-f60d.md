---
id: 2026-10-30-agent-seo-mu-vi-buoc-dat-f60d
code: M-QMGQ
aliases: [M-QMGQ]
date: 2026-10-30
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L954", "claude:f0bf048d#L963", "claude:f0bf048d#L975"]
hook: "Agent SEO mù vì một lệnh sudo bị sót"
tension: nho_ma_to
sides: ["Cài xong cả bộ MCP, chỉ sót một lệnh đặt key", "Agent không đọc được key, công việc đứng hẳn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent SEO mù vì bước đặt key bị sót

**Bối cảnh:** Agent SEO chạy thử một issue đầu tiên và báo blocked vì không đọc được file credentials.
**Chuyện gì xảy ra:** Phần cài MCP đã chạy xong, nhưng lệnh sudo install đặt key cho user daemon bị sót. Agent không có quyền đọc file đó, nên chuyển issue sang blocked và ghi rõ chủ cần làm gì. Lỗi nằm ở gói chứ không ở agent: việc đặt file bí mật là một bước tay riêng, dễ sót. Sau khi sửa, khai báo file bí mật trong manifest và lệnh cài kiểm lại dưới đúng user daemon.
**Bài học:** Một bước tay dễ sót sẽ khiến agent mù. Đưa bước đó vào khai báo của gói và kiểm nó dưới đúng user chạy agent.
**Artefact:** Thông báo blocked trong issue, đã che nội dung nhạy cảm.
