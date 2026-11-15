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
hook: "Cùng một bài đo, mỗi loại CPU cho một điểm khác"
tension: tuong_ma_hoa_ra
sides: ["Tưởng điểm eval chỉ phụ thuộc mã", "Điểm lệch 0,728 so với 0,735 chỉ vì loại CPU"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và người làm đang cố đưa một bản fork lên phát hành qua CI tự động. Họ tin điểm eval chỉ phụ thuộc vào mã, nên baseline ghi trên máy mình là chuẩn để cổng chất lượng so với runner. Hoá ra cùng một mã cho điểm khác theo loại CPU: runner đo 0,728 trong khi baseline ghi 0,735, và một bước kiểm cũng đỏ vì cùng lý do. Ai dựng cổng chất lượng bằng số đo có sẵn trên máy khác nên đọc để biết cách đo baseline trong cùng lần chạy, trên cùng loại máy."
audience: dev xây cổng chất lượng CI dựa trên số đo eval
spine_context: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, người làm đang đưa một bản fork lên phát hành qua CI tự động."
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Hoàn tất các mục trong plan roadmap của fork.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Cổng chất lượng CI đỏ ở mục upstream-no-pack: điểm đo trên runner thấp hơn baseline đã ghi trên máy khác."
spine_obstacle_lines: ["claude:c4caee3c#L3312", "claude:c4caee3c#L3349"]
spine_turn: Tưởng điểm eval chỉ phụ thuộc vào mã; hoá ra cùng một mã cho điểm khác theo loại CPU của runner.
spine_turn_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3370"]
spine_action: Đổi cổng chất lượng để so với bản upstream đo trong cùng lần chạy; giới hạn bước kiểm gói về runner EPYC và thử lại khi gặp máy khác.
spine_action_lines: ["claude:c4caee3c#L3370", "claude:c4caee3c#L3388"]
spine_outcome: "CI xanh trở lại, release v0.17.2-vantt.3 có đủ 4 gói; không baseline nào bị hạ."
spine_outcome_lines: ["claude:c4caee3c#L3397", "claude:c4caee3c#L3415"]
spine_takeaway: "Đừng so số đo chất lượng giữa các loại máy; đo baseline trong cùng lần chạy, trên cùng loại máy."
spine_takeaway_lines: ["claude:c4caee3c#L3349"]
completeness: 7
---

# Điểm eval lệch theo loại CPU, cổng chất lượng đỏ vì baseline ghi trên máy khác

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và người làm đang cố đưa một bản fork lên phát hành qua CI tự động. Họ tin điểm eval chỉ phụ thuộc vào mã, nên baseline ghi trên máy mình là chuẩn để cổng chất lượng so với runner. Hoá ra cùng một mã cho điểm khác theo loại CPU: runner đo 0,728 trong khi baseline ghi 0,735, và một bước kiểm cũng đỏ vì cùng lý do. Ai dựng cổng chất lượng bằng số đo có sẵn trên máy khác nên đọc để biết cách đo baseline trong cùng lần chạy, trên cùng loại máy.
**Bối cảnh:** Quantized ONNX cho số hơi khác nhau theo loại CPU của runner GitHub. Baseline ghi trên máy của lead không khớp với runner.
**Chuyện gì xảy ra:** Mục upstream-no-pack đo được 0,728 trên runner, baseline ghi là 0,735, chênh vượt tolerance 0,005. Lead không hạ baseline mà đổi cổng sang so với upstream được đo trong cùng lần chạy, còn baseline chỉ còn báo trôi. Khi đo chênh lệch của gói Mac Intel, ba runner EPYC cho số giống hệt nhau nhưng runner loại khác cho số lệch, nên cổng chỉ đếm kết quả trên EPYC.
**Bài học:** Đừng so số đo chất lượng giữa các loại máy. Đo baseline trong cùng lần chạy, trên cùng loại máy.
**Artefact:** Bảng số đo của ba runner, không kèm nội dung câu hỏi.
**Góc người ngoài:** cách làm phổ biến là Thường người ta chỉ đọc dòng lỗi cuối rồi sửa thử, hoặc re-run cho đến khi xanh; ở đây khác ở Agent đo lại trên nhiều máy, phát hiện kết quả phụ thuộc loại CPU và sửa cổng so sánh thay vì hạ ngưỡng. Người đọc sẽ muốn biết cách phân biệt 'lỗi cần sửa' với 'số đo thay đổi'.
