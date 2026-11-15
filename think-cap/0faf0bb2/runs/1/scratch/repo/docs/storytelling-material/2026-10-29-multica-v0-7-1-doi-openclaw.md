---
id: 2026-10-29-multica-v0-7-1-doi-openclaw
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3088", "claude:0faf0bb2#L3150"]
hook: "Khai man phiên bản để qua cửa, CLI chạy được nhưng gateway vẫn chết"
tension: cam_ma_van_lot
sides: ["Giả phiên bản để vượt rào kiểm tra", "Qua được cửa đầu, rồi gãy ở gateway: 0/4 tiêu chí"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica v0.7.1 đòi OpenClaw ≥ 2026.5.5, bản AICoworker đóng gói là 2026.3.13: spike trượt

**Bối cảnh:** Mục tiêu spike Multica + AICoworker: kiểm 4 tiêu chí gồm giữ SOUL, ghi ngược, tiếp nối session và workflow theo cột.
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối 'below the minimum supported version'. Thử khai man phiên bản bằng wrapper: CLI chạy được nhưng báo 'Include path escapes config directory' vì thiếu biến OPENCLAW_INCLUDE_ROOTS, gateway thất bại, và tiến trình thoát mà không có output. Kết quả: 0/4 tiêu chí đạt, dừng và liệt kê 3 đường đi tiếp.
**Bài học:** Giả phiên bản chỉ đẩy lỗi xuống tầng sâu hơn; kiểm ràng buộc phiên bản tối thiểu trước khi dựng spike.
**Artefact:** Bảng 4 tiêu chí đạt/trượt, kèm thông báo lỗi version đã rút gọn.
