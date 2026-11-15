---
id: 2026-11-02-harness-chan-sleep-noi-lenh-chuyen
date: 2026-11-02
repo: repo
status: raw
signals: [sự cố vặt]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L1460", "claude:2dfb5915#L1466"]
hook: "Harness chặn lệnh sleep nối lệnh khác, agent chuyển sang watch nền"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Harness chặn sleep nối lệnh, chuyển sang watch nền

**Bối cảnh:** Agent chờ CI bằng sleep 30 rồi gh run watch trong cùng một lệnh.
**Chuyện gì xảy ra:** Harness chặn lệnh ghép sleep với lệnh khác và yêu cầu dùng vòng lặp hoặc chạy nền. Agent chuyển sang chạy watch nền và được báo khi xong.
**Bài học:** Chờ CI bằng lệnh chạy nền có thông báo, không dùng sleep dài.
**Artefact:** Không có.
