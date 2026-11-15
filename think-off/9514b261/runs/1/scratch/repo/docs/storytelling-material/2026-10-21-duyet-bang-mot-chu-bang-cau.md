---
id: 2026-10-21-duyet-bang-mot-chu-bang-cau
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L262", "claude:9514b261#L1815", "claude:9514b261#L2645", "claude:9514b261#L3300", "claude:9514b261#L3362", "claude:9514b261#L3579"]
hook: "Duyệt cả phiên chỉ bằng một chữ: 'đồng ý', '3', hoặc 'probe đi'"
tension: it_ma_nhieu
sides: ["mỗi lượt duyệt chỉ một từ hoặc một số", "điều khiển cả phiên nhiều vòng quyết định"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Duyệt bằng một chữ: bảng câu hỏi có khuyến nghị, người trả đồng ý hoặc số

**Bối cảnh:** Nhiều quyết định phải chờ người duyệt trong suốt phiên làm việc.
**Chuyện gì xảy ra:** Agent gom các quyết định vào bảng có khuyến nghị và yêu cầu người trả lời bằng đồng ý hoặc số câu muốn đổi. Suốt phiên, người duyệt trả bằng một từ hoặc một số như đồng ý, 3, hay probe đi. Mỗi lượt duyệt ngắn, nhưng phiên có nhiều vòng như vậy.
**Bài học:** Thiết kế câu hỏi duyệt để trả lời bằng một chữ: đánh số lựa chọn, ghi khuyến nghị, nêu rõ điều đồng ý sẽ làm.
**Artefact:** Bảng câu hỏi có số thứ tự và khuyến nghị, không kèm nội dung nhạy cảm.
