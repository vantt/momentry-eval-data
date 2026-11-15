---
id: 2026-11-02-may-audit-chi-doc-ma-vi-3c6e
code: M-5PV6
aliases: [M-5PV6]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L1029", "claude:2dfb5915#L1063", "claude:2dfb5915#L1078", "claude:2dfb5915#L1132"]
hook: "Hook chặn cargo build, audit vẫn tìm ra ba blocker"
tension: cam_ma_van_lot
sides: ["Hook chặn agent chạy binary", "Agent vẫn đọc mã và tìm ra ba blocker, nhưng báo sai một chi tiết"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Máy audit chỉ đọc mã vì hook chặn cargo build, và báo sai một chi tiết

**Bối cảnh:** Audit đóng gói theo skill, chạy song song với các phase khác.
**Chuyện gì xảy ra:** Hook của repo chặn lệnh cargo build và thư mục target, nên audit không chạy được binary và suy luận từ mã nguồn. Kết quả: ba blocker, trong đó vcruntime140.dll có thể làm pkm.exe không chạy trên máy Windows sạch. Báo cáo nói chưa có bằng chứng action chạy được, trong khi lần dispatch trước đã chạy thành công; chủ dự án chỉ ra và báo cáo được sửa.
**Bài học:** Kết quả đọc mã phải ghi rõ là chưa chạy thật, và kiểm lại bằng lịch sử trước khi kết luận.
