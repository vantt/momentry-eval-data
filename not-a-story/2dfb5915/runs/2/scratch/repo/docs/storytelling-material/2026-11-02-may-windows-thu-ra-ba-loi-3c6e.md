---
id: 2026-11-02-may-windows-thu-ra-ba-loi-3c6e
code: M-48ZD
aliases: [M-48ZD]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3233", "claude:2dfb5915#L3242", "claude:2dfb5915#L3277"]
hook: "Máy Windows thử ra ba lỗi harness mà Linux không thấy"
tension: khac
sides: ["Harness chạy ổn trên Linux", "Windows lộ ba lỗi: đường dẫn JSON, UTF-8 khi pipe, và cờ -I ẩn PyYAML"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy Windows thử ra ba lỗi harness: đường dẫn JSON, UTF-8 khi pipe, và -I ẩn user site

**Bối cảnh:** Người dùng chạy phần thử trên một máy Windows sạch, gồm cả việc chạy harness với vault thật.
**Chuyện gì xảy ra:** Ba lỗi: Scrub không che đường dẫn Windows dạng escape trong JSON nên CLI lệch 2 mục; in tiếng Việt qua pipe khiến script sập với cp1252; và probe chạy python -I làm ẩn user site, nên không thấy PyYAML cài bằng --user. Fix bằng -E -P, giữ được bảo vệ không import code từ vault.
**Bài học:** Thử trên máy thật có đường dẫn, mã hoá và môi trường Python khác bắt được lỗi mà CI Linux không thấy.
**Artefact:** Báo cáo thử Windows (chụp phần tóm tắt, che đường dẫn).
