---
id: 2026-11-02-lan-phat-hanh-dau-bon-goi
date: 2026-11-02
repo: repo
status: raw
signals: [Artefact nhìn được, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2546", "claude:c4caee3c#L2986", "claude:c4caee3c#L3001", "claude:c4caee3c#L3370"]
hook: "Bốn gói phát hành đầu tiên giải nén 280–330 MB, vượt mục tiêu 250"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lần phát hành đầu: bốn gói dựng sẵn, giải nén 280–330 MB

**Bối cảnh:** Mục tiêu PRD: khách cài từ gói dựng sẵn cho bốn nền, không phải chạy npm.
**Chuyện gì xảy ra:** Release v0.17.2-vantt.1 có win32-x64 (zip 102,6 MB, giải nén 279,3 MB), darwin-arm64 (99,5 MB, 326,3 MB), linux-x64 (99,0 MB, 295,7 MB) và darwin-x64 (87,5 MB, 281,6 MB). Smoke test trên máy sạch kiểm sha256, status, search qua stdio, bắt tay MCP và nạp gói tiếng Việt. Mục tiêu 250 MB không đạt và người duyệt chấp nhận.
**Bài học:** Đo kích thước gói thật sớm; mục tiêu ghi trong spec có thể lệch cả bậc độ lớn.
**Artefact:** Bảng asset của release, không kèm đường dẫn cá nhân.
