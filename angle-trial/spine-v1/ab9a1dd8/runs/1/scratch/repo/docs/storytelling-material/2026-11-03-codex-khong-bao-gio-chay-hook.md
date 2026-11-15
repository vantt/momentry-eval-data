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
angle: "Momentry là công cụ dòng lệnh đọc transcript phiên làm việc với coding agent, và đội đang cài hook để Codex tự ghi lại phiên. Đội tin tên sự kiện snake_case là đúng cho Codex, nhưng commit sửa lại cho thấy Codex cần PascalCase như PreCompact, SessionEnd, SessionStart. Ai cài hook cho agent nên kiểm tên sự kiện theo tài liệu của host, vì test chỉ khớp chuỗi trong code sẽ không bắt được lỗi này, và probe Windows vẫn đỏ nên chưa thể coi là xong."
audience: dev cài hook cho coding agent
spine_context: "Momentry là công cụ dòng lệnh đọc transcript phiên làm việc với coding agent để nhặt chất liệu kể chuyện, đang cài hook cho Codex."
spine_context_lines: [profile]
spine_want: Muốn hook của Codex trên Windows chạy thật và được xác nhận.
spine_want_lines: ["claude:ab9a1dd8#L3214"]
spine_obstacle: Code và test đều đang dùng tên sự kiện snake_case cho Codex.
spine_obstacle_lines: ["claude:ab9a1dd8#L3195"]
spine_turn: "Tưởng snake_case đúng cho Codex; hoá ra Codex cần PascalCase: PreCompact, SessionEnd, SessionStart."
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3228"]
spine_action: "Đổi tên sự kiện sang PascalCase trong code, test, PRD, CHANGELOG và commit."
spine_action_lines: ["claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3228"]
spine_outcome: "Probe Windows trên CI vẫn thất bại, nên hook chưa được xác nhận chạy."
spine_outcome_lines: ["claude:ab9a1dd8#L3239"]
spine_takeaway: "Kiểm tên sự kiện theo nguồn của host và xác nhận bằng log hook chạy thật, không chỉ bằng test cấu hình."
spine_takeaway_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3239"]
completeness: 7
---

# Codex không bao giờ chạy hook: tên sự kiện sai, bị bỏ không báo

**Góc kể:** Momentry là công cụ dòng lệnh đọc transcript phiên làm việc với coding agent, và đội đang cài hook để Codex tự ghi lại phiên. Đội tin tên sự kiện snake_case là đúng cho Codex, nhưng commit sửa lại cho thấy Codex cần PascalCase như PreCompact, SessionEnd, SessionStart. Ai cài hook cho agent nên kiểm tên sự kiện theo tài liệu của host, vì test chỉ khớp chuỗi trong code sẽ không bắt được lỗi này, và probe Windows vẫn đỏ nên chưa thể coi là xong.
**Bối cảnh:** Momentry ghi cấu hình hook cho Codex, và hook được coi là đã cài.
**Chuyện gì xảy ra:** Codex yêu cầu tên sự kiện dạng PascalCase, còn momentry ghi snake_case, nên Codex bỏ qua hook mà không báo lỗi. Agent đổi thành PreCompact, SessionEnd, SessionStart, rồi thử chạy codex exec trên Windows vẫn không thấy hook gọi.
**Bài học:** Hook sai tên sự kiện thường bị host bỏ im lặng. Hãy đo bằng log do chính hook ghi, không đo bằng việc cấu hình đã được ghi.
**Artefact:** Đoạn hooks.json trước và sau khi đổi tên sự kiện.
