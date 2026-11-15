---
id: 2026-11-02-worktree-trong-tmp-lam-day-han
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508", "claude:c4caee3c#L621", "claude:c4caee3c#L632", "claude:c4caee3c#L740"]
hook: "/tmp đầy hạn mức, 11 agent cùng hỏng shell mà không mất việc"
tension: nho_ma_to
sides: ["Một thư mục tạm đầy hạn mức", "Mọi lệnh shell của 11 agent cùng hỏng"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang điều phối 11 agent song song để hoàn tất roadmap cho bản fork của Obsidian Hybrid Search, một gói npm tìm ghi chú Obsidian theo nghĩa. Họ tưởng /tmp vẫn còn chỗ cho worktree và scratchpad, rồi mọi lệnh shell của mọi agent đều hỏng vì hạn mức đĩa đã đầy; mỗi worktree tự kéo node_modules riêng. Họ chuyển worktree sang ổ thật mà không mất việc dở, và /tmp còn 26%. Ai chạy nhiều agent song song trên git worktree nên đặt worktree lên ổ thật, không để trên tmpfs có hạn mức."
audience: dev chạy nhiều agent song song trên git worktree
spine_context: "Một dự án gói npm tìm kiếm ghi chú Obsidian theo nghĩa, đang chạy 11 agent song song để hoàn tất roadmap bản fork."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn hoàn tất roadmap bằng nhiều agent chạy song song.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: Ghi scratchpad lỗi EDQUOT vì hạn mức đĩa /tmp đã đầy; mọi lệnh shell hỏng.
spine_obstacle_lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508"]
spine_turn: Tưởng /tmp còn chỗ cho worktree và scratchpad; hoá ra hạn mức đã đầy vì mỗi worktree có node_modules riêng.
spine_turn_lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L506"]
spine_action: Chuyển worktree sang /home/vantt/projects/ohs-wt và sửa brief chung để agent tạo worktree ở đó.
spine_action_lines: ["claude:c4caee3c#L621", "claude:c4caee3c#L638"]
spine_outcome: /tmp giảm còn 26%; các agent được gửi tin nhắn để resume từ chỗ dừng.
spine_outcome_lines: ["claude:c4caee3c#L740"]
spine_takeaway: "Đặt worktree và node_modules trên ổ đĩa thật, không trên tmpfs có hạn mức."
spine_takeaway_lines: ["claude:c4caee3c#L506", "claude:c4caee3c#L638"]
completeness: 7
---

# Worktree trong /tmp làm đầy hạn mức, 11 agent cùng hỏng shell

**Góc kể:** Người làm đang điều phối 11 agent song song để hoàn tất roadmap cho bản fork của Obsidian Hybrid Search, một gói npm tìm ghi chú Obsidian theo nghĩa. Họ tưởng /tmp vẫn còn chỗ cho worktree và scratchpad, rồi mọi lệnh shell của mọi agent đều hỏng vì hạn mức đĩa đã đầy; mỗi worktree tự kéo node_modules riêng. Họ chuyển worktree sang ổ thật mà không mất việc dở, và /tmp còn 26%. Ai chạy nhiều agent song song trên git worktree nên đặt worktree lên ổ thật, không để trên tmpfs có hạn mức.
**Bối cảnh:** Điều phối 11 agent song song, mỗi agent một worktree riêng, đặt trong tmpfs 16 GB có hạn mức. Mỗi worktree kéo khoảng 1,3 GB thư viện phụ thuộc.
**Chuyện gì xảy ra:** Khi ghi scratchpad báo EDQUOT, mọi lệnh shell của mọi agent đều hỏng vì hạn mức đã đầy. Lead dừng hết agent, chuyển 11 worktree sang ổ /home bằng git worktree repair mà không mất việc dở. /tmp giảm từ đầy xuống còn 26%. Agent được gửi tin nhắn để resume từ chỗ dừng.
**Bài học:** Đặt worktree và node_modules trên ổ đĩa thật, không đặt trên tmpfs có quota; ghi quy định này vào brief chung của agent.
**Artefact:** Bảng df trước và sau khi chuyển worktree, đã che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Thông thường khi hết đĩa, người dùng hoặc tool sẽ báo lỗi và phải làm lại từ đầu, hoặc xóa bừa để giải phóng chỗ; ở đây khác ở Người đọc sẽ hỏi làm sao di chuyển thư mục đang có tiến trình chạy mà không mất code chưa commit, và làm sao agent biết tiếp tục đúng chỗ.
