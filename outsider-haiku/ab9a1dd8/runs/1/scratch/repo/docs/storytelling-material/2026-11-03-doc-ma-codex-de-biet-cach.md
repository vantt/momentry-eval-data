---
id: 2026-11-03-doc-ma-codex-de-biet-cach
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3099", "claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3138", "claude:ab9a1dd8#L3139", "claude:ab9a1dd8#L3149", "claude:ab9a1dd8#L3213", "claude:ab9a1dd8#L3233"]
hook: "Đọc mã Codex thấy cờ bỏ qua duyệt hook, bật lên hook vẫn im"
tension: giup_ma_hai
sides: ["bật cờ bỏ qua bước duyệt", "hook vẫn không được gọi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc mã Codex để biết cách tin hook, và tìm ra cờ bỏ qua bước duyệt

**Bối cảnh:** Codex yêu cầu duyệt tin cậy cho từng hook qua một trusted_hash. Tự tính hash dễ sai vì phải mô phỏng cách Codex chuẩn hoá cấu hình.
**Chuyện gì xảy ra:** Agent đọc mã nguồn mở của Codex để tìm cơ chế tính hash, rồi tìm thấy cờ bypass_hook_trust. Khi thử trên CI Windows với cờ này, phiên codex không đăng nhập vẫn không gọi hook. Chưa chứng minh được nguyên nhân, vì phiên có thể dừng trước bước hook.
**Bài học:** Khi host có bước duyệt bảo mật, đọc mã nguồn chính xác hơn là tự suy đoán; và một cờ bỏ qua không đồng nghĩa với việc hook chạy được.
**Artefact:** Đoạn cấu hình trusted_hash, che giá trị hash.
