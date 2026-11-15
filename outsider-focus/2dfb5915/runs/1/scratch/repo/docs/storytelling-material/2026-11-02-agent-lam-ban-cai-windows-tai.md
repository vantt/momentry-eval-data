---
id: 2026-11-02-agent-lam-ban-cai-windows-tai
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3282", "claude:2dfb5915#L3299"]
hook: "Bản cài Windows tự hạ gói vantt.4 đang dùng xuống vantt.3"
tension: giup_ma_hai
sides: ["Script cài thay gói để khớp bản ghim", "Gói mới hơn bị đè xuống bản cũ mà không ai hay"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent làm bản cài Windows: tải sai bản OHS và hạ cấp ngầm

**Bối cảnh:** Installer của `pkm` tải gói OHS và đè lên gói đã có trong thư mục của pkm.
**Chuyện gì xảy ra:** Nhánh gốc thay gói bất cứ khi nào phiên bản khác bản ghim, nên một gói vantt.4 đang dùng sẽ bị đè xuống vantt.3. Review tìm ra và sửa bằng so sánh phiên bản; gói đưa vào bằng `--ohs DIR` không bao giờ bị ghi đè.
**Bài học:** Installer nâng cấp phải so sánh phiên bản theo chiều tăng, không chỉ 'khác là thay'.
