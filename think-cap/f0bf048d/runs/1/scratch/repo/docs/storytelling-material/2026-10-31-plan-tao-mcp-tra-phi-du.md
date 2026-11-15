---
id: 2026-10-31-plan-tao-mcp-tra-phi-du
date: 2026-10-31
repo: repo
status: raw
signals: ["2"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1598", "claude:f0bf048d#L1601", "claude:f0bf048d#L1604", "claude:f0bf048d#L1620", "claude:f0bf048d#L1635"]
hook: "Plan lọc đúng MCP trả phí, trừ nhánh workspace chưa tồn tại"
tension: cam_ma_van_lot
sides: ["Bộ lọc chặn server trả phí khi khách chưa mua", "Nhánh workspace mới vẫn tạo DataForSEO"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Plan tạo MCP trả phí dù khách chưa mua, do nhánh workspace chưa tồn tại

**Bối cảnh:** Gói có add-on trả phí (DataForSEO); khách chưa mua add-on nhưng plan vẫn tạo server.
**Chuyện gì xảy ra:** Plan có hai nhánh: workspace đã tồn tại thì lọc đúng, còn workspace chưa tồn tại thì đi nhánh khác và vẫn tạo server dataforseo. Tìm ra nhánh bằng grep 'does not exist yet' rồi thêm bộ lọc vào danh sách mcp. Kiểm bằng ba trường hợp, DataForSEO không được tạo khi khách chưa mua.
**Bài học:** Với logic có nhiều nhánh, kiểm mọi nhánh, kể cả nhánh tạo mới, không chỉ nhánh đường chính.
