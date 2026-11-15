---
id: 2026-11-02-goi-windows-smoke-xanh-tren-may-40f9
code: M-EB6X
aliases: [M-EB6X]
date: 2026-11-02
repo: repo
status: raw
signals: [khác, artefact nhìn được]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2561"]
hook: "Gói Windows xanh hết trên máy sạch, nhưng SmartScreen chưa ai đo"
tension: tuong_ma_hoa_ra
sides: ["Mọi bài smoke đều qua, trông như xong", "Cảnh báo SmartScreen và lần tải model đầu chưa đo"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói Windows smoke xanh trên máy sạch nhưng chưa đo SmartScreen

**Bối cảnh:** Gói zip Windows x64 nặng 102,6 MB, giải nén 279 MB, chưa ký mã.
**Chuyện gì xảy ra:** Smoke chạy trên runner sạch đều qua: sha256, đường dẫn có dấu cách và tiếng Việt, status, reindex, search, stdio, bắt tay MCP, nạp gói. Chưa đo được cảnh báo SmartScreen và lần tải model đầu tiên qua mạng thật.
**Bài học:** Smoke trên CI không đo được trải nghiệm người dùng thật; ghi rõ những gì chưa kiểm.
**Artefact:** Bảng kích thước gói theo nền.
