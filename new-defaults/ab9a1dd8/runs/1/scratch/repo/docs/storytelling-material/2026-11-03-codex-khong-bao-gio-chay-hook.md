---
id: 2026-11-03-codex-khong-bao-gio-chay-hook
date: 2026-11-03
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước sau]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3192", "claude:ab9a1dd8#L3195", "claude:ab9a1dd8#L3205", "claude:ab9a1dd8#L3228", "claude:ab9a1dd8#L3239"]
hook: "Codex bỏ qua mọi hook vì viết sai kiểu chữ hoa thường"
tension: nho_ma_to
sides: ["Chỉ sai snake_case thay vì PascalCase", "Codex không bao giờ chạy hook và không báo lỗi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Codex không bao giờ chạy hook: tên sự kiện sai, bị bỏ không báo

**Bối cảnh:** Momentry ghi cấu hình hook cho Codex, và hook được coi là đã cài.
**Chuyện gì xảy ra:** Codex yêu cầu tên sự kiện dạng PascalCase, còn momentry ghi snake_case, nên Codex bỏ qua hook mà không báo lỗi. Agent đổi thành PreCompact, SessionEnd, SessionStart, rồi thử chạy codex exec trên Windows vẫn không thấy hook gọi.
**Bài học:** Hook sai tên sự kiện thường bị host bỏ im lặng. Hãy đo bằng log do chính hook ghi, không đo bằng việc cấu hình đã được ghi.
**Artefact:** Đoạn hooks.json trước và sau khi đổi tên sự kiện.
