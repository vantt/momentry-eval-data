---
id: 2026-10-09-migration-co-marker-phien-ban-ro-4257
code: M-TZ2K
aliases: [M-TZ2K]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [outsider]
lines: ["omp:cd4449ab#L1686", "omp:cd4449ab#L1690", "omp:cd4449ab#L2551", "omp:cd4449ab#L2960", "omp:cd4449ab#L2963"]
hook: "Migration có marker, preview và receipt thay vì script chạy một lần"
tension: none
sides: []
strength: 0
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration có marker phiên bản rõ ràng (file schema-version), mỗi bước là một hàm đăng ký theo thứ tự, có bước preview, rồi apply với receipt có thể replay.

**Chuyện gì xảy ra:** Migration có marker phiên bản rõ ràng (file schema-version), mỗi bước là một hàm đăng ký theo thứ tự, có bước preview, rồi apply với receipt có thể replay.
**Góc người ngoài:** cách làm phổ biến là Viết script migrate một lần, đoán trạng thái cũ theo cấu trúc file, không có marker hay receipt; ở đây khác ở Chính marker phiên bản quyết định code nào coi thư mục .meta là dữ liệu hub, nên v1/v2 và v3 xử lý khác nhau. Người đọc sẽ muốn biết vì sao phải thiết kế như vậy và cách test từng bước.
