---
id: 2026-11-03-tham-do-pi-va-omp-that
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc, khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3881", "claude:ab9a1dd8#L3902", "claude:ab9a1dd8#L3910", "claude:ab9a1dd8#L3913", "claude:ab9a1dd8#L3931", "claude:ab9a1dd8#L3935"]
hook: "Khoá API giả vẫn gọi ra mạng thật và nhận 401"
tension: cam_ma_van_lot
sides: ["khoá giả, tưởng không đi đâu", "host vẫn gọi API và báo 401"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thăm dò pi và omp thật: chặn mạng trước khi chạy

**Bối cảnh:** Máy có sẵn pi, omp và agy. Cần xác nhận hook được gọi khi phiên khởi động mà không gửi yêu cầu nào ra ngoài.
**Chuyện gì xảy ra:** Chạy omp với khoá giả, output vẫn cho thấy host đã gọi API và báo 401 khoá không hợp lệ. Vì vậy agent chuyển sang chạy trong namespace mạng rỗng bằng unshare để chắc không có yêu cầu nào đi ra ngoài.
**Bài học:** Khi thăm dò CLI có gọi mạng, hãy chặn mạng ở mức hệ điều hành trước; khoá giả không đủ để chặn.
**Artefact:** Dòng 401 Incorrect API key trong output, không chứa bí mật.
