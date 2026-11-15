---
id: 2026-11-02-goi-windows-mac-va-linux-dau-40f9
code: M-3N2B
aliases: [M-3N2B]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, artefact_nhin_duoc]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2546", "claude:c4caee3c#L2553", "claude:c4caee3c#L2561", "claude:c4caee3c#L2986", "claude:c4caee3c#L3370"]
hook: "Gói Windows 632 MB cắt còn 279 MB, nén còn 100 MB"
tension: it_ma_nhieu
sides: ["Cắt tỉa gói từ 632 MB", "Còn 279 MB, nén còn khoảng 100 MB"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói Windows, Mac và Linux đầu tiên: 632 MB rút còn 279 MB

**Bối cảnh:** Release đầu tiên có gói dựng sẵn cho bốn nền. Mục tiêu PRD là dưới 250 MB giải nén.
**Chuyện gì xảy ra:** Gói Windows có 632 MB trước khi cắt tỉa, và 279 MB sau khi cắt. Gói nén khoảng 100 MB. Chủ dự án chấp nhận kích thước đo thật. Smoke test chạy trên máy sạch của runner GitHub, không cài Node sẵn, và đều xanh. Chưa đo được cảnh báo SmartScreen vì gói chưa ký mã.
**Bài học:** Đo kích thước sau khi cắt tỉa, và nói rõ những gì smoke test trên CI không đo được.
**Artefact:** Bảng kích thước gói theo nền (không có đường dẫn).
