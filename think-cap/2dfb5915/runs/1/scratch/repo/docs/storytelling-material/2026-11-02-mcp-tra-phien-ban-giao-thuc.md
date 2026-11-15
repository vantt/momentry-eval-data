---
id: 2026-11-02-mcp-tra-phien-ban-giao-thuc
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L279"]
hook: "Server Python gãy trước nếu Claude Code bỏ đường fallback"
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

# MCP trả phiên bản giao thức cũ hơn Claude Code yêu cầu

**Bối cảnh:** Claude Code 2.1.316 hỏi 2025-11-25, nhưng cả ba server đều trả 2025-06-18.
**Chuyện gì xảy ra:** Claude Code thử server/discover của giao thức mới trước, lỗi thì rơi về initialize. Python chỉ hỗ trợ đường fallback này. Nếu bản Claude Code sau bỏ fallback, server Python gãy trước, nên ghi điều đó thành điều kiện xem lại quyết định.
**Bài học:** Ghi lại đường fallback của client như một điều kiện để xem lại lựa chọn.
**Artefact:** Không có.
