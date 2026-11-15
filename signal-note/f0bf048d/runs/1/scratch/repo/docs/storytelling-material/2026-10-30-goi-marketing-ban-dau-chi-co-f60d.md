---
id: 2026-10-30-goi-marketing-ban-dau-chi-co-f60d
code: M-X5QV
aliases: [M-X5QV]
date: 2026-10-30
repo: repo
status: raw
signals: [khac]
signal_note: "Đây là điểm xuất phát của cả chuỗi: một khoảng trống về đội ngũ và quyền dữ liệu, được phát hiện bằng cách đọc gói thay vì đoán."
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L79"]
hook: "Gói marketing có 3 agent viết bài nhưng không ai xem được số liệu"
tension: tuong_ma_hoa_ra
sides: ["gói marketing đủ lead, viết, review", "không agent nào có quyền vào dữ liệu SEO hay GA4"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói marketing ban đầu chỉ có 3 agent nội dung, không có SEO hay GA4

**Bối cảnh:** Chủ nhận thấy team marketing không có agent làm SEO, không đọc GA4, không ai phân tích số liệu.
**Chuyện gì xảy ra:** Agent đọc gói và thấy chỉ có 3 agent (lead, viết, review), 1 workflow, 1 việc định kỳ và 1 secret duy nhất là GH_TOKEN. Không agent nào có quyền vào nguồn dữ liệu marketing. Agent đề xuất thêm agent SEO và agent phân tích, kèm secret cho dữ liệu, rồi chờ chủ duyệt.
**Bài học:** Trước khi thêm agent, kiểm xem gói đã có công cụ để agent làm việc đó chưa. Agent không có quyền đọc dữ liệu thì chỉ viết được kế hoạch, không đọc được số liệu.
**Artefact:** Bảng 3 agent và vai trò trong gói (không có secret).
