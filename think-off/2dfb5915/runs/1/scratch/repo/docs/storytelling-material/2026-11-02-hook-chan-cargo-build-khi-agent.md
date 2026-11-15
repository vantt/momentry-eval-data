---
id: 2026-11-02-hook-chan-cargo-build-khi-agent
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L1078"]
hook: "Agent kiểm packaging nhưng bị chặn cargo build, không dựng được binary"
tension: cam_ma_van_lot
sides: ["agent được giao kiểm tra packaging", "hook chặn dựng binary, kết luận chỉ từ đọc mã"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn cargo build khi agent kiểm packaging

**Bối cảnh:** Agent audit đóng gói chạy ở chế độ chỉ đọc.
**Chuyện gì xảy ra:** Hook scout-block chặn lệnh cargo build và truy cập thư mục target, nên agent không dựng được binary. Mọi kết luận về binary, ví dụ thiếu DLL, chỉ đến từ đọc mã và chưa được chạy thật. Muốn cho phép cần thêm ngoại lệ vào file ignore của hook.
**Bài học:** Báo cáo kiểm tra phải ghi rõ kiểm nào đã chạy thật, kiểm nào chỉ suy từ mã.
**Artefact:** Không có.
