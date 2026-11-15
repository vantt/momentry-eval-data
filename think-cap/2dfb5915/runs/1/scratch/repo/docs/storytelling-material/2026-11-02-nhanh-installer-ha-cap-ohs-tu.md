---
id: 2026-11-02-nhanh-installer-ha-cap-ohs-tu
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3299"]
hook: "Installer 'nâng cấp' OHS lại hạ gói từ vantt.4 xuống vantt.3"
tension: giup_ma_hai
sides: ["Installer đảm bảo đúng bản ghim", "Gói mới hơn bị đưa về bản cũ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhánh installer hạ cấp OHS từ vantt.4 xuống vantt.3

**Bối cảnh:** Installer thay gói OHS khi phiên bản khác với bản ghim.
**Chuyện gì xảy ra:** Nhánh gốc thay gói khi phiên bản khác, nên gói mới hơn cũng bị đưa về bản ghim. Review phát hiện trước khi merge. Sửa: so phiên bản dạng X.Y.Z-vantt.N, chỉ nâng khi gói cũ hơn hoặc không rõ phiên bản; gói đưa vào bằng --ohs không bao giờ bị ghi đè. Có test cho cả hai.
**Bài học:** So phiên bản bằng phép so có thứ tự, không so chuỗi khác nhau.
**Artefact:** Không có.
