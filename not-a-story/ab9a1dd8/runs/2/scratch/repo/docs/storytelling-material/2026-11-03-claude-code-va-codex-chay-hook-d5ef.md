---
id: 2026-11-03-claude-code-va-codex-chay-hook-d5ef
code: M-C7BT
aliases: [M-C7BT]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L2830", "claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
hook: "Một dấu backslash trong đường dẫn hook Windows bị Bash ăn mất"
tension: nho_ma_to
sides: ["Một ký tự backslash bé xíu trong đường dẫn", "Hook chạy qua Bash bị hỏng, và chưa kiểm trên phiên thật"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang viết hướng dẫn cài hook trên Windows. Họ tưởng lệnh hook có đường dẫn backslash chạy được từ cmd và Git Bash là đủ, nhưng Claude Code và Codex chạy hook bằng shell nào vẫn chưa kiểm. Báo cáo cộng đồng cho thấy Bash có thể ăn mất dấu backslash, nên họ đổi sang dấu / và ghi rõ phần chưa kiểm trong tài liệu. Ai viết hook trên Windows nên biết shell của từng công cụ có thể khác nhau."
audience: dev viết hook hoặc cài công cụ dòng lệnh trên Windows
spine_context: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang viết hướng dẫn cài hook trên Windows."
spine_context_lines: [profile, "claude:ab9a1dd8#L2868"]
spine_want: Hook trên Windows phải chạy được trong cả Claude Code và Codex.
spine_want_lines: ["claude:ab9a1dd8#L2868"]
spine_obstacle: Chưa biết Claude Code và Codex chạy hook trên Windows bằng shell nào.
spine_obstacle_lines: ["claude:ab9a1dd8#L2832", "claude:ab9a1dd8#L2837"]
spine_turn: Tưởng lệnh hook có đường dẫn backslash chạy được từ cmd và Git Bash là đủ; báo cáo cộng đồng cho thấy shell của hai công cụ chưa được kiểm và Bash có thể ăn mất dấu backslash.
spine_turn_lines: ["claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2868"]
spine_action: Đổi đường dẫn hook sang dấu / và gọi momentry theo tên qua PATH; ghi rõ phần chưa kiểm vào docs/installation.md.
spine_action_lines: ["claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
spine_outcome: "Test pass 233, fail 0; plan 43/45 việc, còn push và kiểm Windows thật chưa làm."
spine_outcome_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2858"]
spine_takeaway: "Khi chưa kiểm được trên nền tảng, ghi 'chưa kiểm' vào tài liệu thay vì khẳng định; chọn cú pháp chạy được ở mọi shell có khả năng."
spine_takeaway_lines: ["claude:ab9a1dd8#L2868"]
completeness: 7
---

# Claude Code và Codex chạy hook Windows qua shell khác nhau: dùng dấu / và gọi bằng tên lệnh

**Góc kể:** Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang viết hướng dẫn cài hook trên Windows. Họ tưởng lệnh hook có đường dẫn backslash chạy được từ cmd và Git Bash là đủ, nhưng Claude Code và Codex chạy hook bằng shell nào vẫn chưa kiểm. Báo cáo cộng đồng cho thấy Bash có thể ăn mất dấu backslash, nên họ đổi sang dấu / và ghi rõ phần chưa kiểm trong tài liệu. Ai viết hook trên Windows nên biết shell của từng công cụ có thể khác nhau.
**Bối cảnh:** Trước khi viết hướng dẫn hook trên Windows, agent tìm web về shell mà hai công cụ dùng để chạy hook.
**Chuyện gì xảy ra:** Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, còn Codex qua cmd. Đường dẫn có dấu backslash sẽ bị Bash ăn mất. Lệnh hook đổi sang dấu / trong đường dẫn tới momentry.cmd, và /bip gọi momentry theo tên vì installer đã thêm thư mục shim vào PATH. Tài liệu ghi rõ đây là điều chưa kiểm trên phiên thật.
**Bài học:** Khi không kiểm được trên nền tảng, ghi 'chưa kiểm' vào tài liệu thay vì khẳng định. Chọn cú pháp chạy được ở mọi shell có khả năng.
**Artefact:** Dòng hook trong docs/installation.md trước và sau. Che đường dẫn HOME.
