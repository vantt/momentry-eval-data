---
id: 2026-11-03-chay-thu-host-bang-khoa-gia-d5ef
code: M-ZDEW
aliases: [M-ZDEW]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3881", "claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3918", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3935"]
hook: "Thử host bằng khoá giả, chặn mạng để không gửi gì ra ngoài"
tension: none
sides: []
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy thử host bằng khoá giả và namespace mạng rỗng để không gửi yêu cầu ra ngoài

**Bối cảnh:** Kiểm hook pi, omp, agy trên máy thật mà không gọi API thật.
**Chuyện gì xảy ra:** Chạy pi và omp với khoá giả, nhận lỗi 401 Incorrect API key. Vì pi và omp là hàm shell bọc, agent tìm đường dẫn thật. Với agy, agent chặn mạng hẳn bằng unshare -rn để chắc không có yêu cầu nào đi ra ngoài.
**Bài học:** Để chạy host thật mà không gửi dữ liệu ra ngoài: khoá giả cho lỗi nhanh, còn namespace mạng rỗng đảm bảo không có yêu cầu nào đi.
**Artefact:** Trích thông báo 401 đã che khoá.
