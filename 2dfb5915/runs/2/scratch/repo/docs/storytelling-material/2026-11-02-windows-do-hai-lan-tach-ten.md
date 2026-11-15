---
id: 2026-11-02-windows-do-hai-lan-tach-ten
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1364", "claude:2dfb5915#L1873", "claude:2dfb5915#L1929"]
hook: "Windows đỏ hai lần vì một dấu gạch chéo"
tension: nho_ma_to
sides: ["một dấu gạch chéo", "CI Windows đỏ hai lần, chỉ lộ trên Windows"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Windows đỏ hai lần: tách tên theo '/' và dấu gạch chéo nhân đôi trong JSON

**Bối cảnh:** CI trên Windows đỏ ở hai chỗ khác nhau trong cùng một đợt.
**Chuyện gì xảy ra:** Hàm basename chỉ tách theo '/', nên tên vault thành cả đường dẫn có ổ đĩa và lọt vào chuỗi instructions của MCP. Bản Python dùng ntpath nên tách cả hai kiểu. Sau đó bước parity vẫn lệch vì đường dẫn trong JSON có dấu gạch chéo nhân đôi, còn bộ che đường dẫn không nhận ra dạng đó. Cả hai lỗi chỉ lộ trên Windows.
**Bài học:** Xử lý đường dẫn khác nền tảng: dùng đúng hàm của bản gốc, và kiểm cả dạng escape khi đưa vào JSON.
**Artefact:** Không.
