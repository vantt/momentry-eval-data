---
id: 2026-11-03-mot-commit-keo-theo-viec-doi-d5ef
code: M-BMJN
aliases: [M-BMJN]
date: 2026-11-03
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2769"]
hook: "Một commit kéo theo việc đổi tên của phiên khác, main mất README"
tension: nho_ma_to
sides: ["Commit chỉ định đưa lên phần việc của mình", "Kéo theo file stage sẵn của phiên khác, main mất README, CI đỏ hết"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry, một công cụ đọc transcript để nhặt chuyện đáng kể, đang đóng gói bản phát hành và muốn CI chạy lần đầu. Agent tưởng commit của mình chỉ có phần việc của mình, nhưng nó kéo theo việc đổi tên README.md do một phiên khác đã stage sẵn, làm main mất README.md và CI đỏ. Điều này đáng nghe vì các phiên AI dùng chung một index git, nên git add -A có thể nhận nhầm thay đổi của người khác."
audience: dev dùng nhiều phiên AI cùng một repo
spine_context: "Hai phiên agent cùng làm một repo momentry, công cụ đọc transcript để nhặt chuyện đáng kể, đang đóng gói bản phát hành theo plan packaging-distribution."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: Muốn đẩy lên GitHub để CI chạy lần đầu cho gói phát hành.
spine_want_lines: ["claude:ab9a1dd8#L2233"]
spine_obstacle: "Commit đã lên main nhưng main thiếu README.md, nên CI đỏ toàn bộ."
spine_obstacle_lines: ["claude:ab9a1dd8#L2749"]
spine_turn: Agent tưởng commit chỉ chứa việc của mình; hoá ra kéo theo việc đổi tên README.md mà phiên khác đã stage sẵn trong index chung.
spine_turn_lines: ["claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2749"]
spine_action: "Sau khi user trả lời, agent kiểm index đang trống và chạy test, rồi commit đúng 4 file, gồm README.md tiếng Anh mới."
spine_action_lines: ["claude:ab9a1dd8#L2750", "claude:ab9a1dd8#L2759", "claude:ab9a1dd8#L2765", "claude:ab9a1dd8#L2766"]
spine_outcome: "Trước commit: 232 test qua, 0 lỗi. CI chạy nền, chưa có kết quả trong trích đoạn."
spine_outcome_lines: ["claude:ab9a1dd8#L2762", "claude:ab9a1dd8#L2773"]
spine_takeaway: "Khi nhiều phiên cùng repo, kiểm git diff --cached trước khi commit và chỉ stage đúng file của mình."
spine_takeaway_lines: ["claude:ab9a1dd8#L2759", "claude:ab9a1dd8#L2765"]
completeness: 7
---

# Một commit kéo theo việc đổi tên README của phiên khác, main mất README.md

**Góc kể:** Dự án momentry, một công cụ đọc transcript để nhặt chuyện đáng kể, đang đóng gói bản phát hành và muốn CI chạy lần đầu. Agent tưởng commit của mình chỉ có phần việc của mình, nhưng nó kéo theo việc đổi tên README.md do một phiên khác đã stage sẵn, làm main mất README.md và CI đỏ. Điều này đáng nghe vì các phiên AI dùng chung một index git, nên git add -A có thể nhận nhầm thay đổi của người khác.
**Bối cảnh:** Hai phiên làm việc cùng một repo, và chúng dùng chung index của git.
**Chuyện gì xảy ra:** Một commit đưa lên main cả việc đổi tên README.md thành README.vi.md mà phiên khác đã stage sẵn. Kết quả là main không còn README.md và CI đỏ toàn bộ. Chủ chọn commit README song ngữ, CI xanh lại. Từ đó agent chỉ stage đúng file của mình và kiểm git diff --cached trước khi commit.
**Bài học:** Các phiên cùng repo chia sẻ một index; git add -A hay commit không chỉ rõ file có thể nhận nhầm thay đổi của phiên khác.
**Artefact:** Kết quả git diff --cached --stat trước commit.
**Góc người ngoài:** cách làm phổ biến là Dev một mình thường `git add -A`, `git stash`, hoặc `push --force` khi bị từ chối; ở đây khác ở Khi nhiều phiên AI cùng làm một repo, chỉ stage đúng file của mình và rebase thay vì force là cách tránh mất việc của phiên khác. Người đọc sẽ hỏi làm sao tránh được.
