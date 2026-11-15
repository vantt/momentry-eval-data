---
id: 2026-10-29-lech-phien-ban-giao-thuc-agent-c455
code: M-TCFV
aliases: [M-TCFV]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân gốc nhỏ, số]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L922", "claude:0faf0bb2#L947", "claude:0faf0bb2#L959", "claude:0faf0bb2#L968", "claude:0faf0bb2#L987", "claude:0faf0bb2#L1016", "claude:0faf0bb2#L1021"]
hook: "Agent kẹt vì lệch phiên bản v3 và v4; sửa số 4 thành 3 là chạy"
tension: nho_ma_to
sides: ["Một con số trong giao thức lệch nhau", "Agent kẹt ở verifying cho đến khi vá ba chỗ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lệch phiên bản giao thức: agent kẹt ở 'verifying' vì Paperclip đòi v4, gateway chỉ có v3

**Bối cảnh:** Ba agent của công ty mẫu đều không qua được bước kiểm tra kết nối với gateway OpenClaw.
**Chuyện gì xảy ra:** Log báo harness_test_failed. Adapter của Paperclip đặt minProtocol=4, còn gateway của AICoworker chỉ nói v3. Git log của Paperclip có commit 'bump PROTOCOL_VERSION to 4' ghi rõ không đổi ngữ nghĩa khung. Agent sửa minProtocol thành 3 ở ba chỗ trong bản đã cài, có giữ file .orig. Sau khi khởi động lại, log báo 'Gateway connect probe succeeded' và agent chuyển sang ready. Bản vá sẽ mất khi nâng cấp Paperclip.
**Bài học:** Khi hai bên lệch version, hãy đọc commit message của chính dự án trước để biết thay đổi có thật hay chỉ là con số.
**Artefact:** Dòng log 'Gateway connect probe succeeded' và bảng ba chỗ sửa minProtocol.
