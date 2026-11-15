---
id: 2026-10-09-doi-writer-meta-keo-theo-test-4257
code: M-VAK8
aliases: [M-VAK8]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L669", "omp:cd4449ab#L675", "omp:cd4449ab#L699", "omp:cd4449ab#L753", "omp:cd4449ab#L795", "omp:cd4449ab#L873", "omp:cd4449ab#L954", "omp:cd4449ab#L990", "omp:cd4449ab#L999", "omp:cd4449ab#L1050", "omp:cd4449ab#L1174", "omp:cd4449ab#L1218", "omp:cd4449ab#L1287", "omp:cd4449ab#L2204", "omp:cd4449ab#L2234", "omp:cd4449ab#L2249", "omp:cd4449ab#L2255", "omp:cd4449ab#L2294"]
hook: "Đổi cách ghi một file meta, test đỏ liên tiếp 8 lượt"
tension: nho_ma_to
sides: ["Chỉ đổi nơi ghi một file nhỏ", "Test đỏ cả ba package, riêng một package 8 lượt"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi writer .meta kéo theo test app/cli/mcp đỏ cả chục lần

**Bối cảnh:** Sau khi writer chuyển sang .meta/skill.yaml, nhiều test cũ vẫn đọc skill.meta.yaml hoặc mong provenance.
**Chuyện gì xảy ra:** go test ./... đỏ nhiều lần ở internal/app, internal/skill và internal/delivery/cli. Ví dụ: test ghi skill mẫu bằng skill.meta.yaml, test backfill đỏ vì ghi sai thứ tự xác nhận. internal/app đỏ khoảng 8 lượt liên tiếp. Phải sửa helper trong test trước rồi mới sửa code.
**Bài học:** Khi đổi nơi ghi dữ liệu, sửa helper test trước. Nhiều lỗi chỉ là fixture còn trỏ vào đường cũ.
**Artefact:** Bảng gói test theo số lượt đỏ.
