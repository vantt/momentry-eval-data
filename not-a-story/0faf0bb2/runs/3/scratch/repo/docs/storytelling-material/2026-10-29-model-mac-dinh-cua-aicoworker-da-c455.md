---
id: 2026-10-29-model-mac-dinh-cua-aicoworker-da-c455
code: M-PRK1
aliases: [M-PRK1]
date: 2026-10-29
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:0faf0bb2#L1079", "claude:0faf0bb2#L1080", "claude:0faf0bb2#L1115", "claude:0faf0bb2#L2410"]
hook: "Agent chính hỏng vì model đã ngừng, dù bạn không hề chạy thử nghiệm"
tension: nho_ma_to
sides: ["Spike chỉ đổi model theo từng session, tưởng không đụng gì tới agent chính", "Model mặc định đã ngừng nên agent chính vẫn hỏng khi dùng bình thường"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Model mặc định của AICoworker đã ngừng, làm hỏng cả agent chính ngay cả khi không chạy spike

**Bối cảnh:** Trong spike Paperclip, agent không chạy được. Gốc nằm ở cấu hình model, không nằm ở Paperclip như mọi người nghĩ.
**Chuyện gì xảy ra:** Model mặc định gemini-3-pro-low đã không còn khả dụng, nên agent main hỏng ngay cả khi dùng bình thường. Spike chỉ đổi model theo từng session (gemini-3-flash) chứ không sửa openclaw.json, nên lỗi vẫn còn.
**Bài học:** Một model bị ngừng có thể làm hỏng cả hệ thống agent mà không ai nhận ra, vì mọi người nghi ngờ lớp điều phối trước.
**Artefact:** Ảnh chụp danh sách model trong cấu hình (che API key).
