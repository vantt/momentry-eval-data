---
id: 2026-11-02-mac-intel-onnxruntime-1-30-khong-40f9
code: M-8SXA
aliases: [M-8SXA]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2585", "claude:c4caee3c#L2586", "claude:c4caee3c#L2604", "claude:c4caee3c#L2616", "claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3912", "claude:c4caee3c#L3919"]
hook: "Agent khẳng định kết quả lặp lại, đổi CPU là lệch 0,054"
tension: tuong_ma_hoa_ra
sides: ["Kết quả ổn định giữa các lần chạy", "Đổi loại CPU thì điểm lệch"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang muốn bản phát hành có đủ 4 nền, kể cả Mac Intel. Họ tin điểm đo lặp lại giống nhau trên mọi máy, nhưng khi chạy trên máy CPU khác thì nhóm đa ngôn ngữ lệch tới +0,054; hoá ra điểm của bản ONNX đã nén chỉ ổn định trong cùng một loại CPU. Ai ghim thư viện cũ rồi so điểm giữa các máy đều có thể dính bẫy này."
audience: dev làm công cụ có model nhúng và đo chất lượng tìm kiếm
spine_context: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá; người làm đang đưa bản phát hành đủ 4 nền, gồm Mac Intel."
spine_context_lines: [profile, "claude:c4caee3c#L2592"]
spine_want: "Muốn Mac Intel vẫn là nền bắt buộc, mỗi bản phát hành đủ 4 gói."
spine_want_lines: ["claude:c4caee3c#L2592"]
spine_obstacle: "onnxruntime-node 1.30 không có file dựng cho Mac Intel, nên gói Mac Intel không dựng được."
spine_obstacle_lines: ["claude:c4caee3c#L2592"]
spine_turn: "Tưởng điểm đo lặp lại giống nhau trên mọi máy; hoá ra điểm ONNX đã nén phụ thuộc loại CPU, trên máy khác nhóm đa ngôn ngữ lệch +0,054."
spine_turn_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3361"]
spine_action: Ghim onnxruntime-node 1.23.2 chỉ cho gói Mac Intel; kiểm lệch trên máy EPYC và chỉ tính kết quả trên loại CPU đó.
spine_action_lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3913"]
spine_outcome: "vantt.2 có đủ 4 gói; trên vantt.4, vi-snippet tốt hơn 0,024 và vi-synonym kém 0,021; người dùng chọn chỉ chặn khi tụt quá 0,01."
spine_outcome_lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3912", "claude:c4caee3c#L3919"]
spine_takeaway: "Số đo ONNX đã nén chỉ so sánh được trên cùng loại CPU; khi ghim thư viện, đo với bản gốc trên cùng loại máy và ghi rõ điều kiện đo."
spine_takeaway_lines: ["claude:c4caee3c#L3361"]
completeness: 7
---

# Mac Intel: onnxruntime 1.30 không có bản dựng cho darwin-x64, và điểm eval phụ thuộc loại CPU của runner

**Góc kể:** Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang muốn bản phát hành có đủ 4 nền, kể cả Mac Intel. Họ tin điểm đo lặp lại giống nhau trên mọi máy, nhưng khi chạy trên máy CPU khác thì nhóm đa ngôn ngữ lệch tới +0,054; hoá ra điểm của bản ONNX đã nén chỉ ổn định trong cùng một loại CPU. Ai ghim thư viện cũ rồi so điểm giữa các máy đều có thể dính bẫy này.
**Bối cảnh:** Gói Mac Intel không dựng được vì thư viện ONNX mới nhất không còn file cho Intel, trong khi PRD yêu cầu đủ 4 nền.
**Chuyện gì xảy ra:** Lead đề xuất ghim onnxruntime-node 1.23.2 chỉ cho gói Intel và đo lệch điểm trên cùng máy. Agent ban đầu khẳng định kết quả lặp lại được giữa các lần chạy, nhưng khi chạy trên runner CPU khác, multilingual lệch tới +0,054 và điểm tổng của lần chạy catchup là 0,728 thay vì 0,735. Kết luận đúng là điểm lượng tử hoá ổn định theo từng lớp CPU, không ổn định giữa các lớp. Người dùng chấp nhận lệch đã đo rồi chốt quy tắc chỉ chặn khi tụt quá 0,01.
**Bài học:** Số đo của ONNX lượng tử phụ thuộc phần cứng; khi ghim phiên bản thư viện, đo so với bản gốc trên cùng lớp máy và nói rõ điều kiện đo.
**Artefact:** Bảng lệch điểm theo hạng mục giữa bản ghim và bản gốc (chỉ số, không kèm câu hỏi).
