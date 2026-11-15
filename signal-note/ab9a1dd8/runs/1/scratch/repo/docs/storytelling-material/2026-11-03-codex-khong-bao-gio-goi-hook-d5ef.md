---
id: 2026-11-03-codex-khong-bao-gio-goi-hook-d5ef
code: M-5ZFF
aliases: [M-5ZFF]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3206", "claude:ab9a1dd8#L3213", "claude:ab9a1dd8#L3233", "claude:ab9a1dd8#L3239"]
hook: "Hook Codex ghi sai tên sự kiện từ đầu, bị bỏ qua mà không báo"
tension: nho_ma_to
sides: ["Một tên sự kiện ghi sai", "Hook Codex không bao giờ chạy trên mọi nền tảng, không cảnh báo"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript của phiên coding agent, đang chuẩn bị phát hành và kiểm hook trên Windows. Code ghi tên sự kiện Codex là pre_compact và session_start, nhưng Codex thực ra đọc PreCompact, SessionEnd, SessionStart, nên hook có thể không bao giờ chạy mà không báo lỗi. Người làm đọc thẳng mã nguồn Codex để sửa thay vì đoán từ tài liệu, và probe CI vẫn chưa xanh sau khi sửa."
audience: dev viết hook hoặc plugin cho nhiều coding agent
spine_context: momentry đọc transcript của phiên làm việc với coding agent để nhặt chuyện đáng kể; đang chuẩn bị phát hành và kiểm hook chạy thật trên Windows.
spine_context_lines: [profile, "claude:ab9a1dd8#L3047"]
spine_want: "Hook của momentry phải chạy thật trong phiên Codex trên Windows, không chỉ được ghi vào file."
spine_want_lines: ["claude:ab9a1dd8#L3047"]
spine_obstacle: Codex chỉ chạy hook khi bật hooks = true và có trusted_hash sha256 cho từng hook.
spine_obstacle_lines: ["claude:ab9a1dd8#L3106"]
spine_turn: "Code ghi tên sự kiện Codex là pre_compact và session_start; Codex thực ra đọc PreCompact, SessionEnd, SessionStart. Lỗi có từ đầu và hook bị bỏ qua mà không báo."
spine_turn_lines: ["claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3228"]
spine_action: "Đọc mã nguồn Codex qua gh api, sửa tên sự kiện cùng test, PRD, CHANGELOG; đổi probe CI sang cờ bỏ duyệt tin cậy."
spine_action_lines: ["claude:ab9a1dd8#L3184", "claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3213"]
spine_outcome: 234 test nội bộ qua; lần chạy probe CI sau đó vẫn đỏ ở bước mở phiên Codex.
spine_outcome_lines: ["claude:ab9a1dd8#L3209", "claude:ab9a1dd8#L3239"]
spine_takeaway: "Kiểm tên sự kiện theo tài liệu hoặc mã nguồn của host, không chỉ kiểm file đã ghi; hook của bên thứ ba cần đọc mã nguồn để biết cách duyệt tin cậy."
spine_takeaway_lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3195"]
completeness: 7
---

# Codex không bao giờ gọi hook của momentry: ghi sai tên sự kiện, và không báo lỗi

**Góc kể:** momentry là công cụ đọc transcript của phiên coding agent, đang chuẩn bị phát hành và kiểm hook trên Windows. Code ghi tên sự kiện Codex là pre_compact và session_start, nhưng Codex thực ra đọc PreCompact, SessionEnd, SessionStart, nên hook có thể không bao giờ chạy mà không báo lỗi. Người làm đọc thẳng mã nguồn Codex để sửa thay vì đoán từ tài liệu, và probe CI vẫn chưa xanh sau khi sửa.
**Bối cảnh:** Codex đọc hooks.json với tên sự kiện dạng PascalCase, còn momentry ghi pre_compact và session_start.
**Chuyện gì xảy ra:** Tìm trong code cho thấy tên sai từ đầu, nên hook Codex bị bỏ qua trên mọi nền tảng mà không có cảnh báo. Sửa thành PreCompact, SessionEnd, SessionStart. Probe Codex vẫn không gọi hook vì Codex yêu cầu duyệt trust; agent đọc mã nguồn để hiểu trusted_hash rồi dùng cờ bypass chỉ cho probe.
**Bài học:** Hook của host chạy im lặng khi sai tên sự kiện. Test nên kiểm tên sự kiện theo tài liệu hoặc mã của host, không chỉ kiểm file được ghi.
**Artefact:** Đoạn hooks.json đúng và sai, so tên sự kiện.
**Góc người ngoài:** cách làm phổ biến là Dev thường giả định cấu hình hook đúng vì không thấy lỗi, hoặc chỉ đọc tài liệu mà không kiểm chứng với mã nguồn thật; ở đây khác ở Agent đọc trực tiếp mã nguồn của công cụ bên thứ ba qua gh api để xác nhận cách đặt tên và cờ trust, thay vì đoán từ tài liệu. Người đọc sẽ hỏi làm sao biết cần xem mã nguồn và cách tra nhanh.
