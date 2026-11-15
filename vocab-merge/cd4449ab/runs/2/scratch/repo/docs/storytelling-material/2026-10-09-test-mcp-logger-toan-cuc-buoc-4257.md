---
id: 2026-10-09-test-mcp-logger-toan-cuc-buoc-4257
code: M-HK3V
aliases: [M-HK3V]
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1221", "omp:cd4449ab#L1251", "omp:cd4449ab#L1278", "omp:cd4449ab#L3749", "omp:cd4449ab#L3764", "omp:cd4449ab#L3776", "omp:cd4449ab#L3785", "omp:cd4449ab#L3786", "omp:cd4449ab#L3800", "omp:cd4449ab#L3812", "omp:cd4449ab#L3839", "omp:cd4449ab#L3875", "omp:cd4449ab#L3890", "omp:cd4449ab#L3896", "omp:cd4449ab#L3911", "omp:cd4449ab#L3920"]
hook: "12 lần đỏ chỉ vì fixture sai trường, logger toàn cục buộc chạy tuần tự"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test MCP: logger toàn cục buộc chạy tuần tự, fixture source-import đỏ 12 lần

**Bối cảnh:** Các test MCP chạy song song, nhưng một test kiểm tra logger chẩn đoán toàn cục do New() thay thế.
**Chuyện gì xảy ra:** Test telemetry phải chạy serial vì nó assert trên logger toàn cục. Test source import đỏ liên tục: skill mẫu thiếu trường, source record sai kiểu revision, kind không hợp lệ. Đếm khoảng 12 lần chạy đỏ trước khi TestSourceImportMCPPreviewAndConfirm xanh.
**Bài học:** Test có state toàn cục phải được đánh dấu serial rõ ràng. Fixture MCP nên dùng cùng schema với code.
**Artefact:** Không cần ảnh.
