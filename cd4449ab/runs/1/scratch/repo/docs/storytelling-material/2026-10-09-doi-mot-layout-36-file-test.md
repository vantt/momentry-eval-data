---
id: 2026-10-09-doi-mot-layout-36-file-test
date: 2026-10-09
repo: repo
status: raw
signals: ["1"]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1101", "omp:cd4449ab#L1218", "omp:cd4449ab#L1287", "omp:cd4449ab#L1303", "omp:cd4449ab#L1311", "omp:cd4449ab#L1409", "omp:cd4449ab#L1412", "omp:cd4449ab#L1673"]
hook: "Đổi một layout, 36 file test phải sửa theo"
tension: nho_ma_to
sides: ["Một thay đổi layout", "36 file, +1048 dòng, test đỏ rồi xanh"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi một layout, 36 file test theo sau

**Bối cảnh:** Chuyển định dạng skill.meta.yaml sang .meta/skill.yaml chạm nhiều package.
**Chuyện gì xảy ra:** Commit writers 5a01750 chạm 36 file, +1048 và -186 dòng. Sau đó các test trong internal/app, delivery/cli, mcpserver, web và mutation phải sửa theo, qua nhiều lần go test ./... đỏ rồi xanh. Golden của web được regenerate bằng -update. Trạng thái cuối là 24 package ok và 2 package không có test.
**Bài học:** Trước khi đổi định dạng file gốc, grep mọi nơi đọc và ghi để biết trước số file test sẽ đổi, rồi cập nhật fixture trong một lượt.
**Artefact:** Bảng 36 file theo nhóm package. Không cần chụp.
