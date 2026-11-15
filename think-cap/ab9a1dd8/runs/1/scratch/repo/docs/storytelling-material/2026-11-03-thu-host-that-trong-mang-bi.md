---
id: 2026-11-03-thu-host-that-trong-mang-bi
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3932", "claude:ab9a1dd8#L3935"]
hook: "Khoá giả vẫn báo 'Incorrect API key': nó đã gọi ra ngoài"
tension: cam_ma_van_lot
sides: ["khoá giả, tưởng không gọi được API", "vẫn bị báo sai khoá, tức là đã cố gọi ra ngoài"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử host thật trong mạng bị ngắt: unshare chặn mọi request ra ngoài

**Bối cảnh:** Thử pi và omp thật trên máy, với khoá API giả. Hai công cụ này có thể gọi mạng.
**Chuyện gì xảy ra:** omp báo 'Incorrect API key' với khoá giả, cho thấy nó đã cố gọi API. Agent chạy lại qua unshare -rn, namespace mạng rỗng, để chắc không có request nào ra ngoài. Hook vẫn ghi được log cục bộ.
**Bài học:** Khi thử công cụ thật có thể gọi API, ngắt mạng bằng namespace để chắc không có yêu cầu nào ra ngoài.
**Artefact:** Không có artefact.
