---
id: 2026-11-03-antigravity-khong-co-su-kien-ket-d5ef
code: M-R0EZ
aliases: [M-R0EZ]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: "Đọc kỹ sự kiện của host cho thấy Stop chạy sau mỗi lượt và chặn agent, nên không dùng được để gom."
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3305", "claude:ab9a1dd8#L3410", "claude:ab9a1dd8#L3427", "claude:ab9a1dd8#L3433"]
hook: "Antigravity không có sự kiện kết thúc phiên, Stop chạy sau mỗi lượt"
tension: chon_mot_mat_mot
sides: ["Muốn gom chuyện ngay khi phiên kết thúc", "Chỉ có Stop chạy mỗi lượt và chặn agent, nên gom khi mở phiên sau"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và đang thêm Codex cùng nhiều host khác. Người làm tưởng hook của momentry đã chạy trên Codex vì đã ghi sẵn tên sự kiện. Hoá ra Codex đòi tên dạng PreCompact, SessionEnd, còn momentry ghi pre_compact, session_start, nên hook bị bỏ qua hoàn toàn mà không báo lỗi. Ai viết hook cho nhiều agent cùng lúc đều có thể dính đúng kiểu lỗi này."
audience: dev viết hook cho nhiều coding agent
spine_context: "momentry đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể; đang mở rộng sang Codex, pi, omp và Antigravity."
spine_context_lines: [profile, "claude:ab9a1dd8#L3306"]
spine_want: "Muốn gom chuyện từ các host mới, trong đó có Codex."
spine_want_lines: ["claude:ab9a1dd8#L3306"]
spine_obstacle: "Hook của momentry trên Codex bị bỏ qua mà không báo lỗi, và chạy thử vẫn không thấy hook được gọi."
spine_obstacle_lines: ["claude:ab9a1dd8#L3306"]
spine_turn: "Tưởng hook Codex đã chạy vì momentry đã ghi sẵn tên sự kiện; hoá ra Codex đòi tên dạng PreCompact, SessionEnd, còn momentry ghi pre_compact, session_start nên bị bỏ qua."
spine_turn_lines: ["claude:ab9a1dd8#L3306"]
spine_action: "Sửa tên sự kiện trong cấu hình Codex, thêm SessionEnd, rồi push."
spine_action_lines: ["claude:ab9a1dd8#L3306"]
spine_outcome: "CI vẫn xanh, nhưng chạy thử Codex vẫn chưa chứng minh được hook chạy; phần này còn mở trong issue #1."
spine_outcome_lines: ["claude:ab9a1dd8#L3306"]
spine_takeaway: "Tên sự kiện hook phải khớp đúng từng host, và hook bị bỏ qua thì không báo lỗi nên cần kiểm bằng cách chạy thật."
spine_takeaway_lines: ["claude:ab9a1dd8#L3306"]
completeness: 7
---

# Antigravity không có sự kiện kết thúc phiên: chốt gom khi mở phiên sau

**Góc kể:** momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và đang thêm Codex cùng nhiều host khác. Người làm tưởng hook của momentry đã chạy trên Codex vì đã ghi sẵn tên sự kiện. Hoá ra Codex đòi tên dạng PreCompact, SessionEnd, còn momentry ghi pre_compact, session_start, nên hook bị bỏ qua hoàn toàn mà không báo lỗi. Ai viết hook cho nhiều agent cùng lúc đều có thể dính đúng kiểu lỗi này.
**Bối cảnh:** Ba host mới là pi, omp và Antigravity. Mỗi host có cơ chế hook khác nhau.
**Chuyện gì xảy ra:** Researcher đọc tài liệu và mã: pi và omp dùng extension TypeScript với sự kiện session_shutdown. Antigravity chỉ có SessionStart và Stop, trong đó Stop chạy sau mỗi lượt và chặn agent đang chạy. Chủ chọn gom khi mở phiên sau. Các nguồn bên ngoài nói hai định dạng transcript khác nhau, nên agent kiểm trực tiếp trên máy.
**Bài học:** Khi tài liệu host liệt kê sự kiện, xem nó có chặn hay không; một sự kiện chạy sau mỗi lượt có thể làm chậm hoặc dừng agent.
**Artefact:** Bảng sự kiện hook theo từng host.
