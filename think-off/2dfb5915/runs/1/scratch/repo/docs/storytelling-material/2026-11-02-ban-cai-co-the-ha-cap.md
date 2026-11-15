---
id: 2026-11-02-ban-cai-co-the-ha-cap
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3286", "claude:2dfb5915#L3299"]
hook: "Bản cài tự hạ gói OHS mới về bản cũ"
tension: giup_ma_hai
sides: ["cài đặt để đưa máy về đúng bản ghim", "máy có gói mới hơn bị đổi xuống gói cũ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Bản cài có thể hạ cấp gói OHS mới về bản cũ

**Bối cảnh:** Nhánh ghim gói OHS thay gói mỗi khi phiên bản khác với bản ghim.
**Chuyện gì xảy ra:** Máy đang có gói mới hơn bản ghim sẽ bị đổi về gói cũ. Sửa: so phiên bản theo dạng X.Y.Z kèm hậu tố và chỉ nâng khi gói cũ hơn hoặc không rõ phiên bản. Gói đưa vào bằng cờ --ohs không bao giờ bị ghi đè.
**Bài học:** Logic nâng cấp chỉ được đi một chiều. Viết test cho cả hai hướng.
**Artefact:** Không có.
