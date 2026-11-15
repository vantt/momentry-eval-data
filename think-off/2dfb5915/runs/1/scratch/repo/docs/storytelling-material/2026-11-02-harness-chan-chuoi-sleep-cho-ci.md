---
id: 2026-11-02-harness-chan-chuoi-sleep-cho-ci
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L1460", "claude:2dfb5915#L1466"]
hook: "Harness chặn sleep, agent không lách mà chuyển sang chạy nền"
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

# Harness chặn chuỗi sleep, chờ CI bằng vòng until

**Bối cảnh:** Chờ CI bằng lệnh sleep 30 nối với gh run watch.
**Chuyện gì xảy ra:** Harness chặn lệnh kết hợp sleep và gh run watch, yêu cầu dùng vòng until hoặc chạy nền. Agent chuyển sang chạy nền và không chia nhỏ sleep để lách.
**Bài học:** Khi chờ CI, dùng vòng until hoặc chạy nền. Đừng chia nhỏ sleep để lách giới hạn.
**Artefact:** Không có.
