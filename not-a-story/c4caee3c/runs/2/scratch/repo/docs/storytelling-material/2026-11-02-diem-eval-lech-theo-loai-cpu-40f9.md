---
id: 2026-11-02-diem-eval-lech-theo-loai-cpu-40f9
code: M-A8R2
aliases: [M-A8R2]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo, dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L3312", "claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "Cùng một bài đo, 0,728 trên máy này, 0,735 trên máy kia"
tension: tuong_ma_hoa_ra
sides: ["Con số baseline tưởng đúng ở mọi máy", "Loại CPU khác cho điểm lệch, cổng chất lượng đỏ oan"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một fork công cụ tìm kiếm cho vault Obsidian đang đưa bản phát hành tự động qua CI, và cổng chất lượng của nó đang đỏ. Cổng so số đo với một baseline ghi trên máy khác, và runner GitHub cho số lệch 0,007, vượt ngưỡng 0,005. Người làm tưởng số đo đúng cho mọi máy, nhưng ONNX lượng tử cho số khác nhau theo loại CPU, nên họ đổi cổng sang so với bản upstream đo ngay trong cùng lần chạy. Ai viết cổng chất lượng dựa trên số đo ML nên nghe, vì cách so sánh này dễ làm đỏ oan."
audience: dev viết cổng chất lượng hoặc test dựa trên số đo ML trong CI
spine_context: "Một fork của công cụ tìm kiếm cho vault Obsidian, đang đưa bản phát hành tự động qua CI kèm các cổng chất lượng."
spine_context_lines: [profile]
spine_want: Muốn CI catchup xanh và phát hành tự động trọn vẹn.
spine_want_lines: ["claude:c4caee3c#L3415"]
spine_obstacle: "Baseline ghi trên máy khác là 0,735, runner đo được 0,728, lệch vượt tolerance 0,005 nên cổng chất lượng đỏ."
spine_obstacle_lines: ["claude:c4caee3c#L3312"]
spine_turn: "Tưởng số baseline ghi trên một máy đúng cho mọi máy; hoá ra ONNX lượng tử cho số khác nhau theo loại CPU, nên so số giữa hai máy là sai cách."
spine_turn_lines: ["claude:c4caee3c#L3312", "claude:c4caee3c#L3349"]
spine_action: Đổi cổng so với bản upstream đo trong cùng lần chạy; baseline cũ chỉ còn dùng để báo trôi.
spine_action_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3388"]
spine_outcome: "CI catchup xanh, đẩy v0.17.2-vantt.3 với 4 gói; cổng không còn phụ thuộc số đo của máy khác."
spine_outcome_lines: ["claude:c4caee3c#L3397", "claude:c4caee3c#L3415"]
spine_takeaway: "Đừng so số đo chất lượng giữa các loại máy; đo baseline trong cùng lần chạy, trên cùng loại máy."
spine_takeaway_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3415"]
completeness: 7
---

# Điểm eval lệch theo loại CPU, cổng chất lượng đỏ vì baseline ghi trên máy khác

**Góc kể:** Một fork công cụ tìm kiếm cho vault Obsidian đang đưa bản phát hành tự động qua CI, và cổng chất lượng của nó đang đỏ. Cổng so số đo với một baseline ghi trên máy khác, và runner GitHub cho số lệch 0,007, vượt ngưỡng 0,005. Người làm tưởng số đo đúng cho mọi máy, nhưng ONNX lượng tử cho số khác nhau theo loại CPU, nên họ đổi cổng sang so với bản upstream đo ngay trong cùng lần chạy. Ai viết cổng chất lượng dựa trên số đo ML nên nghe, vì cách so sánh này dễ làm đỏ oan.
**Bối cảnh:** Quantized ONNX cho số hơi khác nhau theo loại CPU của runner GitHub. Baseline ghi trên máy của lead không khớp với runner.
**Chuyện gì xảy ra:** Mục upstream-no-pack đo được 0,728 trên runner, baseline ghi là 0,735, chênh vượt tolerance 0,005. Lead không hạ baseline mà đổi cổng sang so với upstream được đo trong cùng lần chạy, còn baseline chỉ còn báo trôi. Khi đo chênh lệch của gói Mac Intel, ba runner EPYC cho số giống hệt nhau nhưng runner loại khác cho số lệch, nên cổng chỉ đếm kết quả trên EPYC.
**Bài học:** Đừng so số đo chất lượng giữa các loại máy. Đo baseline trong cùng lần chạy, trên cùng loại máy.
**Artefact:** Bảng số đo của ba runner, không kèm nội dung câu hỏi.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ đọc dòng lỗi cuối rồi sửa thử, hoặc re-run cho đến khi xanh; ở đây khác ở Agent đo lại trên nhiều máy, phát hiện kết quả phụ thuộc loại CPU và sửa cổng so sánh thay vì hạ ngưỡng. Người đọc sẽ muốn biết cách phân biệt 'lỗi cần sửa' với 'số đo thay đổi'.
