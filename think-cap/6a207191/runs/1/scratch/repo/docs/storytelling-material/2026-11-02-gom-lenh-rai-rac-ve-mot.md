---
id: 2026-11-02-gom-lenh-rai-rac-ve-mot
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L545", "claude:6a207191#L550", "claude:6a207191#L551", "claude:6a207191#L570"]
hook: "fgctl thiếu --version, nên giờ mọi CLI phải có chung một bộ lệnh"
tension: nho_ma_to
sides: ["Một cờ --version bị thiếu ở một công cụ", "Cả bộ lệnh, cờ và exit code chuẩn cho mọi CLI"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gom lệnh rải rác về một file: bộ lệnh chuẩn và cờ JSON chung cho mọi CLI

**Bối cảnh:** Người dùng hỏi về cú pháp lệnh update/upgrade, doctor, init. Các lệnh đã có nhưng rải rác nhiều file, chưa có quy định bộ lệnh chuẩn.
**Chuyện gì xảy ra:** Agent gom về common/07-command-surface.md. Upgrade được thêm làm alias của update. --version và version đều phải chạy, bài học từ fgctl thiếu --version. Các cờ chung --json, -y, --dry-run, -q, -v, NO_COLOR có cùng nghĩa ở mọi lệnh. Có bảng exit code chung: 0, 1, 2, và 10 cho update --check có bản mới. Các định nghĩa lệnh cũ trong UPD-01 và DOC-02 được trỏ về file này.
**Bài học:** Một CLI chuẩn chỉ nên có một nơi định nghĩa cú pháp. Các file khác chỉ trỏ tới, để không trùng và không lệch.
**Artefact:** Khối lệnh chuẩn khoảng 10 dòng, copy được.
