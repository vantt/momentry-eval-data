---
id: 2026-11-02-python-them-ohs-language-pack-thieu
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2178", "claude:2dfb5915#L2247"]
hook: "Thiếu một biến môi trường, hai MCP dựng lại index mãi"
tension: nho_ma_to
sides: ["thiếu một biến môi trường", "hai MCP dựng lại index liên tục"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Python thêm OHS_LANGUAGE_PACK: thiếu biến thì hai MCP dựng lại index liên tục

**Bối cảnh:** Lệnh follow báo một commit Python mới chưa chuyển.
**Chuyện gì xảy ra:** Hai MCP dùng chung một index. Nếu một bên không bật gói ngôn ngữ, OHS sẽ dựng lại view pack liên tục, theo mô tả của agent. Rust đặt biến cho mọi lần khởi động OHS (MCP, related, doctor). Chuyển xong, parity 64/64, follow báo 0.
**Bài học:** Khi hai tiến trình đọc chung một cache, cấu hình phải đồng nhất giữa chúng.
**Artefact:** Không.
