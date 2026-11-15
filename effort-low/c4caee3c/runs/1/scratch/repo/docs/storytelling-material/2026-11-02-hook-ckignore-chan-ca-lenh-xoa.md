---
id: 2026-11-02-hook-ckignore-chan-ca-lenh-xoa
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746"]
hook: "Hook chặn cả lệnh ls chỉ vì có chữ build"
tension: cam_ma_van_lot
sides: ["Hook sinh ra để chặn lệnh nguy hiểm", "Nó chặn luôn ls và lệnh dọn dẹp vô hại"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook .ckignore chặn cả lệnh xoá node_modules lẫn chữ build

**Bối cảnh:** Môi trường có hook kiểm tra lệnh shell. Agent dùng lệnh thường ngày để dọn dẹp và kiểm tra.
**Chuyện gì xảy ra:** Hook từ chối lệnh có chứa node_modules hoặc build, kể cả khi lệnh chỉ là ls hay rm dọn thư mục đã xong. Có lúc agent phải chuyển sang công cụ Edit để sửa file vì mọi lệnh có chữ build đều bị chặn. Các lần chặn xảy ra nhiều lần trong phiên.
**Bài học:** Hook chặn theo từ khoá quá rộng sẽ buộc agent đi đường vòng; nên khai báo ngoại lệ theo mẫu đường dẫn, không theo chữ.
**Artefact:** Thông báo chặn của hook. Không cần che.
