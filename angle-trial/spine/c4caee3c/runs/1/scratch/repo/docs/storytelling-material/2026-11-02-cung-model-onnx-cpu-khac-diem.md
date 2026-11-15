---
id: 2026-11-02-cung-model-onnx-cpu-khac-diem
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:c4caee3c#L3288", "claude:c4caee3c#L3312", "claude:c4caee3c#L3349", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "Cùng model, khác CPU: 0,735 trên máy agent, 0,728 trên CI"
tension: tuong_ma_hoa_ra
sides: ["Cùng một model ONNX thì cùng điểm", "Lượng tử int8 ra số khác nhau theo CPU, cổng đỏ vì lệch 0,007"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đẩy bản phát hành mới qua CI. Họ tin điểm eval đo trên máy nào cũng như nhau, nên so với baseline ghi sẵn để quyết định đỏ hay xanh. Hoá ra cùng một model ONNX lượng tử int8 cho điểm khác nhau theo loại CPU, nên cổng đỏ vì baseline ghi trên máy khác, không phải vì code sai. Ai so benchmark giữa các máy khác nhau đều có thể gặp đúng chuyện này."
audience: dev làm công cụ có đo chất lượng bằng benchmark trên CI
spine_context: Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá; người làm đang đẩy bản phát hành mới qua CI.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: Muốn CI xanh và phát hành đủ gói cho mọi nền.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "Cổng chất lượng đỏ: điểm eval 0,735 trên một máy, 0,728 trên runner CI, lệch quá ngưỡng 0,005."
spine_obstacle_lines: ["claude:c4caee3c#L3312"]
spine_turn: "Tưởng kết quả eval lặp lại được trên mọi máy; hoá ra chỉ lặp lại trong cùng loại CPU, vì cùng model ONNX lượng tử int8 cho số khác nhau theo CPU."
spine_turn_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3361"]
spine_action: Đổi cổng chất lượng để so với upstream đo trong cùng lần chạy; baseline ghi sẵn chỉ còn là cảnh báo trôi; kiểm tra gói chỉ tính kết quả trên một loại CPU và thử lại tối đa 3 lần.
spine_action_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3370", "claude:c4caee3c#L3388"]
spine_outcome: "CI xanh; release v0.17.2-vantt.3 có đủ 4 gói, run 41410567165 thành công."
spine_outcome_lines: ["claude:c4caee3c#L3415"]
spine_takeaway: Đừng coi điểm eval đo trên máy khác là chuẩn; đo đối chứng trong cùng một lần chạy.
spine_takeaway_lines: ["claude:c4caee3c#L3361"]
completeness: 7
---

# Cùng model ONNX, CPU khác, điểm khác: cổng chất lượng đỏ vì baseline ghi trên máy khác

**Góc kể:** Obsidian Hybrid Search là gói npm tìm ghi chú Obsidian theo nghĩa và từ khoá, và người làm đang đẩy bản phát hành mới qua CI. Họ tin điểm eval đo trên máy nào cũng như nhau, nên so với baseline ghi sẵn để quyết định đỏ hay xanh. Hoá ra cùng một model ONNX lượng tử int8 cho điểm khác nhau theo loại CPU, nên cổng đỏ vì baseline ghi trên máy khác, không phải vì code sai. Ai so benchmark giữa các máy khác nhau đều có thể gặp đúng chuyện này.
**Bối cảnh:** Cổng chất lượng so nDCG@5 eval tiếng Anh không gói với baseline đã ghi trước đó.
**Chuyện gì xảy ra:** Trên máy agent điểm là 0,735, trên runner GitHub là 0,728, lệch hơn ngưỡng 0,005. Model lượng tử int8 cho số khác nhau theo loại CPU. Cách sửa: cổng so với upstream đo trong cùng lần chạy trên cùng máy; baseline ghi sẵn chỉ còn là cảnh báo trôi. Không hạ baseline nào. Sau sửa, catchup xanh và tag mới được đẩy.
**Bài học:** Đừng so điểm eval giữa hai máy khác loại CPU; đo đối chứng trong cùng một lần chạy.
**Artefact:** Bảng 0,735 và 0,728 đặt cạnh nhau.
**Góc người ngoài:** cách làm phổ biến là Nhiều người khi CI đỏ sẽ nới ngưỡng, bỏ test, hoặc đẩy lại vài lần cho đến khi xanh; ở đây khác ở Người đọc sẽ hỏi vì sao quyết định không hạ ngưỡng được giữ vững qua nhiều lần đỏ, và làm sao phân biệt lỗi thật với lỗi do máy chạy khác.
