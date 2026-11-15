---
id: 2026-11-03-v0-1-0-ra-mat-release-d5ef
code: M-EEBA
aliases: [M-EEBA]
date: 2026-11-03
repo: repo
status: raw
signals: [khac, artefact_nhin_duoc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2968", "claude:ab9a1dd8#L2980", "claude:ab9a1dd8#L2981", "claude:ab9a1dd8#L2984", "claude:ab9a1dd8#L3018", "claude:ab9a1dd8#L3021", "claude:ab9a1dd8#L3025", "claude:ab9a1dd8#L3042"]
hook: "Phát hành v0.1.0: lệnh cài một dòng chạy được ngay lần đầu"
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

# v0.1.0 ra mắt: release workflow xanh từ đầu tới cuối, lệnh cài một dòng chạy được ngay lần đầu

**Bối cảnh:** User trước đó đã chọn push main, nhưng chưa chọn cắt tag. Lần này user chọn cắt v0.1.0.
**Chuyện gì xảy ra:** Agent kiểm bốn điều kiện: HEAD trùng origin/main, CI xanh trên commit đó, chưa có tag, VERSION khớp CHANGELOG. Sau khi tag, release.yml chạy: CI 9/9, tạo bản nháp, cài thử trên 3 OS, rồi công bố. Lệnh cài một dòng trong HOME tạm cài được 0.1.0, init báo Sẵn sàng, uninstall giữ dữ liệu.
**Bài học:** Trước khi cắt tag, kiểm HEAD, CI, VERSION và CHANGELOG bằng lệnh. Tag là việc công khai nên cần chọn riêng.
**Artefact:** Trang release v0.1.0 với danh sách tài sản: tarball, install.sh, install.ps1, checksums.txt.
