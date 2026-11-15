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
hook: "Codex chưa từng chạy hook momentry vì viết sai chữ hoa"
tension: nho_ma_to
sides: ["Tên sự kiện pre_compact thay vì PreCompact", "Codex bỏ qua im lặng, hook chưa từng chạy trên mọi nền tảng"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, chạy trên máy người dùng và đang chuẩn bị phát hành. Người làm tin tên sự kiện viết kiểu snake_case như pre_compact là đúng, và test cũng xác nhận điều đó. Hoá ra Codex chỉ nhận PascalCase như PreCompact, nên hook bị bỏ qua im lặng mà không báo lỗi. Ai viết hook cho coding agent nên biết: test xanh không chứng minh hook được gọi."
audience: "dev viết hook hoặc plugin cho Claude Code, Codex"
spine_context: "momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, chạy trên máy người dùng, và đang chuẩn bị đóng gói phân phối."
spine_context_lines: [profile, "claude:ab9a1dd8#L2233"]
spine_want: "Muốn biết hook thật sự chạy trong Codex và Claude Code trên Windows, chứ không chỉ pass unit test."
spine_want_lines: ["claude:ab9a1dd8#L3047"]
spine_obstacle: "Hook của Codex không được gọi, nên phải đọc mã nguồn Codex để tìm lý do."
spine_obstacle_lines: ["claude:ab9a1dd8#L3184"]
spine_turn: "Tưởng tên sự kiện viết snake_case như pre_compact là đúng; hoá ra Codex chỉ nhận PascalCase như PreCompact, SessionEnd, SessionStart."
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3228"]
spine_action: "Đổi ba tên sự kiện sang PascalCase, thêm SessionEnd, rồi cập nhật test, PRD và CHANGELOG."
spine_action_lines: ["claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228"]
spine_outcome: "Test còn 234 pass, 0 fail. README vẫn nhắc pre_compact và đang do phiên khác sửa."
spine_outcome_lines: ["claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3209"]
spine_takeaway: Unit test bám theo chuỗi do chính code sinh ra nên không bắt được tên sai; cần chạy host thật để đếm số lần hook được gọi.
spine_takeaway_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3209"]
completeness: 7
---

# Codex chưa từng chạy hook của momentry vì tên sự kiện sai: pre_compact thay vì PreCompact

**Góc kể:** momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, chạy trên máy người dùng và đang chuẩn bị phát hành. Người làm tin tên sự kiện viết kiểu snake_case như pre_compact là đúng, và test cũng xác nhận điều đó. Hoá ra Codex chỉ nhận PascalCase như PreCompact, nên hook bị bỏ qua im lặng mà không báo lỗi. Ai viết hook cho coding agent nên biết: test xanh không chứng minh hook được gọi.
**Bối cảnh:** Probe Codex trên Windows không thấy hook được gọi. Agent đọc mã nguồn Codex để tìm lý do.
**Chuyện gì xảy ra:** hooks.json của Codex đòi tên sự kiện dạng PascalCase: PreCompact, SessionEnd, SessionStart. momentry ghi pre_compact và session_start nên Codex bỏ qua mà không báo lỗi, trên mọi nền tảng. Đã sửa tên và thêm SessionEnd. Test còn 234 pass.
**Bài học:** Hook bị bỏ qua im lặng không lộ ra trong unit test. Cần probe chạy host thật để đếm số lần hook được gọi.
**Artefact:** Đoạn hooks.json trước và sau khi sửa 3 tên sự kiện. Commit 8294bc7.
