---
id: 2026-11-02-hook-chan-cargo-build-audit-phai
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1063", "claude:2dfb5915#L1078", "claude:2dfb5915#L1237"]
hook: "Binary chạy tốt trên máy dev, nhưng máy Windows sạch thiếu một DLL"
tension: tuong_ma_hoa_ra
sides: ["Binary chạy ổn trên máy dev", "Máy Windows sạch thiếu vcruntime140.dll"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn cargo build, audit phải suy luận từ mã nguồn

**Bối cảnh:** Agent audit đóng gói chỉ được đọc. Hook của repo chặn cargo build và truy cập thư mục target.
**Chuyện gì xảy ra:** Audit không chạy được binary nên mọi phát hiện về binary đều suy từ mã. Phát hiện chặn: pkm.exe cần vcruntime140.dll mà nhiều máy Windows sạch không có. Sửa bằng CRT tĩnh và bước CI dùng dumpbin kiểm DLL còn lại. Kết quả audit: 3 lỗi chặn, 9 quan trọng, 8 nên có.
**Bài học:** Hook an toàn vẫn có thể làm agent mù; báo cáo cần ghi rõ kết quả nào là đọc mã, kết quả nào là chạy thật.
**Artefact:** Bảng xếp mức lỗi 3, 9, 8.
