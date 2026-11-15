---
id: 2026-11-03-doc-ma-nguon-codex-de-tim-d5ef
code: M-DX49
aliases: [M-DX49]
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L3106", "claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3139", "claude:ab9a1dd8#L3149"]
hook: "Đọc mã nguồn mở tìm ra cờ bỏ qua duyệt hook"
tension: cam_ma_van_lot
sides: ["Codex bắt duyệt hook bằng hash", "có cờ --dangerously-bypass-hook-trust, agent chỉ dùng trong probe chạy tay"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc mã nguồn Codex để tìm cách duyệt hook

**Bối cảnh:** Codex yêu cầu duyệt tin cậy từng hook qua một trusted_hash. Agent không muốn tự tính hash vì dễ sai.
**Chuyện gì xảy ra:** Agent đọc mã nguồn mở của Codex để xem cách tính hash, sau đó tìm thấy cờ --dangerously-bypass-hook-trust. Agent chỉ dùng cờ này trong workflow probe chạy tay, không đưa vào cài đặt của người dùng.
**Bài học:** Khi host có cơ chế duyệt, đọc mã nguồn của nó tốt hơn đoán. Cờ bỏ qua duyệt chỉ nên dùng trong môi trường thử.
**Artefact:** Đoạn mã nguồn Codex về discovery hook. Không cần che.
