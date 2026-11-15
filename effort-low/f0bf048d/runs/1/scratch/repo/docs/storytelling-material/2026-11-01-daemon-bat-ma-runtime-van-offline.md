---
id: 2026-11-01-daemon-bat-ma-runtime-van-offline
date: 2026-11-01
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước số sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L2897", "claude:f0bf048d#L2908", "claude:f0bf048d#L2937", "claude:f0bf048d#L2938", "claude:f0bf048d#L2948"]
hook: "Daemon bật mà runtime vẫn offline: do một cái tên đổi dở"
tension: nho_ma_to
sides: ["Chỉ đổi tên một lệnh bọc trước khi cài lệnh mới", "Daemon bỏ qua runtime, offline cho đến khi tắt rồi bật lại"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Daemon bật mà runtime vẫn offline: profile chỉ được dò lại khi bị sửa

**Bối cảnh:** Ba runtime (Codex, Grok, Gemini qua pi/omp) đã tạo cùng lệnh bọc, nhưng sau khi cài, runtime OpenAI vẫn offline.
**Chuyện gì xảy ra:** Lúc tạo profile, tên lệnh bọc là pi-openai-codex; sau đó đổi tên thành pi-openai-tetnu trước khi cài lệnh mới, nên daemon không tìm thấy lệnh và bỏ qua. Daemon chỉ dò lại profile khi profile bị sửa, nên tắt rồi bật lại là lên ngay. Từ 2 runtime online ra 3 runtime online, cả hai workspace.
**Bài học:** Đổi tên một thứ daemon đã đọc mà không báo cho nó thì nó không tự nhận lại; sửa profile để kích hoạt dò lại.
**Artefact:** Bảng 3 runtime với lệnh bọc và trạng thái online/offline; che ID.
