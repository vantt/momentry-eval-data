---
id: 2026-11-02-build-index-58-6-ms-xuong
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L941"]
hook: "Build index nhanh gần 2.8 lần, nhưng bản không đổi chỉ hơn 0.3 ms"
tension: khac
sides: ["build mới nhanh gần 2.8 lần, 58.6 xuống 21.2 ms", "build không đổi gần như ngang nhau, 2.4 so với 2.1 ms"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Build index: 58.6 ms xuống 21.2 ms

**Bối cảnh:** Đo build index đầy đủ trên vault tổng hợp, bản release, lấy median.
**Chuyện gì xảy ra:** Python mất 58.6 ms, Rust mất 21.2 ms, nhanh gần 2.8 lần. Bản build không đổi thì gần như ngang nhau: 2.4 ms so với 2.1 ms. Bộ so khớp chạy bản debug nên số đo ở đó chỉ mang tính tham khảo.
**Bài học:** Ghi rõ đo bằng bản release hay debug, và không đem số debug đi so với số release.
**Artefact:** Bảng hai cột Python và Rust, ghi rõ median và kiểu build.
