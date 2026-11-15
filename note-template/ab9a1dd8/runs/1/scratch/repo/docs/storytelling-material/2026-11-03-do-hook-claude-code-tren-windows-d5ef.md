---
id: 2026-11-03-do-hook-claude-code-tren-windows-d5ef
code: M-RABP
aliases: [M-RABP]
date: 2026-11-03
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3052", "claude:ab9a1dd8#L3077", "claude:ab9a1dd8#L3082", "claude:ab9a1dd8#L3091"]
hook: "Chứng minh hook chạy trên Windows bằng lỗi đăng nhập, không cần khoá API"
tension: it_ma_nhieu
sides: ["Không có khoá API, phiên không chạy được", "Chính lỗi đăng nhập chứng minh hook đã được gọi trước đó"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry đọc transcript các phiên làm việc với coding agent, và đang kiểm hook của nó trên Windows. Người làm tin phải có một phiên Claude Code đã đăng nhập mới đo được, trong khi không có máy Windows hay khoá API nào để làm việc đó. Hoá ra có điểm đo nằm trước bước đăng nhập: hook chạy lúc mở phiên, nên dòng hook.spawned trong log có thể chứng minh hook đã được gọi dù phiên báo lỗi. Dev làm hook cho công cụ bên thứ ba nên để ý trick này."
audience: "dev viết hook hoặc plugin cho coding agent, cần kiểm trên nền tảng không có máy thật"
spine_context: momentry đọc transcript các phiên làm việc với coding agent; đang đưa v0.1.0 ra và kiểm hook trên Windows.
spine_context_lines: [profile, "claude:ab9a1dd8#L3042"]
spine_want: Chứng minh hook SessionStart của momentry chạy trên Windows mà không dùng khoá API hay tài khoản của chủ.
spine_want_lines: ["claude:ab9a1dd8#L3052"]
spine_obstacle: "Không có máy Windows nào đã đăng nhập Claude Code, nên phần đo hook bị chuyển sang issue #1."
spine_obstacle_lines: ["claude:ab9a1dd8#L3042", "claude:ab9a1dd8#L3052"]
spine_turn: "Tưởng phải có một phiên đã đăng nhập mới đo được hook; hoá ra điểm đo nằm trước bước đăng nhập, vì hook chạy lúc mở phiên."
spine_turn_lines: ["claude:ab9a1dd8#L3042", "claude:ab9a1dd8#L3052"]
spine_action: "Thêm workflow chạy tay trên runner windows-2025: cài Claude Code, momentry, init, rồi mở claude -p không có khoá API."
spine_action_lines: ["claude:ab9a1dd8#L3053"]
spine_outcome: Workflow chạy xanh; docs vẫn ghi phần Claude Code hay Codex thật gọi hook trên Windows là chưa kiểm.
spine_outcome_lines: ["claude:ab9a1dd8#L3077", "claude:ab9a1dd8#L3082"]
spine_takeaway: "Khi thiếu môi trường thật, tìm điểm trong vòng đời công cụ xảy ra trước điểm cần khoá; đo được phần nào thì ghi phần đó và ghi rõ phần còn lại."
spine_takeaway_lines: ["claude:ab9a1dd8#L3052"]
completeness: 7
---

# Đo hook Claude Code trên Windows mà không dùng khoá API của ai

**Góc kể:** Dự án momentry đọc transcript các phiên làm việc với coding agent, và đang kiểm hook của nó trên Windows. Người làm tin phải có một phiên Claude Code đã đăng nhập mới đo được, trong khi không có máy Windows hay khoá API nào để làm việc đó. Hoá ra có điểm đo nằm trước bước đăng nhập: hook chạy lúc mở phiên, nên dòng hook.spawned trong log có thể chứng minh hook đã được gọi dù phiên báo lỗi. Dev làm hook cho công cụ bên thứ ba nên để ý trick này.
**Bối cảnh:** Máy làm việc không có Windows, và agent không được dùng khoá hay tài khoản của chủ.
**Chuyện gì xảy ra:** Agent viết workflow chạy tay trên runner windows-2025: cài Claude Code, cài momentry, init, rồi mở claude -p không đăng nhập. Hook SessionStart chạy lúc mở phiên, nên dòng hook.spawned trong hook.log chứng minh hook được gọi trước khi phiên báo lỗi đăng nhập. Kết quả: Claude Code gọi được hook trên Windows, Codex còn mở. Tài liệu và issue được cập nhật theo đúng phạm vi đã đo.
**Bài học:** Khi thiếu môi trường thật, tìm một điểm trong vòng đời công cụ xảy ra trước điểm cần khoá; đo được phần nào thì ghi phần đó, và ghi rõ phần còn lại.
**Artefact:** Dòng sự kiện trong hook.log, đã che mọi đường dẫn và thông tin đăng nhập.
**Góc người ngoài:** cách làm phổ biến là Chỉ tin tài liệu của host, hoặc không kiểm được gì và ghi 'chưa xác minh'; ở đây khác ở Có cách kiểm hành vi thật của công cụ bên thứ ba mà không cần thông tin đăng nhập. Người đọc sẽ muốn biết trick 'hook được gọi trước khi phiên báo lỗi đăng nhập'.
