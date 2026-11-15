---
id: 2026-11-02-chon-model-nhung-khi-chenh-lech-40f9
code: M-5XWE
aliases: [M-5XWE]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2733", "claude:c4caee3c#L2776"]
hook: "Các model nhúng chênh nhau vài câu, nhỏ hơn nhiễu của bộ 255 câu"
tension: tuong_ma_hoa_ra
sides: ["Tưởng model đắt hơn là tốt hơn", "Chênh lệch chỉ bằng nhiễu của bộ đo"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian đang hoàn tất roadmap và sửa lỗi gói tiếng Việt. Người làm tưởng ngưỡng 50% khi phục hồi dấu gây ra việc 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng đúng theo PRD, lỗi nằm ở cách dựng câu truy vấn gửi cho model nhúng. Ai làm tìm kiếm tiếng Việt nên biết: test tái hiện trước khi đổi ngưỡng tránh được sửa nhầm chỗ."
audience: dev làm tìm kiếm hoặc xử lý văn bản tiếng Việt
spine_context: "Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian, đang hoàn tất roadmap và sửa lỗi gói tiếng Việt."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Muốn hoàn tất plan roadmap bằng các agent chạy song song, và chốt cấu hình tìm kiếm tiếng Việt."
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Tìm theo câu có dấu một phần, ví dụ 'Hội An', trả về kết quả sai vì câu truy vấn bị đổi chữ."
spine_obstacle_lines: ["claude:c4caee3c#L2776"]
spine_turn: "Tưởng ngưỡng 50% khi phục hồi dấu là nguyên nhân; hoá ra ngưỡng đúng theo PRD, lỗi nằm ở cách dựng câu truy vấn gửi cho model nhúng."
spine_turn_lines: ["claude:c4caee3c#L2776", "claude:c4caee3c#L2787"]
spine_action: "Viết test tái hiện lỗi trên code cũ, rồi sửa cách dựng truy vấn: từ đã có dấu không bị đổi, từ không dấu chỉ được phục hồi khi chắc chắn."
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt; tuỳ chọn phục hồi dấu giờ bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789"]
spine_takeaway: "Khi lỗi có vẻ nằm ở một ngưỡng, hãy tái hiện bằng test trước: ngưỡng có thể đúng và lỗi nằm ở chỗ khác."
spine_takeaway_lines: ["claude:c4caee3c#L2787"]
completeness: 7
---

# Chọn model nhúng khi chênh lệch nhỏ hơn nhiễu

**Góc kể:** Một công cụ tìm kiếm chạy cục bộ trên kho ghi chú Obsidian đang hoàn tất roadmap và sửa lỗi gói tiếng Việt. Người làm tưởng ngưỡng 50% khi phục hồi dấu gây ra việc 'Hội An' bị đổi thành 'hội ăn'. Hoá ra ngưỡng đúng theo PRD, lỗi nằm ở cách dựng câu truy vấn gửi cho model nhúng. Ai làm tìm kiếm tiếng Việt nên biết: test tái hiện trước khi đổi ngưỡng tránh được sửa nhầm chỗ.
**Bối cảnh:** Đo năm cấu hình model và reranker trên 255 câu của bộ sinh.
**Chuyện gì xảy ra:** nDCG@5 nằm trong khoảng 0,932 đến 0,956. Chênh lệch giữa các model chỉ vài câu, nhỏ hơn nhiễu của bộ 255 câu. Khuyến nghị: bật restoreForEmbedding, reranker tắt mặc định, giữ e5-small, dùng bge-m3 cho hồ sơ chất lượng cao. Reranker tăng 0,05 đến 0,10 vi-semantic nhưng thêm 150 ms mỗi câu và 616 MB tải về.
**Bài học:** Khi chênh lệch giữa các lựa chọn nhỏ hơn độ nhiễu của bộ đo, chọn theo chi phí và đo lại trên dữ liệu thật.
**Artefact:** Bảng nDCG@5 theo model và cấu hình (không nhạy cảm).
