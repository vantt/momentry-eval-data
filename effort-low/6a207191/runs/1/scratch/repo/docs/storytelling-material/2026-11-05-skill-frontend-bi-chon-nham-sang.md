---
id: 2026-11-05-skill-frontend-bi-chon-nham-sang
date: 2026-11-05
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L1534", "claude:6a207191#L1538", "claude:6a207191#L1540", "claude:6a207191#L1543", "claude:6a207191#L1555"]
hook: "Hỏi việc frontend, hub lại đưa skill phát hành, dù đã trừ điểm"
tension: cam_ma_van_lot
sides: ["Hub đã trừ điểm vì not_for", "Skill phát hành vẫn thắng việc frontend"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Skill frontend bị chọn nhầm sang skill phát hành

**Bối cảnh:** Agent gọi skill_resolve cho một việc thuần frontend trên web UI.
**Chuyện gì xảy ra:** Lần đầu hub trả về skill đóng gói và phát hành với độ tin cậy medium, tức là chọn nhầm. Agent từ chối kết quả và hỏi lại, lần này nhận no_skill. Routing của skill đóng gói quá rộng nên việc frontend vẫn bị kéo vào. Hub đã trừ điểm vì not_for nhưng skill vẫn thắng.
**Bài học:** Routing cần not_for ngay từ đầu, và phải kiểm bằng những câu nằm gần ranh giới phạm vi, không chỉ bằng câu đúng.
**Artefact:** Kết quả resolve đã che nội dung nhạy cảm.
