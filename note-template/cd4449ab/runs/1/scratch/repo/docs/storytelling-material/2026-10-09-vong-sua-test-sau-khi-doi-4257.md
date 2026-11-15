---
id: 2026-10-09-vong-sua-test-sau-khi-doi-4257
code: M-G98K
aliases: [M-G98K]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L667", "omp:cd4449ab#L669", "omp:cd4449ab#L1309", "omp:cd4449ab#L1311"]
hook: "Đổi schema một lần, 24 package test phải sửa từng vòng"
tension: nho_ma_to
sides: ["Một thay đổi schema", "Test đỏ ở migration, web, app, cli, mcpserver, sửa từng vòng"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vòng sửa test sau khi đổi schema: 24 package, lặp đi lặp lại

**Bối cảnh:** Chuyển metadata skill từ skill.meta.yaml sang .meta/skill.yaml làm nhiều fixture test cũ hỏng cùng lúc.
**Chuyện gì xảy ra:** go test ./... đỏ lần đầu ở L669. Sau nhiều vòng sửa fixture (migration, mutation, web golden, app, cli, mcpserver), lần chạy cuối là 24 package ok và 2 package không có test (L1311). Mỗi vòng sửa một chỗ rồi chạy lại.
**Bài học:** Khi đổi định dạng file, liệt kê toàn bộ fixture bị ảnh hưởng trước khi sửa từng test theo lỗi.
**Artefact:** Chuỗi log go test đỏ rồi xanh qua các vòng; che đường dẫn cá nhân.
