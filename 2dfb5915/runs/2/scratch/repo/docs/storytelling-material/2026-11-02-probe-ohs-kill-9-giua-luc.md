---
id: 2026-11-02-probe-ohs-kill-9-giua-luc
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L307", "claude:2dfb5915#L325"]
hook: "Kill -9 giữa lúc index mà không còn tiến trình mồ côi"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe OHS: kill -9 giữa lúc index không để lại tiến trình node

**Bối cảnh:** Phase 04 kiểm OHS chạy qua stdio.
**Chuyện gì xảy ra:** Sáu truy vấn search gửi đồng thời, khớp 6/6 với CLI của OHS. Sau mỗi lần thoát, ps không còn node. Khi kill -9 giữa lúc index, OHS thấy stdin đóng và thoát trong dưới 1 giây.
**Bài học:** Dựa vào stdin đóng để tiến trình con tự thoát, đừng tin vào tín hiệu kill.
**Artefact:** Không.
