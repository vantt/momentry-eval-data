---
id: 2026-11-05-agent-khang-dinh-hub-khong-co
date: 2026-11-05
repo: repo
status: raw
signals: [đảo quyết định, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L1396", "claude:6a207191#L1400", "claude:6a207191#L1406", "claude:6a207191#L1414", "claude:6a207191#L1417", "claude:6a207191#L1441", "claude:6a207191#L1445"]
hook: "Agent nói 'hub không có routing', trong khi hub có 9 trigger"
tension: tuong_ma_hoa_ra
sides: ["Agent khẳng định skill chưa có routing", "Hub thật sự có 9 trigger, 5 example, 5 not_for"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent khẳng định 'hub không có routing' khi máy khách không đọc được

**Bối cảnh:** Agent định bổ sung skill.yaml cho routing, và viết bản nháp trước.
**Chuyện gì xảy ra:** Agent nói skill chưa có topic hay routing vì chỉ kiểm tra thư mục local, nơi không có skill.yaml. User hỏi lại vì trước đó vẫn thấy triggers. Trên hub có 9 trigger, 5 example và 5 not_for. Lệnh skill show --verbose bị từ chối từ máy khách, còn skill_get chỉ trả triggers, không trả operations, topics, technologies hay min_scope. Agent phải đọc source để biết các trường đó tồn tại.
**Bài học:** Đừng kết luận là 'không có' khi công cụ của mình không đọc được. Hãy nói rõ đã nhìn ở đâu, local hay hub.
**Artefact:** Bảng các trường routing và nguồn đọc được từ mỗi chỗ. Ẩn nội dung routing thật.
