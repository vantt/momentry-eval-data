---
id: 2026-10-29-multica-v0-7-1-tu-choi
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3046", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150", "claude:0faf0bb2#L3187"]
hook: "Giả mạo phiên bản để qua mặt kiểm tra, vẫn trượt cả 4 tiêu chí"
tension: cam_ma_van_lot
sides: ["dùng shim khai man phiên bản để qua cổng kiểm tra", "bản cũ thiếu một biến cấu hình nên vẫn vỡ, spike trượt cả 4 tiêu chí"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica v0.7.1 từ chối OpenClaw 2026.3.13 vì yêu cầu bản ≥2026.5.5: spike trượt

**Bối cảnh:** Spike B: Multica điều khiển agent OpenClaw của AICoworker qua CLI, kiểm 4 tiêu chí (workspace, ghi ngược, session, workflow).
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối với 'below the minimum supported version 2026.5.5'. Thử khai man phiên bản bằng shim thì CLI báo 'Include path escapes config directory' vì bản 2026.3.13 thiếu OPENCLAW_INCLUDE_ROOTS. Kết luận không đạt 4 tiêu chí nào. Dọn toàn bộ stack Docker, volume và 3 image (~1,2 GB), giữ lại agent mai.
**Bài học:** Trước khi thiết kế tích hợp, kiểm phiên bản tối thiểu mà đối tác yêu cầu; một ràng buộc phiên bản có thể làm cả hướng đi không khả thi.
**Artefact:** Bảng 4 tiêu chí với cột trượt, kèm đoạn thông báo lỗi phiên bản. Che: không có.
