---
id: 2026-11-02-tu-ban-rc-1-toi-rc-3c6e
code: M-7XQ0
aliases: [M-7XQ0]
date: 2026-11-02
repo: repo
status: raw
signals: [artefact_nhin_duoc, rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L2536", "claude:2dfb5915#L3551", "claude:2dfb5915#L3585", "claude:2dfb5915#L3684", "claude:2dfb5915#L3929"]
hook: "Ba bản rc, bản nào cũng đủ checksum, nhưng rerun trả HTTP 500"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ bản rc.1 tới rc.3: mỗi bản có checksums, và một lần job bị huỷ vì chờ runner quá lâu

**Bối cảnh:** Mỗi bản pre-release có 7 file gồm 4 binary, hai script cài và checksums.txt; agent tải về và kiểm sha256.
**Chuyện gì xảy ra:** rc.1 phát hành có đủ 7 file, sha256 khớp. rc.2 bị job macOS Intel bị huỷ vì chờ runner 15 phút, rerun thì được; API rerun trả HTTP 500 lần đầu. rc.3 ra từ nhánh phase 17, 6 file trong checksum đều khớp.
**Bài học:** Kiểm sha256 từ file tải về thật sau mỗi lần phát hành, và chuẩn bị rerun vì runner có thể chờ lâu.
**Artefact:** Danh sách 7 file của Release và kết quả kiểm checksum.
