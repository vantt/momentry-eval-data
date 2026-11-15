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
hook: "Tôi push một commit, main mất README.md, 9 job CI đỏ"
tension: nho_ma_to
sides: ["Rebase thường, không force, tưởng an toàn", "Commit mang theo lệnh đổi tên của phiên kia, main mất README"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai phiên cùng làm một repo: commit của tôi kéo theo đổi tên README, main mất README.md và CI đỏ toàn bộ

**Bối cảnh:** Có phiên khác đang làm README song ngữ và đã stage sẵn lệnh đổi tên README.md thành README.vi.md.
**Chuyện gì xảy ra:** Push bị từ chối vì main có 2 commit tài liệu đặt tên. Agent rebase thường lên remote, không force. Sau đó commit e78f3ab mang theo lệnh đổi tên từ phiên kia, nên main không còn README.md và cả 9 job CI đỏ. Chủ dự án chọn commit README song ngữ, CI xanh lại. Từ đó agent chỉ stage đúng file của mình.
**Bài học:** Khi nhiều phiên làm chung repo, index đang stage sẵn có thể kéo theo việc không phải của mình. Luôn kiểm git diff --cached trước khi commit.
**Artefact:** Đầu ra git diff --cached --stat trước commit.
