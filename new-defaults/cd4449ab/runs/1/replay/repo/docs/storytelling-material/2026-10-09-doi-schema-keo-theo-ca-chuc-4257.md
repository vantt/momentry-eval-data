---
id: 2026-10-09-doi-schema-keo-theo-ca-chuc-4257
code: M-GR93
aliases: [M-GR93]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1086", "omp:cd4449ab#L1087", "omp:cd4449ab#L1089", "omp:cd4449ab#L1290", "omp:cd4449ab#L1303", "omp:cd4449ab#L1305", "omp:cd4449ab#L1356", "omp:cd4449ab#L1359", "omp:cd4449ab#L2845", "omp:cd4449ab#L2860", "omp:cd4449ab#L2887", "omp:cd4449ab#L2888", "omp:cd4449ab#L2890", "omp:cd4449ab#L2891"]
hook: "Đổi một số version, 49 file thay đổi lan qua nhiều package"
tension: nho_ma_to
sides: ["Chỉ đổi một số version", "49 file chưa stage, nhiều vòng sửa"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đổi schema kéo theo cả chục fixture, golden cập nhật bằng -update

**Bối cảnh:** Bump version schema lên v3 làm các test CLI, web và evaluation đỏ, vì fixture còn ghi version 2 hoặc layout cũ.
**Chuyện gì xảy ra:** Cây làm việc tăng lên 49 file chưa stage rồi còn 35 file. Golden được regenerate bằng flag -update, và manifest evaluation được sửa tay. Để tìm nguyên nhân, agent dùng git log -S và tìm ra commit đổi digest catalog. Nhiều vòng sửa vì cùng một thay đổi version lan qua nhiều package.
**Bài học:** Tách commit đổi schema khỏi commit cập nhật fixture, và diff golden trước khi chạy -update để không che mất regression.
**Artefact:** Bảng số file đổi theo package trước và sau khi bump version.
