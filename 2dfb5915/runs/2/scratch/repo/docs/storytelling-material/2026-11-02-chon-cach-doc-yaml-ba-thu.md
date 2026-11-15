---
id: 2026-11-02-chon-cach-doc-yaml-ba-thu
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, đảo quyết định]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L335", "claude:2dfb5915#L352"]
hook: "Ba thư viện đọc YAML, lệch từ 0 đến hơn 21 nghìn note"
tension: khac
sides: ["ba thư viện cùng đọc một định dạng", "kết quả lệch từ 0 đến 21 nghìn note"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chọn cách đọc YAML: ba thư viện Rust đều lệch hoặc panic so với PyYAML

**Bối cảnh:** Phase 02 chọn lớp đọc YAML cho index Rust.
**Chuyện gì xảy ra:** Trong bảng ứng viên, kết quả chênh rất lớn giữa các thư viện, từ 0 đến hơn 21 nghìn note lệch. Quyết định cuối là libyaml gốc cộng lớp tương thích, vì đây là cùng bản libyaml 0.2.5 mà PyYAML dùng.
**Bài học:** Chọn thư viện theo bằng chứng đối chiếu với bản gốc, không theo độ phổ biến.
**Artefact:** Bảng số lệch theo ứng viên.
