---
id: 2026-11-02-panic-luc-build-dau-lam-moi-3c6e
code: M-RC1W
aliases: [M-RC1W]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1777", "claude:2dfb5915#L1780", "claude:2dfb5915#L1790", "claude:2dfb5915#L1950"]
hook: "Một panic lúc khởi động làm mọi lệnh gọi tool treo mãi"
tension: nho_ma_to
sides: ["Panic chỉ xảy ra ở lần build đầu", "Mọi lệnh gọi tool sau đó chờ vô hạn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Panic lúc build đầu làm mọi lệnh gọi tool treo, và truy vấn đường đi bùng nổ tổ hợp

**Bối cảnh:** Server MCP một luồng, giữ khoá trạng thái khi chạy tool.
**Chuyện gì xảy ra:** Panic trong build đầu không đặt cờ sẵn sàng, nên tools/call chờ vô hạn. Truy vấn paths với max_len 8 đến 10 ăn hết CPU và RAM, hành vi này kế thừa từ Python. Sửa bằng trần max_len 12, dừng sau 10 giây; bộ golden chỉ dùng tối đa 4 và answer key tối đa 10 nên không ảnh hưởng.
**Bài học:** Đặt trần và thời hạn cho mọi truy vấn do model sinh ra.
