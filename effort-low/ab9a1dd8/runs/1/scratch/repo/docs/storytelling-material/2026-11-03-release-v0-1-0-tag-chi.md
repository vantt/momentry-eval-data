---
id: 2026-11-03-release-v0-1-0-tag-chi
date: 2026-11-03
repo: repo
status: raw
signals: [artefact nhìn được]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2961", "claude:ab9a1dd8#L2968", "claude:ab9a1dd8#L2980", "claude:ab9a1dd8#L2984", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3021", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
hook: "Tag v0.1.0 chỉ sau khi CI xanh, rồi curl thử từ GitHub thật"
tension: none
sides: []
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release v0.1.0: tag chỉ sau khi CI xanh đúng commit, rồi thử lệnh cài một dòng từ GitHub thật

**Bối cảnh:** README có lệnh cài một dòng nhưng chưa có release nào nên lệnh chưa chạy được. Người dùng đã đồng ý cắt bản công khai.
**Chuyện gì xảy ra:** Agent kiểm HEAD trùng origin/main, CI xanh trên commit đó, chưa có tag và VERSION khớp CHANGELOG, rồi mới tạo tag v0.1.0. Workflow release chạy qua CI 9 tổ hợp, tạo bản nháp, cài thử trên ba hệ điều hành rồi mới công bố. Sau đó lệnh curl trong README được chạy thật trong HOME tạm và cài đúng phiên bản.
**Bài học:** Lệnh cài trong README chỉ đáng tin khi đã chạy đúng lệnh đó từ nguồn công khai trong môi trường sạch.
**Artefact:** Trang release với danh sách tài sản, và output terminal của lệnh cài một dòng. Che đường dẫn HOME tạm.
