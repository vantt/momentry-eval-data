---
id: 2026-11-02-worktree-trong-tmp-lam-day-han-40f9
code: M-VSQ6
aliases: [M-VSQ6]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:c4caee3c#L492", "claude:c4caee3c#L508", "claude:c4caee3c#L621", "claude:c4caee3c#L632", "claude:c4caee3c#L740"]
hook: "/tmp đầy hạn mức, 11 agent hỏng shell cùng lúc"
tension: nho_ma_to
sides: ["một thư mục tạm đầy hạn mức", "11 agent mất shell cùng lúc"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Worktree trong /tmp làm đầy hạn mức, 11 agent cùng hỏng shell

**Bối cảnh:** Điều phối 11 agent song song, mỗi agent một worktree riêng, đặt trong tmpfs 16 GB có hạn mức. Mỗi worktree kéo khoảng 1,3 GB thư viện phụ thuộc.
**Chuyện gì xảy ra:** Khi ghi scratchpad báo EDQUOT, mọi lệnh shell của mọi agent đều hỏng vì hạn mức đã đầy. Lead dừng hết agent, chuyển 11 worktree sang ổ /home bằng git worktree repair mà không mất việc dở. /tmp giảm từ đầy xuống còn 26%. Agent được gửi tin nhắn để resume từ chỗ dừng.
**Bài học:** Đặt worktree và node_modules trên ổ đĩa thật, không đặt trên tmpfs có quota; ghi quy định này vào brief chung của agent.
**Artefact:** Bảng df trước và sau khi chuyển worktree, đã che đường dẫn.
**Góc người ngoài:** cách làm phổ biến là Thông thường khi hết đĩa, người dùng hoặc tool sẽ báo lỗi và phải làm lại từ đầu, hoặc xóa bừa để giải phóng chỗ; ở đây khác ở Người đọc sẽ hỏi làm sao di chuyển thư mục đang có tiến trình chạy mà không mất code chưa commit, và làm sao agent biết tiếp tục đúng chỗ.
