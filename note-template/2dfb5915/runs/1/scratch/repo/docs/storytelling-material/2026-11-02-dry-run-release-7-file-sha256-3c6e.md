---
id: 2026-11-02-dry-run-release-7-file-sha256-3c6e
code: M-PM9B
aliases: [M-PM9B]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: Quy trình thử release bằng workflow_dispatch để kiểm trước khi gắn tag thật.
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L251", "claude:2dfb5915#L257", "claude:2dfb5915#L267", "claude:2dfb5915#L2536"]
hook: "Chạy thử phát hành: 7 file, mọi checksum khớp, chưa tạo Release"
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

# Dry run release: 7 file, sha256 khớp, không tạo Release thật

**Bối cảnh:** Workflow release dựng bốn binary và hai script cài.
**Chuyện gì xảy ra:** Lần dispatch đầu ra đủ bốn binary, mọi sha256 khớp, và không tạo Release. Sau đó bản rc thật được đăng với 7 file và agent tải về kiểm lại từng checksum.
**Bài học:** Chạy release bằng dispatch trước khi đánh tag, và kiểm checksum bằng file tải về.
