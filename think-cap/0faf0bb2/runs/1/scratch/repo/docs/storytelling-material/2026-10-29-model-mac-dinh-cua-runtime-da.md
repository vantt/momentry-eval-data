---
id: 2026-10-29-model-mac-dinh-cua-runtime-da
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, ràng buộc định hình thiết kế]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1079", "claude:0faf0bb2#L1115", "claude:0faf0bb2#L1119", "claude:0faf0bb2#L1129", "claude:0faf0bb2#L1137", "claude:0faf0bb2#L1519"]
hook: "Model mặc định bị ngừng, agent chính chết, sửa đúng một session là xong"
tension: nho_ma_to
sides: ["Một model mặc định bị ngừng", "Cả agent chính ngừng chạy, vá bằng một lệnh cho riêng session"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model mặc định của runtime đã ngừng, làm hỏng cả agent chính

**Bối cảnh:** AICoworker/OpenClaw có model mặc định trong openclaw.json, dùng chung cho agent main.
**Chuyện gì xảy ra:** Session của agent báo 'model no longer available' vì model mặc định đã bị ngừng. Thay vì sửa cấu hình chung, spike đổi model riêng cho từng session qua lệnh sessions.patch (trả ok: true). Cách này không làm đổi openclaw.json, và các session khác không bị ảnh hưởng.
**Bài học:** Model mặc định là điểm chết chung; khi cần sửa gấp, đổi ở tầng session để không chạm cấu hình dùng chung.
**Artefact:** Trường model trong session trước (model cũ) và sau (model mới), không kèm key.
