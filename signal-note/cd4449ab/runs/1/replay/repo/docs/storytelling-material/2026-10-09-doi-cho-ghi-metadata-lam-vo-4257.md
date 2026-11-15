---
id: 2026-10-09-doi-cho-ghi-metadata-lam-vo-4257
code: M-GHBV
aliases: [M-GHBV]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L276", "omp:cd4449ab#L286", "omp:cd4449ab#L288", "omp:cd4449ab#L459", "omp:cd4449ab#L468", "omp:cd4449ab#L507", "omp:cd4449ab#L534", "omp:cd4449ab#L543", "omp:cd4449ab#L552", "omp:cd4449ab#L561", "omp:cd4449ab#L576", "omp:cd4449ab#L621", "omp:cd4449ab#L633", "omp:cd4449ab#L642", "omp:cd4449ab#L651", "omp:cd4449ab#L669", "omp:cd4449ab#L675", "omp:cd4449ab#L699", "omp:cd4449ab#L753", "omp:cd4449ab#L795", "omp:cd4449ab#L873", "omp:cd4449ab#L954", "omp:cd4449ab#L990", "omp:cd4449ab#L999", "omp:cd4449ab#L1047", "omp:cd4449ab#L1050", "omp:cd4449ab#L1101", "omp:cd4449ab#L1119", "omp:cd4449ab#L1161", "omp:cd4449ab#L1188", "omp:cd4449ab#L1218", "omp:cd4449ab#L1221", "omp:cd4449ab#L1251", "omp:cd4449ab#L1278", "omp:cd4449ab#L1287", "omp:cd4449ab#L1290", "omp:cd4449ab#L1302", "omp:cd4449ab#L1305", "omp:cd4449ab#L1309", "omp:cd4449ab#L1311", "omp:cd4449ab#L1673", "omp:cd4449ab#L1675"]
hook: "Đổi chỗ ghi metadata, fixture vỡ qua cả 24 package"
tension: nho_ma_to
sides: ["chỉ đổi chỗ ghi metadata", "test đỏ lan qua app, cli, mcpserver, web"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi chỗ ghi metadata làm vỡ fixture qua 24 package

**Bối cảnh:** Đổi file metadata từ skill.meta.yaml sang .meta/skill.yaml, nhưng nhiều test vẫn tạo file cũ hoặc đọc đường cũ.
**Chuyện gì xảy ra:** Lần go test ./... đầu tiên đỏ ở migration. Trong đợt sửa, test đỏ lần lượt ở app, cli, mcpserver, web: hàng chục lần chạy đỏ. Golden của web được cập nhật bằng cờ -update. Kết thúc: go test ./... xanh với 24 package ok, 2 không có test.
**Bài học:** Khi đổi đường dẫn ghi, grep cả fixture test ngay từ đầu; đếm số file test còn nhắc đường cũ trước khi chạy.
**Artefact:** Bảng: package nào đỏ ở vòng nào.
