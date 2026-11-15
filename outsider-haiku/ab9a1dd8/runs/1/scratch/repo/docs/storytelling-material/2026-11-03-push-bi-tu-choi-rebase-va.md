---
id: 2026-11-03-push-bi-tu-choi-rebase-va
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2269", "claude:ab9a1dd8#L2282", "claude:ab9a1dd8#L2290", "claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2777"]
hook: "Một commit của agent âm thầm kéo theo README.md bị đổi tên, CI đỏ toàn bộ"
tension: nho_ma_to
sides: ["một commit tưởng chỉ chứa phần của agent", "main mất README.md, CI đỏ toàn bộ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Push bị từ chối, rebase, và một commit kéo theo file của phiên khác

**Bối cảnh:** Nhiều phiên làm việc trên cùng một repo. Một phiên khác đã stage sẵn việc đổi tên README.
**Chuyện gì xảy ra:** Push bị từ chối vì GitHub có hai commit tài liệu khác, rebase êm. Nhưng một commit của agent vô tình kéo theo việc đổi tên README.md thành README.vi.md mà phiên kia đã stage. Main thiếu README.md và CI đỏ toàn bộ. User chọn commit README song ngữ, CI xanh lại. Từ đó agent chỉ stage đúng file và kiểm git diff --cached trước khi commit.
**Bài học:** Với nhiều phiên trên một repo, hãy kiểm git diff --cached trước mỗi commit; index dùng chung là nguồn lỗi im lặng.
**Artefact:** Git log trước và sau commit sửa.
**Góc người ngoài:** cách làm phổ biến là Commit `git add -A` hoặc bỏ qua, không báo; hoặc force push để dọn; ở đây khác ở Ghi nhận lỗi công khai, sửa bằng lựa chọn của người dùng, và đổi quy tắc làm việc ngay sau đó. Người đọc sẽ hỏi làm sao để phát hiện và báo nhanh như vậy.
