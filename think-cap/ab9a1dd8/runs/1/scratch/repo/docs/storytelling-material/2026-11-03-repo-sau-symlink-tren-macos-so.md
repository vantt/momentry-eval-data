---
id: 2026-11-03-repo-sau-symlink-tren-macos-so
date: 2026-11-03
repo: repo
status: raw
signals: ["2"]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2338", "claude:ab9a1dd8#L2339", "claude:ab9a1dd8#L2464", "claude:ab9a1dd8#L2515", "claude:ab9a1dd8#L2532", "claude:ab9a1dd8#L2535"]
hook: "macOS không thấy phiên nào vì /var là lối tắt của /private/var"
tension: nho_ma_to
sides: ["một symlink /var trỏ tới /private/var", "test không thấy phiên nào, transcript biến mất"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Repo sau symlink trên macOS: so khớp đường dẫn làm mất transcript

**Bối cảnh:** Test scan tìm phiên của repo trong HOME. Trên runner macOS, repo nằm sau symlink.
**Chuyện gì xảy ra:** Một test trên macOS không thấy phiên nào. Nguyên nhân là /var là symlink tới /private/var, nên so khớp đường dẫn thất bại. Agent sửa bằng cách so khớp theo cả hai dạng đường dẫn, dùng realpath, và macOS xanh.
**Bài học:** So khớp đường dẫn phải dùng realpath cả hai phía. Trên macOS, /var là symlink tới /private/var.
**Artefact:** Đầu ra test macOS trước và sau khi sửa.
