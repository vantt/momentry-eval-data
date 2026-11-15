---
id: 2026-11-02-o-tmp-co-han-muc-lam-40f9
code: M-7PBP
aliases: [M-7PBP]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506", "claude:c4caee3c#L508", "claude:c4caee3c#L621", "claude:c4caee3c#L740", "claude:c4caee3c#L3966", "claude:c4caee3c#L3973"]
hook: "Ổ /tmp đầy hạn mức làm mọi agent hỏng cùng lúc"
tension: nho_ma_to
sides: ["Chỉ là thư mục tạm cho scratchpad", "Mọi lệnh shell của mọi agent đều hỏng"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án npm tìm trong kho ghi chú Obsidian cục bộ, và người làm đang chạy 11 agent song song để hoàn tất một roadmap. Họ đặt worktree và thư viện phụ thuộc, mỗi cái khoảng 1,3G, trong /tmp và tưởng đó chỉ là chỗ chứa tạm. Hoá ra /tmp là tmpfs 16G có hạn mức: khi đầy, mọi lệnh shell của mọi agent đều hỏng. Ai chạy nhiều agent song song trên máy cá nhân nên xem lại chỗ đặt worktree của mình."
audience: dev chạy nhiều agent AI song song trên máy cá nhân
spine_context: "Một dự án npm tìm trong kho ghi chú Obsidian cục bộ, và người làm đang điều phối 11 agent chạy song song để hoàn tất một roadmap."
spine_context_lines: [profile, "claude:c4caee3c#L740"]
spine_want: Muốn các agent chạy song song và tiếp tục đúng từ chỗ đã dừng.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Hạn mức đĩa trên /tmp đầy, và mọi lệnh shell của mọi agent đều hỏng."
spine_obstacle_lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508"]
spine_turn: "Tưởng /tmp chỉ là chỗ chứa tạm; hoá ra worktree và thư viện phụ thuộc (mỗi cái khoảng 1,3G) nằm trên tmpfs 16G có hạn mức, nên đầy đĩa kéo sập cả 11 agent."
spine_turn_lines: ["claude:c4caee3c#L506", "claude:c4caee3c#L740"]
spine_action: "Dừng agent, chuyển các worktree sang ổ thật, sửa đường dẫn git, rồi chạy lại từng agent; sau đó chỉ xoá những thứ của agent đã xong."
spine_action_lines: ["claude:c4caee3c#L740", "claude:c4caee3c#L3972"]
spine_outcome: "/tmp còn 26%; thư mục làm việc giảm từ 21G xuống 6,4G, và không mất phần việc dở dang."
spine_outcome_lines: ["claude:c4caee3c#L740", "claude:c4caee3c#L3974"]
spine_takeaway: "Đặt worktree và bản dựng lớn trên ổ có dung lượng thật, không đặt trên tmpfs có hạn mức; ghi quy tắc này vào brief của mọi agent ngay từ đầu."
spine_takeaway_lines: ["claude:c4caee3c#L740"]
completeness: 7
---

# Ổ /tmp có hạn mức làm mọi agent hỏng, phải chuyển worktree sang ổ thật

**Góc kể:** Một dự án npm tìm trong kho ghi chú Obsidian cục bộ, và người làm đang chạy 11 agent song song để hoàn tất một roadmap. Họ đặt worktree và thư viện phụ thuộc, mỗi cái khoảng 1,3G, trong /tmp và tưởng đó chỉ là chỗ chứa tạm. Hoá ra /tmp là tmpfs 16G có hạn mức: khi đầy, mọi lệnh shell của mọi agent đều hỏng. Ai chạy nhiều agent song song trên máy cá nhân nên xem lại chỗ đặt worktree của mình.
**Bối cảnh:** Điều phối 11 agent song song, mỗi worktree đặt trong /tmp (tmpfs 16G có hạn mức) và mỗi worktree tốn khoảng 1,3G cho thư viện phụ thuộc.
**Chuyện gì xảy ra:** Khi ghi scratchpad, lệnh báo EDQUOT và mọi lệnh shell của mọi agent đều hỏng. Lead dừng toàn bộ agent, chuyển nguyên các worktree sang một thư mục trên ổ chính, sửa lại đường dẫn cho git, rồi chạy lại từng agent từ chỗ đã dừng mà không mất phần việc dở. /tmp sau đó còn 26%. Về sau, dọn dẹp theo từng việc đã xong đưa thư mục làm việc từ 21G xuống 6,4G.
**Bài học:** Đặt worktree và bản dựng lớn trên ổ có dung lượng thật, không đặt trên tmpfs có hạn mức; và đưa quy tắc này vào brief của mọi agent ngay từ đầu.
**Artefact:** Trạng thái điều phối lead-state và thông báo lỗi EDQUOT (không kèm đường dẫn cá nhân).
**Góc người ngoài:** cách làm phổ biến là Dev thường để rác tích lũy đến khi đầy đĩa mới dọn một lần, hoặc xoá hết một lúc và làm hỏng việc đang chạy; ở đây khác ở Người đọc sẽ hỏi cách biết cái nào còn dùng được: lead liệt kê theo từng agent và chỉ xoá phần đã xác nhận xong.
