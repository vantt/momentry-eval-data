---
id: 2026-11-02-khoi-phuc-dau-bien-ten-rieng-40f9
code: M-2N18
aliases: [M-2N18]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2789", "claude:c4caee3c#L2837", "claude:c4caee3c#L2842"]
hook: "Tên riêng có dấu một nửa bị 'khôi phục' thành từ khác"
tension: giup_ma_hai
sides: ["Khôi phục dấu để tìm chính xác hơn", "Tên riêng bị đổi thành từ thường"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và theo từ, và người làm muốn người gõ không dấu vẫn tìm đúng ghi chú có dấu. Họ tưởng ngưỡng 50% (chỉ khôi phục dấu khi câu gần như không có dấu) là chỗ sai, vì \"Hội An\" có một âm tiết có dấu mà \"An\" lại bị đổi thành \"ăn\". Hoá ra ngưỡng đúng; lỗi nằm ở cách dựng câu gửi cho model nhúng, nơi tên riêng bị khôi phục thành từ thường hay gặp hơn trong vault. Ai làm tìm kiếm tiếng Việt có bước tự thêm dấu nên xem bước dựng đầu vào trước khi chỉnh ngưỡng."
audience: dev làm tìm kiếm hoặc embedding tiếng Việt
spine_context: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa, từ khoá và liên kết, chạy cục bộ qua CLI, JSON-lines hoặc MCP."
spine_context_lines: [profile]
spine_want: "Muốn người gõ không dấu vẫn tìm đúng ghi chú tiếng Việt có dấu, nhờ khôi phục dấu cho câu gửi đi nhúng."
spine_want_lines: ["claude:c4caee3c#L2776"]
spine_obstacle: "Trong câu có dấu một phần như \"Hội An\", tên riêng \"An\" bị đổi thành \"ăn\"."
spine_obstacle_lines: ["claude:c4caee3c#L2787"]
spine_turn: "Tưởng ngưỡng 50% là lỗi; hoá ra ngưỡng đúng, lỗi nằm ở cách dựng câu gửi đi nhúng."
spine_turn_lines: ["claude:c4caee3c#L2776", "claude:c4caee3c#L2787"]
spine_action: "Giữ nguyên các từ đã gõ có dấu, chỉ khôi phục từ không dấu khi vault không bao giờ viết nó trần và xác suất đủ cao, rồi thêm test cho \"Hội An\"."
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, nên tuỳ chọn được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2789"]
spine_takeaway: "Khi quy tắc đúng về ngưỡng mà kết quả vẫn sai, xem lại bước dựng đầu vào phía sau nó, đừng chỉnh ngưỡng."
spine_takeaway_lines: ["claude:c4caee3c#L2789"]
completeness: 7
---

# Khôi phục dấu biến tên riêng thành từ thường: ngưỡng không phải lỗi, lỗi nằm ở cách dựng câu embedding

**Góc kể:** Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và theo từ, và người làm muốn người gõ không dấu vẫn tìm đúng ghi chú có dấu. Họ tưởng ngưỡng 50% (chỉ khôi phục dấu khi câu gần như không có dấu) là chỗ sai, vì "Hội An" có một âm tiết có dấu mà "An" lại bị đổi thành "ăn". Hoá ra ngưỡng đúng; lỗi nằm ở cách dựng câu gửi cho model nhúng, nơi tên riêng bị khôi phục thành từ thường hay gặp hơn trong vault. Ai làm tìm kiếm tiếng Việt có bước tự thêm dấu nên xem bước dựng đầu vào trước khi chỉnh ngưỡng.
**Bối cảnh:** Tuỳ chọn restoreForEmbedding đã có nhưng bị tắt mặc định vì gây lỗi trong một số câu có dấu một phần.
**Chuyện gì xảy ra:** Agent đã chứng minh bằng test: một tên riêng hai âm tiết chỉ có một âm tiết có dấu, tỉ lệ 0,5 không vượt ngưỡng nên rơi vào nhánh khôi phục, và âm tiết còn lại bị đổi thành một từ thường hay gặp hơn trong vault. Sửa bằng cách giữ nguyên từ đã gõ có dấu và chỉ khôi phục từ không dấu khi vault không bao giờ viết nó trần và xác suất đủ cao. Sau đó nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, nên tuỳ chọn được bật mặc định.
**Bài học:** Khi một quy tắc đúng về ngưỡng mà kết quả vẫn sai, xem lại bước dựng đầu vào phía sau nó, đừng chỉnh ngưỡng.
**Artefact:** Bảng nDCG@5 trước và sau sửa cho từng hạng mục (không kèm câu truy vấn).
