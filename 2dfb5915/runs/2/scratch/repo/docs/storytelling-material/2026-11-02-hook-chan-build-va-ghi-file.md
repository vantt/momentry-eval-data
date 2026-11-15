---
id: 2026-11-02-hook-chan-build-va-ghi-file
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L506", "claude:2dfb5915#L1078", "claude:2dfb5915#L1460"]
hook: "Hook an toàn chặn build, agent audit chỉ đọc được mã nguồn"
tension: giup_ma_hai
sides: ["hook chặn để an toàn", "audit không chạy được binary, chỉ đoán từ mã"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn build và ghi file, audit chỉ đọc được mã nguồn

**Bối cảnh:** Repo có hook scout-block và harness chặn một số lệnh.
**Chuyện gì xảy ra:** Hook chặn cargo build và truy cập thư mục target, nên agent audit đóng gói chỉ suy ra lỗi từ mã nguồn, chưa chạy binary. Một lệnh ghi nhật ký quyết định bị chặn vì đường dẫn chứa chữ build, phải ghi qua file tạm. Harness chặn lệnh sleep nối nhiều lần, phải dùng cơ chế chờ có điều kiện.
**Bài học:** Hook bảo vệ hợp lý vẫn có thể làm đứt vòng kiểm chứng. Ghi rõ kết luận nào chưa chạy thật để người đọc biết.
**Artefact:** Không.
