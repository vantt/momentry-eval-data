---
id: 2026-11-02-panic-lan-build-dau-lam-moi
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1777", "claude:2dfb5915#L1950"]
hook: "Một lần panic khi build đầu làm mọi tool call treo vĩnh viễn"
tension: nho_ma_to
sides: ["một panic ở lần build đầu", "mọi tool call treo mãi, server không thoát"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Panic lần build đầu làm mọi tool call treo vĩnh viễn

**Bối cảnh:** Review crate pkm sau khi nối tool vào MCP server.
**Chuyện gì xảy ra:** Cờ ready chỉ được đặt sau lần build đầu. Nếu build panic, tools/call chờ không giới hạn và server không thoát. Truy vấn paths và loops không có trần max_len, nên max_len 8 đến 10 có thể nổ tổ hợp, chiếm CPU và RAM, và giữ khoá state làm mọi request sau đó đứng. Sửa: trần max_len 12, timeout 10 giây cho mỗi truy vấn, và đường thoát khi panic.
**Bài học:** Mọi chờ đợi trong server cần giới hạn thời gian. Luồng nền panic phải được báo lại, không được im lặng.
**Artefact:** Không.
