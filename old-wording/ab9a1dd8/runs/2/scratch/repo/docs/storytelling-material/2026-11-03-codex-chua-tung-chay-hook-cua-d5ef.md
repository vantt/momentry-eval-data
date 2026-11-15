---
id: 2026-11-03-codex-chua-tung-chay-hook-cua-d5ef
code: M-B0ZJ
aliases: [M-B0ZJ]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3228"]
hook: "Codex chưa từng chạy hook vì pre_compact thay vì PreCompact"
tension: nho_ma_to
sides: ["Chỉ sai kiểu viết tên sự kiện", "Codex bỏ qua im lặng trên mọi nền tảng"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và nó đăng ký hook vào các agent như Codex. Người làm tưởng hook Codex đã chạy vì unit test vẫn xanh, nhưng test chỉ kiểm chính tên sai đó. Hoá ra Codex chỉ nhận tên dạng PascalCase như PreCompact, còn momentry ghi pre_compact nên Codex bỏ qua im lặng. Ai viết hook cho agent nên đếm số lần hook thật sự được gọi, không chỉ tin test xanh."
audience: dev viết hook hoặc plugin cho coding agent
spine_context: "momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, chạy trên máy người dùng và đọc transcript của Codex cùng Claude Code."
spine_context_lines: [profile]
spine_want: Muốn hook của momentry thật sự chạy trong Codex và đếm được số lần gọi.
spine_want_lines: ["claude:ab9a1dd8#L3214"]
spine_obstacle: Probe Codex trên Windows không thấy hook được gọi.
spine_obstacle_lines: ["claude:ab9a1dd8#L3214"]
spine_turn: Tưởng tên sự kiện dạng snake_case là đúng cho Codex; hoá ra Codex chỉ nhận PascalCase như PreCompact.
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3228"]
spine_action: "Đổi pre_compact và session_start sang PreCompact và SessionStart, thêm SessionEnd, rồi sửa test, PRD và CHANGELOG."
spine_action_lines: ["claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228"]
spine_outcome: "Test còn 234 pass, 0 fail."
spine_outcome_lines: ["claude:ab9a1dd8#L3209", "claude:ab9a1dd8#L3228"]
spine_takeaway: Hook bị bỏ qua im lặng không lộ ra trong unit test; cần probe chạy host thật để đếm số lần hook được gọi.
spine_takeaway_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3209"]
completeness: 7
---

# Codex chưa từng chạy hook của momentry vì tên sự kiện sai: pre_compact thay vì PreCompact

**Góc kể:** momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và nó đăng ký hook vào các agent như Codex. Người làm tưởng hook Codex đã chạy vì unit test vẫn xanh, nhưng test chỉ kiểm chính tên sai đó. Hoá ra Codex chỉ nhận tên dạng PascalCase như PreCompact, còn momentry ghi pre_compact nên Codex bỏ qua im lặng. Ai viết hook cho agent nên đếm số lần hook thật sự được gọi, không chỉ tin test xanh.
**Bối cảnh:** Probe Codex trên Windows không thấy hook được gọi. Agent đọc mã nguồn Codex để tìm lý do.
**Chuyện gì xảy ra:** hooks.json của Codex đòi tên sự kiện dạng PascalCase: PreCompact, SessionEnd, SessionStart. momentry ghi pre_compact và session_start nên Codex bỏ qua mà không báo lỗi, trên mọi nền tảng. Đã sửa tên và thêm SessionEnd. Test còn 234 pass.
**Bài học:** Hook bị bỏ qua im lặng không lộ ra trong unit test. Cần probe chạy host thật để đếm số lần hook được gọi.
**Artefact:** Đoạn hooks.json trước và sau khi sửa 3 tên sự kiện. Commit 8294bc7.
