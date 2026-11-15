---
id: 2026-11-02-phase-15-python-them-goi-tieng-3c6e
code: M-8079
aliases: [M-8079]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Hai tiến trình dùng chung index nhưng khác cấu hình gói ngôn ngữ, OHS sẽ dựng lại view liên tục."
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2178", "claude:2dfb5915#L2282"]
hook: "Một biến môi trường quên đặt làm hai công cụ đọc cùng index khác nhau"
tension: nho_ma_to
sides: ["Một biến môi trường nhỏ", "pkm và MCP dùng hai cấu hình trên cùng index"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phase 15: Python thêm gói tiếng Việt, Rust phải bật cùng biến môi trường

**Bối cảnh:** Commit Python mới bật gói ngôn ngữ tiếng Việt cho OHS.
**Chuyện gì xảy ra:** Nếu pkm không đặt biến OHS_LANGUAGE_PACK như bản Python, pkm và MCP ohs của người dùng sẽ dùng cấu hình khác trên cùng index. Agent chuyển commit này sang Rust, mọi tiến trình OHS do pkm khởi động đều đặt biến, và kiểm bằng gói OHS thật.
**Bài học:** Khi chia sẻ index giữa hai tiến trình, cấu hình phải giống nhau ở cả hai bên.
