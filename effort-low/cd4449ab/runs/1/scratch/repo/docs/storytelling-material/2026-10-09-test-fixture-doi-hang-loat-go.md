---
id: 2026-10-09-test-fixture-doi-hang-loat-go
date: 2026-10-09
repo: repo
status: raw
signals: [số trước sau, khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3622", "omp:cd4449ab#L3683", "omp:cd4449ab#L3695", "omp:cd4449ab#L3749", "omp:cd4449ab#L3930", "omp:cd4449ab#L3932"]
hook: "Mỗi vòng sửa-chạy mất 22 giây, còn fixture gọi sai tên input"
tension: nho_ma_to
sides: ["fixture chỉ sai tên input", "test fail nhiều lần, mỗi vòng 9–22 giây"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test fixture đổi hàng loạt: go test internal/app mất 9–22 giây mỗi lần

**Bối cảnh:** Sau khi bỏ skill.meta.yaml cũ, hàng chục file test phải đổi fixture sang .meta/skill.yaml.
**Chuyện gì xảy ra:** Số file thay đổi chưa commit lên tới 49 trước một lần commit, và giảm dần còn 35. Mỗi lần chạy go test ./internal/app mất khoảng 9 đến 22 giây, nên một vòng sửa-chạy kéo dài. Các test mcpserver fail nhiều lần vì fixture gọi đúng tool nhưng sai tên input.
**Bài học:** Đếm số file test cần đổi trước khi bắt đầu, và chạy đúng gói test thay vì cả repo mỗi lần.
**Artefact:** Bảng thời gian chạy go test theo gói và số vòng sửa.
