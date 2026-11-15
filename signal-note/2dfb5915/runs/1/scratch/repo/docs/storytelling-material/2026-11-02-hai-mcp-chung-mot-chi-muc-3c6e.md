---
id: 2026-11-02-hai-mcp-chung-mot-chi-muc-3c6e
code: M-529F
aliases: [M-529F]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2187", "claude:2dfb5915#L2282"]
hook: "Hai MCP khác một biến cấu hình, OHS dựng lại index mãi"
tension: nho_ma_to
sides: ["Một biến môi trường pkm quên đặt", "OHS dựng lại view liên tục"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai MCP chung một chỉ mục, khác cấu hình gói ngôn ngữ thì OHS dựng lại index liên tục

**Bối cảnh:** Người dùng có MCP ohs riêng đọc cùng index với pkm. Bản Python đã bật gói ngôn ngữ tiếng Việt qua biến môi trường.
**Chuyện gì xảy ra:** Nếu pkm không đặt cùng biến, hai bên dùng cấu hình gói khác nhau và OHS liên tục dựng lại các view gói. Đây là một commit Python cần chuyển sang Rust, kèm việc nâng ghim và dựng lại golden.
**Bài học:** Khi hai tiến trình dùng chung cache hay index, mọi cấu hình ảnh hưởng tới index phải giống hệt nhau ở cả hai.
**Artefact:** Mô tả hai tiến trình chung index (không kèm đường dẫn).
