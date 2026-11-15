---
id: 2026-10-29-paperclip-lech-phien-ban-giao-thuc
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L919", "claude:0faf0bb2#L947", "claude:0faf0bb2#L959", "claude:0faf0bb2#L987", "claude:0faf0bb2#L1016", "claude:0faf0bb2#L1021", "claude:0faf0bb2#L1036"]
hook: "Commit ghi 'không đổi giao thức' làm cả ba agent kẹt, vá một con số là xong"
tension: nho_ma_to
sides: ["commit tự nhận không đổi nội dung giao thức, chỉ nâng v3 lên v4", "cả ba agent kẹt ở verifying, sửa minProtocol thành 3 ở 3 chỗ mới chạy lại"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Paperclip: lệch phiên bản giao thức làm agent kẹt ở verifying, vá một dòng trong bản đã cài

**Bối cảnh:** Spike chạy Paperclip (control plane) điều phối agent trên AICoworker/OpenClaw trên cùng máy. Agent được tạo qua API nhưng kẹt ở trạng thái verifying.
**Chuyện gì xảy ra:** Ba agent đều dừng ở lifecycle 'verifying' với lỗi 'The lifecycle step failed'. Log cho thấy harness_test_failed. Gốc là Paperclip đòi giao thức gateway phiên bản 4 (minProtocol=4), còn gateway AICoworker chỉ nói v3. Commit ec2d87d của Paperclip bump v3→v4 nhưng ghi là không đổi nội dung giao thức. Sửa minProtocol thành 3 ở 3 chỗ trong bản đã cài (có file .orig), restart, và trạng thái chuyển sang ready cho cả 3 agent.
**Bài học:** Khi nối hai hệ agent qua giao thức nội bộ, kiểm tra phiên bản min/max trước; một dòng lệch có thể chặn toàn bộ luồng mà log chỉ báo 'step failed'.
**Artefact:** Bảng 3 agent: trạng thái verifying → ready, kèm đoạn log 'Gateway connect probe succeeded'. Che: token gateway, đường dẫn home.
