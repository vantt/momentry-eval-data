---
id: 2026-11-03-commit-keo-nham-doi-ten-readme
date: 2026-11-03
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L2733", "claude:ab9a1dd8#L2741", "claude:ab9a1dd8#L2749", "claude:ab9a1dd8#L2766", "claude:ab9a1dd8#L2769", "claude:ab9a1dd8#L2796"]
hook: "Một commit kéo nhầm lệnh đổi tên README, cả CI đỏ"
tension: nho_ma_to
sides: ["một commit kéo theo việc đổi tên README", "main thiếu README.md và toàn bộ CI đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Commit kéo nhầm đổi tên README, main thiếu file và CI đỏ

**Bối cảnh:** Index git dùng chung giữa các phiên làm việc. Một phiên khác đã stage sẵn việc đổi tên README.md thành README.vi.md.
**Chuyện gì xảy ra:** Commit của agent kéo theo việc đổi tên này, nên main thiếu README.md và CI đỏ toàn bộ. Người dùng chọn commit README song ngữ đang có, và sau đó CI xanh lại.
**Bài học:** Khi index git dùng chung, git add đúng tên file và kiểm git diff --cached trước khi commit.
**Artefact:** Kết quả git diff --cached trước commit, chỉ lấy tên file.
**Góc người ngoài:** cách làm phổ biến là Người làm một mình thường tự revert hoặc force push để dọn, và ít khi nhận ra việc stage chung giữa các phiên AI chạy song song; ở đây khác ở Agent chỉ stage đúng file của mình từ đó về sau, và không đụng vào file đang được phiên khác sửa. Người đọc sẽ hỏi cách nhận biết và tách phần việc giữa các phiên.
