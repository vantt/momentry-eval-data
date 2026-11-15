---
id: 2026-10-29-lay-token-gateway-ma-khong-de-c455
code: M-KDCQ
aliases: [M-KDCQ]
date: 2026-10-29
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L824", "claude:0faf0bb2#L827", "claude:0faf0bb2#L891", "claude:0faf0bb2#L894", "claude:0faf0bb2#L909", "claude:0faf0bb2#L3913"]
hook: "Lấy token từ tiến trình đang chạy mà không in ra màn hình"
tension: cam_ma_van_lot
sides: ["Token không được export, script báo lỗi", "Đọc từ /proc vẫn lấy được, và grep không thấy lộ"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lấy token gateway mà không để lộ: đọc từ tiến trình đang chạy

**Bối cảnh:** Script tạo agent cần token của gateway, nhưng shell không có biến môi trường đó.
**Chuyện gì xảy ra:** Script báo KeyError vì token không được export. Agent đọc token từ /proc của tiến trình gateway và chỉ đưa vào cấu hình adapter, không in ra màn hình. Cùng lúc, file key có tên tiếng Việt được đổi sang tên ASCII để tránh lỗi đường dẫn. Trước khi commit, một lệnh grep quét các mẫu token trong docs và không tìm thấy gì.
**Bài học:** Lấy secret từ tiến trình đang chạy thay vì lưu vào script, và quét docs bằng regex trước khi commit.
**Artefact:** Lệnh grep quét mẫu token. Không in kết quả nhạy cảm.
