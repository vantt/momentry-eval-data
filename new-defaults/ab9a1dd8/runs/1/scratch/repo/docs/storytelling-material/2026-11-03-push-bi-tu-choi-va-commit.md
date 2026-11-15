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
---

# Push bị từ chối, và commit kéo theo việc đổi tên README của phiên khác

**Bối cảnh:** Agent commit nhiều file rồi push lên main. Một phiên làm việc khác dùng chung index và đã stage sẵn việc đổi tên README.md thành README.vi.md.
**Chuyện gì xảy ra:** Push bị từ chối vì main trên GitHub có 2 commit mới, agent rebase rồi push. Commit của agent kéo theo việc đổi tên đã stage sẵn, nên main mất README.md và CI đỏ toàn bộ. Người dùng chọn commit README song ngữ, sau đó CI xanh lại.
**Bài học:** Khi nhiều phiên dùng chung index, hãy `git add <file>` đúng file của mình và kiểm `git diff --cached` trước khi commit.
**Artefact:** Đồ thị git log quanh sự cố. Không có nội dung riêng tư.
