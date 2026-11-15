---
id: 2026-10-21-sua-config-toan-cuc-dung-chung-fd46
code: M-4JKK
aliases: [M-4JKK]
date: 2026-10-21
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2375", "claude:9514b261#L2422", "claude:9514b261#L2438", "claude:9514b261#L3609", "claude:9514b261#L3949"]
hook: "Config toàn cục đã sửa, nhưng các workspace cũ chưa kiểm"
tension: nho_ma_to
sides: ["Đã sao lưu và kiểm định dạng config toàn cục", "Chưa chạy doctor ở các workspace khác, rủi ro còn mở"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Sửa config toàn cục dùng chung mà chưa kiểm các workspace cũ, theo cảnh báo trong hướng dẫn

**Bối cảnh:** Config toàn cục ~/.fgos dùng chung cho nhiều workspace. Hướng dẫn TheHive ghi thêm khoá mới từng làm hỏng workspace chạy release cũ, ngày 13/10.
**Chuyện gì xảy ra:** Agent đã ghi khoá llmAccounts vào config toàn cục, có sao lưu và kiểm định dạng. Đến cuối, agent nói rõ việc chạy fgos doctor ở các workspace khác để kiểm vẫn chưa làm, nên rủi ro còn mở.
**Bài học:** Config dùng chung nhiều workspace cần kiểm các workspace cũ trước khi thêm khoá mới, không chỉ kiểm máy hiện tại.
**Artefact:** Không có. Ghi cảnh báo và danh sách việc còn lại.
