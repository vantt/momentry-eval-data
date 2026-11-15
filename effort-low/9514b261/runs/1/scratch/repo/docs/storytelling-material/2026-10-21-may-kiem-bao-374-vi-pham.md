---
id: 2026-10-21-may-kiem-bao-374-vi-pham
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L95", "claude:9514b261#L530", "claude:9514b261#L542"]
hook: "Máy kiểm bắt 374 lỗi, nhưng không ai chạy nó"
tension: cam_ma_van_lot
sides: ["Có máy kiểm báo 374 vi phạm", "Chỉ test của chính script chạy trong npm test, với đội coi như không có"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy kiểm báo 374 vi phạm nhưng không chạy ở đâu cả

**Bối cảnh:** Một máy kiểm ngăn tên test nhúng mã quyết định nội bộ. Nó có code, có test riêng, nhưng không được nối vào lệnh test chính.
**Chuyện gì xảy ra:** Máy kiểm báo 374 vi phạm hiện có, nhưng chỉ test của chính script chạy trong npm test. Với đội, nó như không tồn tại. Khi nối vào, phải làm mới baseline một lần trước, và phải có test dây nối chạy trên repo thật.
**Bài học:** Một máy kiểm chưa nằm trong đường chạy thường xuyên thì chưa phải máy kiểm. Đo xem nó có chạy ở đâu trước khi tin nó.
**Artefact:** Sơ đồ đường chạy: lệnh test, pre-commit, cron, và ô nào trống cho máy kiểm.
