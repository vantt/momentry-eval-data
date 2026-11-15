---
id: 2026-11-03-hook-cua-codex-khong-bao-gio-d5ef
code: M-T4JX
aliases: [M-T4JX]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228", "claude:ab9a1dd8#L3233"]
hook: "Hook Codex không chạy lần nào vì viết sai kiểu chữ tên sự kiện"
tension: nho_ma_to
sides: ["Test xanh, hook tưởng đã cài xong", "Tên sự kiện sai kiểu chữ nên Codex lặng lẽ bỏ qua từ đầu"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang muốn hook của Codex chạy thật trước khi phát hành. Test vẫn xanh (234/234), nhưng hook Codex chưa chạy lần nào: tên sự kiện viết snake_case trong khi Codex dùng PascalCase, nên nó bỏ qua lặng lẽ. Ai viết test chỉ kiểm chuỗi cấu hình có thể mắc đúng lỗi này."
audience: dev viết hook hoặc test cho công cụ dùng nhiều coding agent
spine_context: "momentry là công cụ đọc transcript phiên làm việc với coding agent (Claude Code, Codex) để nhặt chuyện đáng kể; người làm đang hoàn tất kế hoạch đóng gói và phát hành."
spine_context_lines: [profile, "claude:ab9a1dd8#L2233"]
spine_want: Muốn hook của Codex chạy thật trong phiên Codex trước khi coi kế hoạch là hoàn tất tốt đẹp.
spine_want_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L3047"]
spine_obstacle: Codex bỏ qua hook có tên sự kiện sai mà không báo lỗi nào.
spine_obstacle_lines: ["claude:ab9a1dd8#L3195"]
spine_turn: "Tưởng test xanh nghĩa là hook đã chạy; hoá ra tên sự kiện snake_case khiến Codex lặng lẽ bỏ qua, còn test chỉ kiểm chuỗi trong file."
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3209"]
spine_action: "Đổi tên sự kiện sang PascalCase (PreCompact, SessionEnd, SessionStart), sửa test, PRD và CHANGELOG, rồi commit."
spine_action_lines: ["claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228"]
spine_outcome: Test cục bộ qua 234/234; probe Windows trên CI đỏ nên hook Codex trên Windows vẫn chưa được xác nhận chạy thật.
spine_outcome_lines: ["claude:ab9a1dd8#L3047", "claude:ab9a1dd8#L3209", "claude:ab9a1dd8#L3239"]
spine_takeaway: "Hook sai tên không báo lỗi; test kiểm chuỗi cấu hình chưa đủ, cần một lần chạy thật."
spine_takeaway_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3239"]
completeness: 7
---

# Hook của Codex không bao giờ chạy: tên sự kiện viết sai kiểu chữ

**Góc kể:** momentry là công cụ đọc transcript phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang muốn hook của Codex chạy thật trước khi phát hành. Test vẫn xanh (234/234), nhưng hook Codex chưa chạy lần nào: tên sự kiện viết snake_case trong khi Codex dùng PascalCase, nên nó bỏ qua lặng lẽ. Ai viết test chỉ kiểm chuỗi cấu hình có thể mắc đúng lỗi này.
**Bối cảnh:** Codex đọc hooks.json với tên sự kiện PascalCase, còn momentry ghi snake_case.
**Chuyện gì xảy ra:** Agent tra mã nguồn Codex: tên đúng là PreCompact, SessionEnd và SessionStart. momentry ghi pre_compact và session_start nên Codex bỏ qua mà không báo lỗi, từ đầu dự án. Đã sửa và thêm SessionEnd. Test cũ vẫn xanh vì chỉ kiểm chuỗi trong file, không kiểm sự kiện có chạy hay không.
**Bài học:** Hook sai tên không báo lỗi. Test kiểm chuỗi cấu hình là chưa đủ; cần một lần chạy thật.
**Artefact:** Đoạn hooks.json trước và sau khi sửa.
