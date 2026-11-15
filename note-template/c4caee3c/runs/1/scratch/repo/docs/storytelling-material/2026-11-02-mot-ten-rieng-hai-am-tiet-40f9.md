---
id: 2026-11-02-mot-ten-rieng-hai-am-tiet-40f9
code: M-7KC9
aliases: [M-7KC9]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2789", "claude:c4caee3c#L2842", "claude:c4caee3c#L2927"]
hook: "Tên riêng 'phục hồi dấu' thành một cụm vô nghĩa"
tension: giup_ma_hai
sides: ["Phục hồi dấu để tìm kiếm tốt hơn", "Tên riêng bị đổi thành cụm vô nghĩa"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, có tìm theo nghĩa và hỗ trợ tiếng Việt, đang chuẩn bị bản phát hành. Người làm tưởng ngưỡng 'quá nửa chữ có dấu' là chỗ sai, vì tên riêng 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng đúng, lỗi nằm ở cách ghép câu gửi cho model nhúng: tên riêng phải được bảo vệ khỏi mọi bước tự động sửa. Ai xây pipeline tiền xử lý văn bản trước khi nhúng nên để ý, vì lỗi kiểu này im lặng làm sai kết quả tìm kiếm mà không báo gì."
audience: dev xây tìm kiếm hoặc xử lý văn bản tiếng Việt trước khi nhúng
spine_context: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, kết hợp tìm theo nghĩa và từ khoá, có hỗ trợ tiếng Việt."
spine_context_lines: [profile]
spine_want: "Tìm tiếng Việt đúng cả khi câu tìm có dấu, không dấu hoặc chỉ có dấu một phần."
spine_want_lines: ["claude:c4caee3c#L2776"]
spine_obstacle: "Câu tìm có một phần chữ có dấu bị phục hồi dấu sai: tên riêng 'Hội An' thành 'hội ăn'."
spine_obstacle_lines: ["claude:c4caee3c#L2787"]
spine_turn: "Tưởng ngưỡng 50% chữ có dấu là lỗi; hoá ra ngưỡng đúng theo đặc tả, lỗi nằm ở cách ghép câu gửi cho model nhúng."
spine_turn_lines: ["claude:c4caee3c#L2776", "claude:c4caee3c#L2787"]
spine_action: "Thêm test chứng minh lỗi, rồi sửa cách ghép: từ có dấu giữ nguyên, từ không dấu chỉ được phục hồi khi vault không bao giờ viết nó trần và độ tin cậy đủ cao."
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt; tuỳ chọn này được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2789"]
spine_takeaway: Ngưỡng tỷ lệ không phải lỗi; tên riêng cần được bảo vệ khỏi mọi bước tự động sửa trước khi đưa vào model.
spine_takeaway_lines: ["claude:c4caee3c#L2787"]
completeness: 7
---

# Một tên riêng hai âm tiết bị phục hồi sai dấu

**Góc kể:** Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, có tìm theo nghĩa và hỗ trợ tiếng Việt, đang chuẩn bị bản phát hành. Người làm tưởng ngưỡng 'quá nửa chữ có dấu' là chỗ sai, vì tên riêng 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng đúng, lỗi nằm ở cách ghép câu gửi cho model nhúng: tên riêng phải được bảo vệ khỏi mọi bước tự động sửa. Ai xây pipeline tiền xử lý văn bản trước khi nhúng nên để ý, vì lỗi kiểu này im lặng làm sai kết quả tìm kiếm mà không báo gì.
**Bối cảnh:** Khi câu tìm có một phần chữ có dấu, bộ phục hồi dấu được dùng để tạo câu gửi cho model nhúng.
**Chuyện gì xảy ra:** Một tên riêng hai âm tiết có một âm tiết có dấu và một âm tiết không dấu. Tỷ lệ có dấu đúng bằng 50%, không vượt ngưỡng, nên âm tiết không dấu bị phục hồi thành một từ thường hơn trong vault. Tên riêng bị đổi thành một cụm vô nghĩa. Sửa lại để từ có dấu không bị đổi, và chỉ phục hồi từ không dấu khi vault không bao giờ viết nó trần và độ tin cậy đủ cao. Sau khi sửa, nDCG@5 tổng đạt 0,954, mọi hạng mục không tụt.
**Bài học:** Ngưỡng tỷ lệ không phải lỗi. Lỗi là cách ghép câu gửi cho model. Tên riêng cần được bảo vệ khỏi mọi bước tự động sửa.
**Artefact:** Ví dụ một cụm tên riêng bị đổi dấu (đã thay bằng mô tả, không đưa câu thật).
