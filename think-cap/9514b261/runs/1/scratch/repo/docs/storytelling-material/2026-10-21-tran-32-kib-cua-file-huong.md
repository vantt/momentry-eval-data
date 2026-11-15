---
id: 2026-10-21-tran-32-kib-cua-file-huong
date: 2026-10-21
repo: repo
status: raw
signals: [số trước/sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L1704"]
hook: "File hướng dẫn agent vượt trần 32 KiB: 46.754 byte, rồi thành 46.919"
tension: giup_ma_hai
sides: ["Khối AgentKit chưa commit thêm vào để hướng dẫn agent", "File phình thêm 165 byte, đã vượt trần 32 KiB từ trước"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trần 32 KiB của file hướng dẫn agent: khối chưa commit đưa file vượt trần

**Bối cảnh:** File hướng dẫn chung của repo được Codex đọc, và có giới hạn cắt sau 32 KiB mà không báo lỗi.
**Chuyện gì xảy ra:** Cây làm việc của chủ có file này 46.754 byte, vượt trần 32 KiB. Sau khi pull, file tăng lên 46.919 byte vì khối AgentKit chưa commit. Agent không commit nguyên file mà quy định quy trình chỉ commit từng phần.
**Bài học:** Đặt trần kích thước cho file đọc tự động và kiểm trong pre-commit, vì giới hạn cắt âm thầm rất khó nhận ra.
**Artefact:** Bảng số byte qua các thời điểm và trần 32 KiB.
