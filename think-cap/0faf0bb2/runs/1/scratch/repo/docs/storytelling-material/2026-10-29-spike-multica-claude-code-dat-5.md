---
id: 2026-10-29-spike-multica-claude-code-dat-5
date: 2026-10-29
repo: repo
status: raw
signals: [người duyệt thứ máy soạn, artefact nhìn được, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3539", "claude:0faf0bb2#L3540", "claude:0faf0bb2#L3553", "claude:0faf0bb2#L3556", "claude:0faf0bb2#L3629", "claude:0faf0bb2#L3643", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3707", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3747"]
hook: "Agent marketing không bịa giá, dừng lại hỏi chủ: spike đạt 5/5"
tension: tuong_ma_hoa_ra
sides: ["Agent AI hay tự bịa số khi thiếu dữ liệu", "Nó dừng lại và hỏi chủ về giá và hạn chót"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Spike Multica + Claude Code đạt 5/5: agent hỏi chủ thay vì bịa số

**Bối cảnh:** Spike B' với Claude Code làm runtime, 3 agent (marketing, sales, chủ) chạy workflow cột 'Nháp → Sales review → In review → Done'.
**Chuyện gì xảy ra:** Issue không chỉ định người được tự giao theo cột đầu, và agent ghi comment, chuyển cột trong khoảng 16 giây. Sales agent trả lại bài 2 lần vì thiếu giá. Marketing agent không bịa giá và hạn chót, dừng lại hỏi chủ; sau khi chủ comment, bài được hoàn thiện, sales duyệt, issue sang in_review giao cho chủ. Chat hai phiên với cùng agent giữ đúng hai mã khách riêng, không lẫn.
**Bài học:** Vòng trả lại, sửa, hỏi người chạy được khi chỉ dẫn yêu cầu hỏi khi thiếu dữ liệu; còn việc chặn done phải nằm ở server, không chỉ trong chỉ dẫn.
**Artefact:** Chuỗi status của issue theo thời gian (todo → sales_review → todo → in_review) dưới dạng sơ đồ cột.
