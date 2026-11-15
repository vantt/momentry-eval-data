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
angle: "Tưởng thư mục tạm /tmp đủ chỗ cho 11 bản làm việc song song. Hoá ra /tmp có hạn mức, mỗi bản kéo theo khoảng 1,3 GB thư viện nên đầy nhanh; khi đầy, mọi lệnh shell của cả 11 agent cùng hỏng. Ai chạy nhiều agent song song nên kiểm tra chỗ chứa trước khi bắt đầu."
audience: dev chạy nhiều agent AI song song trên máy cá nhân
---

# Worktree trong /tmp làm đầy hạn mức, 11 agent cùng hỏng shell

**Góc kể:** Tưởng thư mục tạm /tmp đủ chỗ cho 11 bản làm việc song song. Hoá ra /tmp có hạn mức, mỗi bản kéo theo khoảng 1,3 GB thư viện nên đầy nhanh; khi đầy, mọi lệnh shell của cả 11 agent cùng hỏng. Ai chạy nhiều agent song song nên kiểm tra chỗ chứa trước khi bắt đầu.
**Bối cảnh:** Điều phối 11 agent song song, mỗi agent một worktree riêng, đặt trong tmpfs 16 GB có hạn mức. Mỗi worktree kéo khoảng 1,3 GB thư viện phụ thuộc.
**Chuyện gì xảy ra:** Khi ghi scratchpad báo EDQUOT, mọi lệnh shell của mọi agent đều hỏng vì hạn mức đã đầy. Lead dừng hết agent, chuyển 11 worktree sang ổ /home bằng git worktree repair mà không mất việc dở. /tmp giảm từ đầy xuống còn 26%. Agent được gửi tin nhắn để resume từ chỗ dừng.
**Bài học:** Đặt worktree và node_modules trên ổ đĩa thật, không đặt trên tmpfs có quota; ghi quy định này vào brief chung của agent.
**Artefact:** Bảng df trước và sau khi chuyển worktree, đã che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Thông thường khi hết đĩa, người dùng hoặc tool sẽ báo lỗi và phải làm lại từ đầu, hoặc xóa bừa để giải phóng chỗ; ở đây khác ở Người đọc sẽ hỏi làm sao di chuyển thư mục đang có tiến trình chạy mà không mất code chưa commit, và làm sao agent biết tiếp tục đúng chỗ.
