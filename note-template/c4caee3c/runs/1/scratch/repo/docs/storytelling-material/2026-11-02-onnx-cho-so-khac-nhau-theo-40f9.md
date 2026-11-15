---
id: 2026-11-02-onnx-cho-so-khac-nhau-theo-40f9
code: M-YF2B
aliases: [M-YF2B]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2569", "claude:c4caee3c#L2585", "claude:c4caee3c#L2893", "claude:c4caee3c#L2899", "claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3912", "claude:c4caee3c#L3919"]
hook: "Agent nói kết quả cố định, nhưng đổi CPU là lệch 0,063"
tension: tuong_ma_hoa_ra
sides: ["Agent tin kết quả là xác định", "Mỗi loại CPU cho một số khác"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian đang đưa gói cài cho macOS Intel lên bản phát hành, nhưng bản onnxruntime mới không có gói cho Intel nên phải ghim bản cũ. Người làm tin kết quả đo của bản ghim là cố định, rồi thấy số đổi theo loại CPU: multilingual lệch +0,063 trên EPYC nhưng +0,054 trên máy khác, còn vi-synonym lúc −0,017 lúc +0,023. Ai làm công cụ có model lượng tử nên đo lại trên đúng loại máy và ghi rõ loại CPU trong kết quả."
audience: dev làm công cụ chạy model lượng tử trên máy người dùng
spine_context: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang đưa gói cài có model lên bản phát hành cho Windows, Mac và Linux."
spine_context_lines: [profile]
spine_want: "Muốn có gói chạy được trên macOS Intel, nên ghim onnxruntime-node 1.23.2 chỉ cho gói này."
spine_want_lines: ["claude:c4caee3c#L2579"]
spine_obstacle: onnxruntime-node 1.30.0 mà upstream dùng không có bản dựng sẵn cho darwin-x64.
spine_obstacle_lines: ["claude:c4caee3c#L2553"]
spine_turn: "Tưởng kết quả đo của bản ghim là xác định; hoá ra số đổi theo loại CPU, chỉ lặp lại được trên cùng một loại máy."
spine_turn_lines: ["claude:c4caee3c#L2890", "claude:c4caee3c#L3361"]
spine_action: "Tách phép kiểm lệch sang cùng một loại CPU (AMD EPYC), thử lại trên runner khác khi gặp máy khác, và đổi tiêu chí sang chỉ chặn khi có hạng mục tụt quá 0,01."
spine_action_lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3919"]
spine_outcome: "Release vantt.2 có đủ 4 gói. Ở vantt.4, gói Mac Intel vẫn chưa lên vì vi-snippet lệch mới +0,024 và đang chờ quyết định."
spine_outcome_lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3912"]
spine_takeaway: "Kết quả model lượng tử phụ thuộc phần cứng: đo lại trên cùng loại máy và ghi rõ loại CPU cùng tiêu chí đã đổi bao nhiêu lần."
spine_takeaway_lines: ["claude:c4caee3c#L3361"]
completeness: 7
---

# ONNX cho số khác nhau theo CPU, tiêu chí Mac Intel đổi ba lần

**Góc kể:** Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian đang đưa gói cài cho macOS Intel lên bản phát hành, nhưng bản onnxruntime mới không có gói cho Intel nên phải ghim bản cũ. Người làm tin kết quả đo của bản ghim là cố định, rồi thấy số đổi theo loại CPU: multilingual lệch +0,063 trên EPYC nhưng +0,054 trên máy khác, còn vi-synonym lúc −0,017 lúc +0,023. Ai làm công cụ có model lượng tử nên đo lại trên đúng loại máy và ghi rõ loại CPU trong kết quả.
**Bối cảnh:** macOS Intel cần onnxruntime-node, nhưng bản 1.30 không có binary cho darwin-x64. Chủ dự án chọn ghim bản 1.23.2 chỉ cho gói này.
**Chuyện gì xảy ra:** Tiêu chí đầu là lệch so với Linux dưới 0,01, nhưng bản ARM không ghim cũng lệch 0,063, vì ONNX lượng tử cho số khác nhau theo CPU. Tiêu chí thứ hai đo trên cùng máy. Kết quả: multilingual +0,063, vi-synonym −0,017, và trên một CPU khác thì baseline upstream là 0,728 thay vì 0,735. Tiêu chí cuối cùng do chủ dự án chọn: chỉ chặn khi có hạng mục tụt quá 0,01. Agent từng nói kết quả là xác định, nhưng thực ra chỉ xác định trên cùng một loại CPU.
**Bài học:** Kết quả model lượng tử phụ thuộc phần cứng. Đo lại trên cùng loại máy, và ghi rõ tiêu chí đã đổi bao nhiêu lần cùng lý do.
**Artefact:** Bảng chênh lệch điểm theo hạng mục giữa bản ghim và bản gốc (không nhạy cảm).
