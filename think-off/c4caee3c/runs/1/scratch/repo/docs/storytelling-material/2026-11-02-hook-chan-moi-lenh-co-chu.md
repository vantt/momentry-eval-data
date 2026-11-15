---
id: 2026-11-02-hook-chan-moi-lenh-co-chu
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L75", "claude:c4caee3c#L612", "claude:c4caee3c#L791", "claude:c4caee3c#L3746", "claude:c4caee3c#L3749"]
hook: "Hook chặn cả lệnh chỉ đọc đường dẫn, vì tên thư mục có chữ build"
tension: cam_ma_van_lot
sides: ["Hook chặn lệnh build nguy hiểm", "Nó chặn luôn lệnh vô hại chỉ vì có chữ 'build' trong đường dẫn"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hook chặn mọi lệnh có chữ build, kể cả khi chỉ đọc đường dẫn

**Bối cảnh:** Môi trường có hook scout-block và file .ckignore. Hook chặn lệnh có chữ build hoặc node_modules trong đường dẫn.
**Chuyện gì xảy ra:** Lệnh kiểm tra gói bị chặn vì tên thư mục build, và lệnh xoá node_modules trong worktree cũng bị chặn. Agent chuyển sang công cụ sửa file thay cho lệnh shell để sửa test. Đây là ràng buộc của môi trường, không phải lỗi trong mã.
**Bài học:** Đặt tên thư mục đầu ra khác hoặc có kế hoạch cho hook; đừng để công cụ chặn chặn luôn việc kiểm tra.
**Artefact:** Thông báo của hook (đã bỏ đường dẫn).
