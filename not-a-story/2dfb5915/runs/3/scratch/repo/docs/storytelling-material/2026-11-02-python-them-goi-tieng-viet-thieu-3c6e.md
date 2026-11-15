---
id: 2026-11-02-python-them-goi-tieng-viet-thieu-3c6e
code: M-6W47
aliases: [M-6W47]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2178", "claude:2dfb5915#L2196", "claude:2dfb5915#L2247"]
hook: "Commit 54 dòng, thiếu một biến môi trường là index dựng lại mãi"
tension: nho_ma_to
sides: ["Commit chỉ 54 dòng", "Hai OHS cấu hình gói khác nhau khiến view dựng lại liên tục"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Python thêm gói tiếng Việt: thiếu biến môi trường thì index dựng lại mãi

**Bối cảnh:** Commit 223c9c3 của bản Python làm OHS chạy từ bundle có sẵn gói tiếng Việt.
**Chuyện gì xảy ra:** Commit chỉ 54 dòng, nhưng nếu OHS của pkm và OHS của MCP người dùng dùng cấu hình gói khác nhau trên cùng index, OHS sẽ dựng lại view gói liên tục. Agent đặt biến OHS_LANGUAGE_PACK cho mọi lần khởi động OHS, dựng lại golden với ghim mới, và follow báo 0 commit chưa chuyển.
**Bài học:** Hai tiến trình dùng chung một index phải dùng cùng cấu hình, nếu không sẽ tranh nhau dựng lại.
