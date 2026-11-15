---
id: 2026-11-02-tieu-chi-client-nhan-su-kien-40f9
code: M-X0KF
aliases: [M-X0KF]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1614", "claude:c4caee3c#L1615", "claude:c4caee3c#L1622", "claude:c4caee3c#L1923"]
hook: "Agent xin hạ tiêu chí 1 giây, lead bắt đổi debounce"
tension: nguoi_dung_may_sai
sides: ["Agent đề nghị nới tiêu chí vì chưa đạt", "Lead giữ tiêu chí, đổi debounce từ 5000 xuống 250 ms"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang dựng bản fork để client nhận sự kiện khi index đổi. Tiêu chí là trong 1 giây, nhưng watcher của bản gốc chờ cố định 5 giây nên không đạt, và người làm từng định nới tiêu chí. Lead không cho hạ tiêu chí mà yêu cầu đưa thời gian chờ thành biến môi trường với mặc định 5 giây; đặt 250 ms thì sự kiện đến dưới 1 giây. Bài học là khi tiêu chí trượt vì mặc định của bản gốc, thêm tuỳ chọn giữ mặc định cũ thay vì nới tiêu chí."
audience: dev dựng công cụ tích hợp AI agent với ghi chú Obsidian
spine_context: "Một nhóm đang dựng bản fork của Obsidian Hybrid Search, công cụ tìm kiếm cho ghi chú Obsidian trên máy, và điều phối nhiều agent để hoàn tất roadmap."
spine_context_lines: [profile, "claude:c4caee3c#L1526"]
spine_want: Client nhận sự kiện index trong 1 giây.
spine_want_lines: ["claude:c4caee3c#L1614"]
spine_obstacle: Watcher của bản gốc chờ cố định 5 giây sau khi file đổi rồi mới index.
spine_obstacle_lines: ["claude:c4caee3c#L1614"]
spine_turn: "Tưởng tiêu chí 1 giây không đạt được vì watcher cố định 5 giây; hoá ra thời gian chờ đặt được qua biến môi trường, mặc định vẫn 5 giây."
spine_turn_lines: ["claude:c4caee3c#L1614", "claude:c4caee3c#L1923"]
spine_action: "Đổi watcher thành đặt thời gian chờ qua OBSIDIAN_WATCH_DEBOUNCE_MS, mặc định 5000 ms, thêm test sự kiện đến dưới 1 giây khi đặt 250 ms, rồi dựng lại bản vá trên chuỗi."
spine_action_lines: ["claude:c4caee3c#L1615", "claude:c4caee3c#L1923"]
spine_outcome: Client nhận sự kiện index dưới 1 giây; 2091/2091 test xanh; kiểm tra tự động trả 1 trên bản gốc và 0 trên fork.
spine_outcome_lines: ["claude:c4caee3c#L1923", "claude:c4caee3c#L1926"]
spine_takeaway: "Khi tiêu chí trượt vì mặc định của bản gốc, thêm tuỳ chọn giữ mặc định cũ, đừng hạ tiêu chí."
spine_takeaway_lines: ["claude:c4caee3c#L1615"]
completeness: 7
---

# Tiêu chí client nhận sự kiện trong 1 giây không được hạ, phải đổi debounce

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho ghi chú Obsidian trên máy, và người làm đang dựng bản fork để client nhận sự kiện khi index đổi. Tiêu chí là trong 1 giây, nhưng watcher của bản gốc chờ cố định 5 giây nên không đạt, và người làm từng định nới tiêu chí. Lead không cho hạ tiêu chí mà yêu cầu đưa thời gian chờ thành biến môi trường với mặc định 5 giây; đặt 250 ms thì sự kiện đến dưới 1 giây. Bài học là khi tiêu chí trượt vì mặc định của bản gốc, thêm tuỳ chọn giữ mặc định cũ thay vì nới tiêu chí.
**Bối cảnh:** Watcher của upstream chờ 5 giây sau khi file đổi mới index, nên sự kiện index chậm hơn tiêu chí 1 giây.
**Chuyện gì xảy ra:** Agent báo chưa đạt và đề nghị nới tiêu chí. Lead từ chối hạ tiêu chí và giao đổi debounce thành biến môi trường, mặc định vẫn 5000 ms. Với 250 ms, test thấy sự kiện đến trong dưới 1 giây. Probe cho 1 trên upstream và 0 trên fork.
**Bài học:** Khi một tiêu chí không đạt vì mặc định của upstream, thêm tuỳ chọn có mặc định giữ hành vi cũ. Đừng nới tiêu chí.
