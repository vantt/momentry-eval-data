---
id: 2026-11-03-antigravity-khong-co-su-kien-ket-d5ef
code: M-R0EZ
aliases: [M-R0EZ]
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3427", "claude:ab9a1dd8#L3428", "claude:ab9a1dd8#L3433"]
hook: "Antigravity không có sự kiện kết thúc, nên gom chuyện khi mở phiên sau"
tension: khac
sides: ["Claude Code gom khi phiên kết thúc", "Antigravity chỉ gom được khi mở phiên sau"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Antigravity không có sự kiện kết thúc: gom chuyện khi mở phiên sau

**Bối cảnh:** Pi và omp có extension TypeScript. Antigravity chỉ có SessionStart và Stop, không có sự kiện kết thúc hay trước compact.
**Chuyện gì xảy ra:** Stop chạy sau mỗi lượt và chặn agent trong lúc chạy, nên không dùng được để gom. Người dùng chọn gom khi mở phiên sau và tự tìm mọi profile. Quyết định này đổi thời điểm gom so với Claude Code.
**Bài học:** Host không có sự kiện kết thúc phiên buộc phải đổi thời điểm gom. Đừng mặc định mọi host đều có SessionEnd.
**Artefact:** Bảng sự kiện hook của Claude Code, Codex, pi, agy. Không cần che.
