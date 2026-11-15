---
id: 2026-10-21-rang-buoc-chinh-sach-cho-hoi
date: 2026-10-21
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3453", "claude:9514b261#L3489", "claude:9514b261#L3518"]
hook: "Cả năm lệnh gọi qua kiểm chính sách chỉ đọc, nhưng chưa chứng minh cách ly lúc chạy"
tension: cam_ma_van_lot
sides: ["Posture read-only, host-write-denied, năm invocation đều qua kiểm", "Mới là kiểm chính sách, chưa chứng minh cách ly khi chạy"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ràng buộc chính sách cho hội đồng: chỉ đọc và chặn ghi trước khi giao việc

**Bối cảnh:** Trước khi mở hội đồng, agent muốn chắc các ghế không ghi được vào repo.
**Chuyện gì xảy ra:** Agent kiểm posture read-only, policy host-write-denied ở chế độ required, và cả năm invocation đều qua kiểm resolvePostureInvocation. Agent nói rõ đây chỉ là kiểm chính sách, chưa chứng minh cách ly lúc chạy.
**Bài học:** Kiểm chính sách ghi trước khi giao việc cho model bên ngoài, và ghi rõ đây không thay cho kiểm cách ly thật.
**Artefact:** Kết quả kiểm posture: posture, policy, mode, hostWrite, và ok của từng invocation.
