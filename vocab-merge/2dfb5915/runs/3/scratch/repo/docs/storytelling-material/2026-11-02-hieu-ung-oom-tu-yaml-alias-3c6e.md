---
id: 2026-11-02-hieu-ung-oom-tu-yaml-alias-3c6e
code: M-BRNY
aliases: [M-BRNY]
date: 2026-11-02
repo: repo
status: raw
signals: ["số trước, số sau", nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L607", "claude:2dfb5915#L811", "claude:2dfb5915#L819", "claude:2dfb5915#L844"]
hook: "338 byte YAML đủ ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["Một tệp YAML chỉ 338 byte", "Alias bomb nở ra 1,45 GB RAM, và lỗ hổng nằm sẵn trong đặc tả Python"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hiệu ứng OOM từ YAML alias bomb: 338 byte làm 1,45 GB RAM

**Bối cảnh:** Review phát hiện một note 338 byte với alias lồng nhau ×10 mỗi tầng sinh ra 11,1 triệu prop, 1,45 GB RSS trong Rust. Python cũng bị, nhưng tốn 877 MB ở cùng độ sâu.
**Chuyện gì xảy ra:** Đây là lỗ hổng từ chính đặc tả Python, không phải lỗi mới của port. Sửa bằng ngân sách 1 triệu prop và 64 MiB văn bản cho mỗi note; vượt ngân sách thì ghi MemoryError và coi là lệch có chủ ý.
**Bài học:** Khi port, đừng chỉ sao chép hành vi đặc tả: kiểm xem có lỗ hổng tài nguyên không và ghi rõ đó là lệch có chủ ý.
**Artefact:** Bảng RSS theo độ sâu alias; không chứa nội dung note.
