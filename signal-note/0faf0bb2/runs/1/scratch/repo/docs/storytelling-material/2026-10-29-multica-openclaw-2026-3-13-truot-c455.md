---
id: 2026-10-29-multica-openclaw-2026-3-13-truot-c455
code: M-0W73
aliases: [M-0W73]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3088", "claude:0faf0bb2#L3104", "claude:0faf0bb2#L3116", "claude:0faf0bb2#L3150", "claude:0faf0bb2#L3160", "claude:0faf0bb2#L3198"]
hook: "Giả báo phiên bản 2026.5.5 vẫn hỏng: lỗi nằm ở phiên bản thật"
tension: tuong_ma_hoa_ra
sides: ["Tưởng chỉ cần giả số phiên bản", "Bản cũ thiếu OPENCLAW_INCLUDE_ROOTS nên vẫn hỏng"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm muốn để Multica điều phối agent của AICoworker thay vì tự viết lớp điều phối. Họ tin chỉ cần giả số phiên bản OpenClaw là Multica sẽ chạy, vì bản đóng gói cũ chỉ bị chặn ở chỗ kiểm tra. Hoá ra bản cũ còn thiếu tính năng include cấu hình, nên lỗi vẫn còn và spike phải ghi là trượt. Ai dựng công cụ điều phối agent nên kiểm phiên bản tối thiểu của runtime trước, vì giả số phiên bản không che được khác biệt thật."
audience: dev dựng công cụ điều phối cho agent AI
spine_context: "Dự án là bộ dựng công ty một người chạy bằng đội agent AI, đang spike Multica để điều phối agent của AICoworker."
spine_context_lines: [profile, "claude:0faf0bb2#L2772"]
spine_want: Để Multica điều khiển được agent của AICoworker qua OpenClaw.
spine_want_lines: ["claude:0faf0bb2#L2772", "claude:0faf0bb2#L3150"]
spine_obstacle: "Multica v0.7.1 yêu cầu OpenClaw từ 2026.5.5, còn AICoworker đóng gói 2026.3.13."
spine_obstacle_lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3150"]
spine_turn: Tưởng chỉ cần giả số phiên bản là chạy được; hoá ra bản cũ còn thiếu OPENCLAW_INCLUDE_ROOTS nên lỗi include vẫn chặn.
spine_turn_lines: ["claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
spine_action: Viết wrapper báo phiên bản 2026.5.5 cho CLI 2026.3.13.
spine_action_lines: ["claude:0faf0bb2#L3061"]
spine_outcome: "Qua được kiểm tra phiên bản nhưng CLI báo 'Include path escapes config directory', gateway thất bại; spike ghi là trượt."
spine_outcome_lines: ["claude:0faf0bb2#L3150"]
spine_takeaway: Kiểm phiên bản tối thiểu của runtime trước khi dựng lớp điều phối lên trên; giả số phiên bản không che được khác biệt thật.
spine_takeaway_lines: ["claude:0faf0bb2#L3150"]
completeness: 7
---

# Multica + OpenClaw 2026.3.13 trượt: Multica yêu cầu từ 2026.5.5; giả phiên bản vẫn hỏng

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng đội agent AI, và người làm muốn để Multica điều phối agent của AICoworker thay vì tự viết lớp điều phối. Họ tin chỉ cần giả số phiên bản OpenClaw là Multica sẽ chạy, vì bản đóng gói cũ chỉ bị chặn ở chỗ kiểm tra. Hoá ra bản cũ còn thiếu tính năng include cấu hình, nên lỗi vẫn còn và spike phải ghi là trượt. Ai dựng công cụ điều phối agent nên kiểm phiên bản tối thiểu của runtime trước, vì giả số phiên bản không che được khác biệt thật.
**Bối cảnh:** Spike Multica v0.7.1 với agent Mai chạy qua CLI OpenClaw đóng gói trong AICoworker.
**Chuyện gì xảy ra:** Lượt đầu bị từ chối: 'openclaw 2026.3.13 is below the minimum supported version 2026.5.5'. Mình viết wrapper báo phiên bản 2026.5.5 để thử, nhưng CLI báo 'Include path escapes config directory' vì bản cũ thiếu OPENCLAW_INCLUDE_ROOTS, và gateway thất bại không có output. Kết luận: trượt vì phiên bản, không phải cấu hình. Chủ yêu cầu dọn Multica và giữ agent mai.
**Bài học:** Kiểm phiên bản tối thiểu của runtime trước khi dựng lớp điều phối trên nó.
**Artefact:** Bảng ba chỗ lỗi, không kèm token.
