---
id: 2026-11-03-cat-v0-1-0-lenh-cai-d5ef
code: M-Y8FS
aliases: [M-Y8FS]
date: 2026-11-03
repo: repo
status: raw
signals: [artefact_nhin_duoc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2968", "claude:ab9a1dd8#L2981", "claude:ab9a1dd8#L2994", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3021", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
hook: "Trước khi công bố v0.1.0, agent cài thử bằng đúng lệnh curl thật"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cắt v0.1.0: lệnh cài một dòng chạy được từ GitHub thật

**Bối cảnh:** Lệnh cài một dòng trong README chỉ chạy được sau tag đầu tiên, và release là việc công khai.
**Chuyện gì xảy ra:** Trước khi tag, agent kiểm HEAD trùng origin/main, CI trên commit đó xanh, chưa có tag, VERSION và CHANGELOG khớp. Sau khi push tag, release.yml chạy CI chín ô, tạo bản nháp, cài thử bản nháp trên ba hệ điều hành, rồi mới công bố. Agent chạy đúng lệnh curl rồi sh trong HOME tạm: cài được 0.1.0, init báo sẵn sàng, uninstall gỡ sạch và giữ dữ liệu.
**Bài học:** Lệnh cài trong README là một hợp đồng với người dùng; sau khi phát hành, thử lại đúng lệnh đó từ HOME trống, đừng chỉ tin workflow xanh.
**Artefact:** Trang release với danh sách asset: tarball, install.sh, install.ps1, checksums.txt.
