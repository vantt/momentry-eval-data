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
hook: "Bản cài Windows lặng lẽ đè vantt.4 xuống vantt.3"
tension: giup_ma_hai
sides: ["Cài đặt để đưa người dùng về đúng bản ghim", "Bản đang dùng bị hạ xuống bản cũ mà không báo"]
strength: 3
stakes: 2
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
