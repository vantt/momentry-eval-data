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
hook: "Một dấu \\ trong đường dẫn, và Bash ăn mất cả lệnh hook"
tension: nho_ma_to
sides: ["Chỉ một dấu backslash trong đường dẫn", "Bash nuốt mất, hook Windows không chạy"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang hoàn tất plan đóng gói để phát hành. Tài liệu cũ ghi lệnh hook có dấu backslash chạy được từ cmd và Git Bash. Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, và Bash ăn mất backslash, nên lệnh phải đổi sang dấu /. Chưa kiểm trên máy Windows thật, nên tài liệu ghi rõ là chưa kiểm; ai viết hook trên Windows nên chọn cú pháp chạy được ở mọi shell."
audience: dev viết hook hoặc script cho Claude Code và Codex trên Windows
spine_context: Dự án momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent; người làm đang hoàn tất plan đóng gói và phân phối.
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: Hoàn tất plan đóng gói và phân phối; hai việc còn lại là push để CI chạy lần đầu và kiểm nhánh Windows trên máy thật.
spine_want_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2233"]
spine_obstacle: "Hook Windows chạy qua shell khác nhau tuỳ công cụ, và nhánh Windows chưa được kiểm trên máy thật."
spine_obstacle_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2837"]
spine_turn: "Tưởng lệnh hook có dấu backslash chạy được ở cả cmd và Git Bash; hoá ra theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, nơi Bash ăn mất backslash."
spine_turn_lines: ["claude:ab9a1dd8#L2837", "claude:ab9a1dd8#L2868"]
spine_action: "Đổi đường dẫn hook sang dấu /, gọi momentry theo tên qua thư mục shim, và ghi 'chưa kiểm' vào tài liệu cho Windows native."
spine_action_lines: ["claude:ab9a1dd8#L2845", "claude:ab9a1dd8#L2855", "claude:ab9a1dd8#L2868"]
spine_outcome: "Bộ test chạy 233 pass, 0 fail; kết quả CI chưa thấy trong trích đoạn."
spine_outcome_lines: ["claude:ab9a1dd8#L2858", "claude:ab9a1dd8#L2881"]
spine_takeaway: "Khi không kiểm được trên nền tảng, ghi 'chưa kiểm' thay vì khẳng định; chọn cú pháp chạy được ở mọi shell có khả năng."
spine_takeaway_lines: ["claude:ab9a1dd8#L2855"]
completeness: 7
---

# Claude Code và Codex chạy hook Windows qua shell khác nhau: dùng dấu / và gọi bằng tên lệnh

**Góc kể:** Dự án momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang hoàn tất plan đóng gói để phát hành. Tài liệu cũ ghi lệnh hook có dấu backslash chạy được từ cmd và Git Bash. Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, và Bash ăn mất backslash, nên lệnh phải đổi sang dấu /. Chưa kiểm trên máy Windows thật, nên tài liệu ghi rõ là chưa kiểm; ai viết hook trên Windows nên chọn cú pháp chạy được ở mọi shell.
**Bối cảnh:** Trước khi viết hướng dẫn hook trên Windows, agent tìm web về shell mà hai công cụ dùng để chạy hook.
**Chuyện gì xảy ra:** Theo báo cáo cộng đồng, Claude Code chạy hook qua Git Bash, còn Codex qua cmd. Đường dẫn có dấu backslash sẽ bị Bash ăn mất. Lệnh hook đổi sang dấu / trong đường dẫn tới momentry.cmd, và /bip gọi momentry theo tên vì installer đã thêm thư mục shim vào PATH. Tài liệu ghi rõ đây là điều chưa kiểm trên phiên thật.
**Bài học:** Khi không kiểm được trên nền tảng, ghi 'chưa kiểm' vào tài liệu thay vì khẳng định. Chọn cú pháp chạy được ở mọi shell có khả năng.
**Artefact:** Dòng hook trong docs/installation.md trước và sau. Che đường dẫn HOME.
