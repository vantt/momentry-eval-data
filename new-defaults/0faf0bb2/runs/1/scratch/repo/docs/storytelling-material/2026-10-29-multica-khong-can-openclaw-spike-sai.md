---
id: 2026-10-29-multica-khong-can-openclaw-spike-sai
date: 2026-10-29
repo: repo
status: raw
signals: [điều tưởng đúng hoá sai, đảo quyết định]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3373", "claude:0faf0bb2#L3379", "claude:0faf0bb2#L3382", "claude:0faf0bb2#L3398"]
hook: "Spike chọn nhầm OpenClaw; đổi sang Claude Code, 5/5 tiêu chí trong một buổi"
tension: tuong_ma_hoa_ra
sides: ["Tưởng Multica phải chạy OpenClaw", "Hơn 25 CLI được hỗ trợ, OpenClaw chỉ là một"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica không cần OpenClaw: spike sai hướng vì giả định Multica chạy OpenClaw

**Bối cảnh:** Sau khi spike Multica + AICoworker trượt, người dùng hỏi có cần runtime OpenClaw không.
**Chuyện gì xảy ra:** Multica là tầng điều phối, daemon tự tìm các CLI có trong PATH. Có hơn 25 CLI được hỗ trợ, gồm Claude Code và Codex. OpenClaw chỉ là một trong số đó. Spike trước đã chọn OpenClaw từ đầu vì một giả định chưa kiểm chứng. Khi chuyển sang Claude Code, spike đạt 5/5 tiêu chí chỉ trong một buổi.
**Bài học:** Đọc danh sách runtime được hỗ trợ trước khi chọn runtime để thử. Giả định về kiến trúc của nền tảng có thể sai.
**Artefact:** Sơ đồ daemon gọi các CLI khác nhau.
