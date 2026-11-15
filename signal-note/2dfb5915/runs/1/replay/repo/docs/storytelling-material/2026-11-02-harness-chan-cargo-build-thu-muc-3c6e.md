---
id: 2026-11-02-harness-chan-cargo-build-thu-muc-3c6e
code: M-MZ7C
aliases: [M-MZ7C]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L1078", "claude:2dfb5915#L1460"]
hook: "Agent audit đóng gói không được build, nên phải đoán binary từ mã nguồn"
tension: cam_ma_van_lot
sides: ["Harness chặn cargo build và thư mục target", "Phát hiện về binary vẫn phải đưa ra, chỉ ghi là chưa chạy thật"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Harness chặn cargo build, thư mục target và lệnh sleep chuỗi: audit đóng gói phải suy từ đọc code

**Bối cảnh:** Môi trường có hook riêng chặn lệnh build và truy cập vào target, và chặn lệnh sleep nối tiếp để chờ.
**Chuyện gì xảy ra:** Agent audit đóng gói không dựng được binary, nên các phát hiện về binary (phụ thuộc DLL vcruntime140, thiếu installer) suy ra từ mã nguồn và được ghi là chưa chạy thật. Lệnh chờ sleep 30 nối với lệnh watch bị chặn, phải chuyển sang vòng until hoặc chạy nền.
**Bài học:** Khi hook chặn công cụ kiểm chứng, ghi rõ kết luận là đọc code hay đã chạy, và đổi cách chờ theo đúng quy định của harness.
**Artefact:** Đoạn báo cáo ghi phần kiểm bằng đọc code và phần đã chạy thật.
