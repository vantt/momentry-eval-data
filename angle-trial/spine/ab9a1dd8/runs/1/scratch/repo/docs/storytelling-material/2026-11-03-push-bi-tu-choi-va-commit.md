---
id: 2026-11-03-push-bi-tu-choi-va-commit
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L2266", "claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2289", "claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766"]
hook: "Một commit làm main mất README và CI đỏ toàn bộ"
tension: nho_ma_to
sides: ["Rebase rồi push, một commit bình thường", "Kéo theo việc đổi tên của phiên khác, main mất README"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry đang chuẩn bị đóng gói và phát hành: cài bằng một lệnh, có README, và CI chạy trên Linux, macOS, Windows. Khi đẩy lên main thì bị từ chối vì GitHub có commit mới; sau khi rebase, commit lại kéo theo việc đổi tên README.md của một phiên khác đã stage sẵn trong cùng index, nên main mất README.md và CI đỏ. Người làm tưởng commit chỉ có file của mình, nhưng index dùng chung không báo trước điều đó. Ai chạy nhiều phiên agent trên cùng một repo nên kiểm `git diff --cached` trước khi commit."
audience: dev chạy nhiều phiên AI agent trên cùng một repo
spine_context: "Dự án momentry đang chuẩn bị đóng gói và phát hành: cài bằng một lệnh, có README, và CI chạy trên nhiều hệ điều hành."
spine_context_lines: ["claude:ab9a1dd8#L664", "claude:ab9a1dd8#L2260"]
spine_want: Đẩy bản đóng gói và tài liệu lên main để CI chạy.
spine_want_lines: ["claude:ab9a1dd8#L2233", "claude:ab9a1dd8#L2266"]
spine_obstacle: Push bị từ chối vì main trên GitHub có commit mà máy này chưa có.
spine_obstacle_lines: ["claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2282"]
spine_turn: "Tưởng commit chỉ chứa file của mình; hoá ra index dùng chung đã có sẵn việc đổi tên README.md thành README.vi.md của phiên khác, và commit kéo theo việc đó."
spine_turn_lines: ["claude:ab9a1dd8#L2288", "claude:ab9a1dd8#L2733"]
spine_action: "Rebase lên origin/main rồi push. Sau khi người dùng chọn hướng xử lý, commit lại README tiếng Anh mới cùng README.vi.md."
spine_action_lines: ["claude:ab9a1dd8#L2750", "claude:ab9a1dd8#L2766"]
spine_outcome: "Test cục bộ: 232 pass, 0 fail, gồm test README song ngữ. Kết quả CI không có trong đoạn trích."
spine_outcome_lines: ["claude:ab9a1dd8#L2762"]
spine_takeaway: "Khi nhiều phiên dùng chung index, `git add` đúng file của mình và xem `git diff --cached` trước khi commit."
spine_takeaway_lines: ["claude:ab9a1dd8#L2759", "claude:ab9a1dd8#L2766"]
completeness: 7
---

# Push bị từ chối, và commit kéo theo việc đổi tên README của phiên khác

**Góc kể:** Dự án momentry đang chuẩn bị đóng gói và phát hành: cài bằng một lệnh, có README, và CI chạy trên Linux, macOS, Windows. Khi đẩy lên main thì bị từ chối vì GitHub có commit mới; sau khi rebase, commit lại kéo theo việc đổi tên README.md của một phiên khác đã stage sẵn trong cùng index, nên main mất README.md và CI đỏ. Người làm tưởng commit chỉ có file của mình, nhưng index dùng chung không báo trước điều đó. Ai chạy nhiều phiên agent trên cùng một repo nên kiểm `git diff --cached` trước khi commit.
**Bối cảnh:** Agent commit nhiều file rồi push lên main. Một phiên làm việc khác dùng chung index và đã stage sẵn việc đổi tên README.md thành README.vi.md.
**Chuyện gì xảy ra:** Push bị từ chối vì main trên GitHub có 2 commit mới, agent rebase rồi push. Commit của agent kéo theo việc đổi tên đã stage sẵn, nên main mất README.md và CI đỏ toàn bộ. Người dùng chọn commit README song ngữ, sau đó CI xanh lại.
**Bài học:** Khi nhiều phiên dùng chung index, hãy `git add <file>` đúng file của mình và kiểm `git diff --cached` trước khi commit.
**Artefact:** Đồ thị git log quanh sự cố. Không có nội dung riêng tư.
