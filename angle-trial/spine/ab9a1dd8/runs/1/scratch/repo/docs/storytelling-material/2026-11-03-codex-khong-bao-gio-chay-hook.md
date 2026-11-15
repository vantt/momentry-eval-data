---
id: 2026-11-03-codex-khong-bao-gio-chay-hook
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3228", "claude:ab9a1dd8#L3239"]
hook: "Codex bỏ qua mọi hook vì viết sai kiểu chữ hoa thường"
tension: nho_ma_to
sides: ["Chỉ sai snake_case thay vì PascalCase", "Codex không bao giờ chạy hook và không báo lỗi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent như Codex, và người làm muốn hook của Codex ghi lại các phiên đó. Họ tin tên sự kiện kiểu snake_case như pre_compact là đúng, nhưng Codex chỉ nhận PascalCase và bỏ qua hook mà không báo lỗi. Sửa tên xong, test cục bộ xanh, còn probe trên Windows vẫn đỏ. Ai viết hook cho host khác nên kiểm bằng log do chính hook ghi, không tin vào cấu hình đã ghi."
audience: dev viết hook hoặc plugin cho coding agent
spine_context: "Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent như Codex, và đang nối hook để ghi lại các phiên Codex."
spine_context_lines: [profile]
spine_want: Muốn hook của Codex thật sự chạy và ghi lại phiên.
spine_want_lines: ["claude:ab9a1dd8#L3184"]
spine_obstacle: Cấu hình hook dùng tên sự kiện kiểu snake_case như pre_compact.
spine_obstacle_lines: ["claude:ab9a1dd8#L3195"]
spine_turn: Tưởng snake_case là đúng; hoá ra Codex cần PascalCase và bỏ qua hook im lặng.
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3228"]
spine_action: "Đổi tên sự kiện thành PreCompact, SessionEnd, SessionStart; cập nhật test, PRD, CHANGELOG và thêm probe chạy Codex trên Windows."
spine_action_lines: ["claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3214", "claude:ab9a1dd8#L3228"]
spine_outcome: "Test cục bộ pass 234, fail 0; nhưng run CI probe trên Windows kết luận failure."
spine_outcome_lines: ["claude:ab9a1dd8#L3209", "claude:ab9a1dd8#L3239"]
spine_takeaway: "Hook sai tên bị host bỏ im lặng; kiểm bằng log do chính hook ghi trong phiên thật, đừng chỉ xem cấu hình đã ghi."
spine_takeaway_lines: ["claude:ab9a1dd8#L3214", "claude:ab9a1dd8#L3239"]
completeness: 7
---

# Codex không bao giờ chạy hook: tên sự kiện sai, bị bỏ không báo

**Góc kể:** Momentry là công cụ dòng lệnh nhặt chất liệu kể chuyện từ phiên làm việc với coding agent như Codex, và người làm muốn hook của Codex ghi lại các phiên đó. Họ tin tên sự kiện kiểu snake_case như pre_compact là đúng, nhưng Codex chỉ nhận PascalCase và bỏ qua hook mà không báo lỗi. Sửa tên xong, test cục bộ xanh, còn probe trên Windows vẫn đỏ. Ai viết hook cho host khác nên kiểm bằng log do chính hook ghi, không tin vào cấu hình đã ghi.
**Bối cảnh:** Momentry ghi cấu hình hook cho Codex, và hook được coi là đã cài.
**Chuyện gì xảy ra:** Codex yêu cầu tên sự kiện dạng PascalCase, còn momentry ghi snake_case, nên Codex bỏ qua hook mà không báo lỗi. Agent đổi thành PreCompact, SessionEnd, SessionStart, rồi thử chạy codex exec trên Windows vẫn không thấy hook gọi.
**Bài học:** Hook sai tên sự kiện thường bị host bỏ im lặng. Hãy đo bằng log do chính hook ghi, không đo bằng việc cấu hình đã được ghi.
**Artefact:** Đoạn hooks.json trước và sau khi đổi tên sự kiện.
