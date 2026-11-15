---
id: 2026-11-02-dieu-phoi-ghep-cac-goi-phat
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2546", "claude:c4caee3c#L2561", "claude:c4caee3c#L2981"]
hook: "Ba gói đầu qua máy sạch, nhưng Windows chưa ai đo cảnh báo SmartScreen"
tension: khac
sides: ["Ba gói qua smoke test trên máy sạch", "Gói Windows chưa ký mã, chưa biết SmartScreen báo gì"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điều phối ghép các gói phát hành bằng CI và kích thước gói

**Bối cảnh:** Release đầu tiên gồm bốn gói dựng sẵn cho Windows x64, Mac chip Apple, Mac Intel và Linux x64, mỗi gói có sha256 và manifest.
**Chuyện gì xảy ra:** Ba gói đầu qua smoke test trên máy sạch của GitHub, gồm kiểm sha256, đường dẫn có dấu cách và tiếng Việt, và giao thức MCP. Kích thước gói nén 87 đến 103 MB, giải nén 280 đến 330 MB. Gói Windows chưa đo cảnh báo SmartScreen vì chưa ký mã.
**Bài học:** Smoke test trên CI không đo được mọi thứ người dùng gặp; ghi rõ phần chưa đo.
**Artefact:** Bảng kích thước nén và giải nén theo nền.
