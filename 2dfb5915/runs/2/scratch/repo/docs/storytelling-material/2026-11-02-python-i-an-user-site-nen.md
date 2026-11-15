---
id: 2026-11-02-python-i-an-user-site-nen
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3242", "claude:2dfb5915#L3275"]
hook: "Cờ cô lập Python ẩn luôn PyYAML của người dùng trên Windows"
tension: giup_ma_hai
sides: ["cờ -I để cô lập cho an toàn", "probe không thấy PyYAML đã cài"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Python -I ẩn user site nên probe không thấy PyYAML trên Windows

**Bối cảnh:** Máy Windows thử handoff, PyYAML cài bằng pip --user.
**Chuyện gì xảy ra:** Cờ -I là -E -s -P, và -s bỏ user site là nơi pip --user cài. Đổi sang -E -P: vẫn bỏ biến PYTHON*, vẫn không nạp code từ thư mục vault, và thấy được PyYAML của người dùng. -P cần Python 3.11 trở lên.
**Bài học:** Hiểu rõ từng cờ cô lập của interpreter trước khi dùng.
**Artefact:** Không.
