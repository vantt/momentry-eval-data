---
id: 2026-11-03-antigravity-khong-co-su-kien-ket
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, người duyệt thứ máy soạn]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3427", "claude:ab9a1dd8#L3428", "claude:ab9a1dd8#L3433"]
hook: "Antigravity không có sự kiện kết thúc, nên gom chuyện lúc mở phiên sau"
tension: khac
sides: ["Muốn gom chuyện khi phiên kết thúc", "Công cụ không có sự kiện đó, phải gom ở phiên sau"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dễ tưởng công cụ AI nào cũng có sự kiện báo khi phiên kết thúc để gom chuyện đúng lúc. Antigravity thì không: chỉ có sự kiện mở phiên và Stop, mà Stop chạy sau mỗi lượt và chặn agent trong lúc chạy, nên phải gom khi mở phiên sau. Ai viết hook cho nhiều công cụ nên kiểm tra sự kiện có sẵn trước khi chọn thời điểm gom."
audience: dev viết hook hoặc extension cho công cụ AI dòng lệnh
---

# Antigravity không có sự kiện kết thúc: gom chuyện khi mở phiên sau

**Góc kể:** Dễ tưởng công cụ AI nào cũng có sự kiện báo khi phiên kết thúc để gom chuyện đúng lúc. Antigravity thì không: chỉ có sự kiện mở phiên và Stop, mà Stop chạy sau mỗi lượt và chặn agent trong lúc chạy, nên phải gom khi mở phiên sau. Ai viết hook cho nhiều công cụ nên kiểm tra sự kiện có sẵn trước khi chọn thời điểm gom.
**Bối cảnh:** Pi và omp có extension TypeScript. Antigravity chỉ có SessionStart và Stop, không có sự kiện kết thúc hay trước compact.
**Chuyện gì xảy ra:** Stop chạy sau mỗi lượt và chặn agent trong lúc chạy, nên không dùng được để gom. Người dùng chọn gom khi mở phiên sau và tự tìm mọi profile. Quyết định này đổi thời điểm gom so với Claude Code.
**Bài học:** Host không có sự kiện kết thúc phiên buộc phải đổi thời điểm gom. Đừng mặc định mọi host đều có SessionEnd.
**Artefact:** Bảng sự kiện hook của Claude Code, Codex, pi, agy. Không cần che.
