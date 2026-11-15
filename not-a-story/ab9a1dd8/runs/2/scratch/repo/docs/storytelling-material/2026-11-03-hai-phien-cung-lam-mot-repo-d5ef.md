---
id: 2026-11-03-hai-phien-cung-lam-mot-repo-d5ef
code: M-8DTA
aliases: [M-8DTA]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L2283", "claude:ab9a1dd8#L2289", "claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2796"]
hook: "Một commit kéo theo lệnh đổi tên: main mất README, 9/9 CI đỏ"
tension: nho_ma_to
sides: ["Rebase thường, không force, tưởng an toàn", "Commit mang theo lệnh đổi tên từ phiên kia, main mất README, CI đỏ toàn bộ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang đẩy commit lên main trong khi một phiên khác cũng làm việc trên cùng repo. Họ tưởng rebase thường, không force, là an toàn; hoá ra một lệnh đổi tên README đã được phiên kia stage sẵn trong index, và commit đẩy lên đã mang theo nó, làm main mất README.md và CI đỏ cả 9 job. Ai chạy nhiều agent trên cùng một repo nên biết index dùng chung có thể chứa việc không phải của mình, và chạy git diff --cached trước mỗi commit là cách chặn lỗi này."
audience: dev chạy nhiều phiên coding agent trên cùng một repo
spine_context: Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent. Người làm đang đẩy commit lên main trong khi một phiên khác cũng làm việc trên cùng repo.
spine_context_lines: [profile]
spine_want: Đẩy commit lên main và giữ CI xanh.
spine_want_lines: ["claude:ab9a1dd8#L2300", "claude:ab9a1dd8#L2749"]
spine_obstacle: Push bị từ chối vì main trên GitHub có commit mà máy này chưa có.
spine_obstacle_lines: ["claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2282"]
spine_turn: "Tưởng rebase thường không force là an toàn. Hoá ra index đã có sẵn lệnh đổi tên README.md thành README.vi.md do phiên khác stage, nên commit e78f3ab mang theo việc đổi tên, main mất README.md và CI đỏ toàn bộ."
spine_turn_lines: ["claude:ab9a1dd8#L2282", "claude:ab9a1dd8#L2290", "claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2749"]
spine_action: "Commit lại đúng 4 file để khôi phục README.md tiếng Anh, sau khi kiểm index trống và toàn bộ test qua."
spine_action_lines: ["claude:ab9a1dd8#L2765", "claude:ab9a1dd8#L2766"]
spine_outcome: CI xanh cả 9 tổ hợp.
spine_outcome_lines: ["claude:ab9a1dd8#L2796", "claude:ab9a1dd8#L2800"]
spine_takeaway: "Khi nhiều phiên cùng làm một repo, index đã stage sẵn có thể kéo theo thay đổi không phải của mình. Chạy git diff --cached trước mỗi commit."
spine_takeaway_lines: ["claude:ab9a1dd8#L2766"]
completeness: 7
---

# Hai phiên cùng làm một repo: commit của tôi kéo theo đổi tên README, main mất README.md và CI đỏ toàn bộ

**Góc kể:** Momentry là công cụ nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang đẩy commit lên main trong khi một phiên khác cũng làm việc trên cùng repo. Họ tưởng rebase thường, không force, là an toàn; hoá ra một lệnh đổi tên README đã được phiên kia stage sẵn trong index, và commit đẩy lên đã mang theo nó, làm main mất README.md và CI đỏ cả 9 job. Ai chạy nhiều agent trên cùng một repo nên biết index dùng chung có thể chứa việc không phải của mình, và chạy git diff --cached trước mỗi commit là cách chặn lỗi này.
**Bối cảnh:** Có phiên khác đang làm README song ngữ và đã stage sẵn lệnh đổi tên README.md thành README.vi.md.
**Chuyện gì xảy ra:** Push bị từ chối vì main có 2 commit tài liệu đặt tên. Agent rebase thường lên remote, không force. Sau đó commit e78f3ab mang theo lệnh đổi tên từ phiên kia, nên main không còn README.md và cả 9 job CI đỏ. Chủ dự án chọn commit README song ngữ, CI xanh lại. Từ đó agent chỉ stage đúng file của mình.
**Bài học:** Khi nhiều phiên làm chung repo, index đang stage sẵn có thể kéo theo việc không phải của mình. Luôn kiểm git diff --cached trước khi commit.
**Artefact:** Đầu ra git diff --cached --stat trước commit.
