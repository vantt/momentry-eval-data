---
id: 2026-11-02-cong-g0-cau-tra-loi-tu
date: 2026-11-02
repo: repo
status: raw
signals: [người duyệt]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L483", "claude:2dfb5915#L486", "claude:2dfb5915#L555", "claude:2dfb5915#L563"]
hook: "User chỉ nói 'như vậy đã sẵn sàng', agent coi là lệnh mở cổng"
tension: nho_ma_to
sides: ["một câu trả lời tự do", "được hiểu thành lệnh mở cổng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cổng G0: câu trả lời tự do được hiểu thành lệnh mở cổng

**Bối cảnh:** Plan có cổng G0 trước phase 08, cần user xác nhận đã chạy thử và một tuần không đổi schema.
**Chuyện gì xảy ra:** User trả lời 'như vậy đã sẵn sàng chạy thử' và agent coi đó là mở cổng. Agent ghi rõ rủi ro còn lại: nếu schema phía Python đổi thì phải làm lại một phần, và sẽ bắt kịp bằng lệnh follow.
**Bài học:** Cổng duyệt nên có lựa chọn rõ ràng, và ghi lại câu trả lời kèm phạm vi.
**Artefact:** Hộp câu hỏi và câu trả lời, che nội dung câu hỏi thật.
