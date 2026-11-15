---
id: 2026-10-21-hoi-dong-kien-truc-qua-framing
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3970", "claude:9514b261#L3987", "claude:9514b261#L3993"]
hook: "Hội đồng qua bước một, gãy ngay ở bước hai"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hội đồng kiến trúc qua framing nhưng shaping thất bại ngay vòng đầu

**Bối cảnh:** Workflow hội đồng chạy nền theo các bước framing, shaping (ba panelist đề xuất mù), critique, synthesis và cổng người.
**Chuyện gì xảy ra:** Framing đánh dấu pass, còn shaping đánh dấu execution-failure. Agent đọc trạng thái từng bước để tìm ghế nào hỏng, và lệnh status trả dạng JSON khác với dự đoán nên lần parse đầu tiên lỗi.
**Bài học:** Workflow có trạng thái riêng cho từng bước giúp biết chính xác chỗ hỏng thay vì phải đoán.
**Artefact:** Sơ đồ các bước với trạng thái từng bước.
