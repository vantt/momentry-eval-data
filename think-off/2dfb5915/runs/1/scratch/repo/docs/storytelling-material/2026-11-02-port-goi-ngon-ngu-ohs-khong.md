---
id: 2026-11-02-port-goi-ngon-ngu-ohs-khong
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2187", "claude:2dfb5915#L2247", "claude:2dfb5915#L2282"]
hook: "Hai công cụ dùng chung index nhưng lệch cấu hình, dựng lại mãi"
tension: hop_ma_tan
sides: ["pkm và MCP ohs dùng chung một index", "cấu hình gói ngôn ngữ khác nhau, index dựng lại liên tục"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Port gói ngôn ngữ OHS: không bật thì index dựng lại liên tục

**Bối cảnh:** Bản Python thêm biến OHS_LANGUAGE_PACK trỏ tới gói tiếng Việt trong bundle.
**Chuyện gì xảy ra:** Nếu pkm và MCP ohs của người dùng dùng chung một index nhưng cấu hình gói ngôn ngữ khác nhau, OHS sẽ dựng lại view gói liên tục. Port vào Rust: mọi lần khởi động OHS đều đặt biến này khi có gói. Kiểm với gói thật cho thấy status báo language_pack.loaded là true.
**Bài học:** Hai tiến trình dùng chung một index phải có cùng cấu hình, nếu không sẽ rebuild mà không ai thấy.
**Artefact:** Không có.
