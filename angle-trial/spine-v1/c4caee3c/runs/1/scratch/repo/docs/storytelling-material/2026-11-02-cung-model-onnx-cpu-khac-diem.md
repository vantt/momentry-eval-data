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
angle: "Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang hoàn tất roadmap phát hành bản fork có cổng chất lượng đo bằng điểm eval. Nhóm tin baseline 0,735 là điểm cố định của model, nhưng cùng một model ONNX lượng tử cho điểm khác theo loại CPU: runner GitHub đo 0,728, lệch quá ngưỡng nên cổng đỏ. Cách sửa là so với bản upstream đo trong cùng lần chạy, không hạ baseline nào, và lượt catchup sau đó xanh. Ai đặt ngưỡng từ số đo trên máy khác có thể gặp đúng lỗi này."
audience: dev xây công cụ có test chất lượng bằng số
spine_context: Obsidian Hybrid Search là công cụ tìm kiếm ghi chú Obsidian; nhóm đang hoàn tất roadmap phát hành bản fork.
spine_context_lines: [profile, "claude:c4caee3c#L11"]
spine_want: "Muốn hoàn tất roadmap, trong đó lượt catchup phải xanh để phát hành."
spine_want_lines: ["claude:c4caee3c#L11", "claude:c4caee3c#L3349"]
spine_obstacle: "Lượt catchup đỏ ở mục upstream-no-pack: 0,728 trên runner so với baseline 0,735, lệch quá ngưỡng 0,005."
spine_obstacle_lines: ["claude:c4caee3c#L3312"]
spine_turn: "Tưởng 0,735 là điểm cố định của model; hoá ra cùng model ONNX lượng tử cho điểm khác theo loại CPU, nên so số giữa hai máy là sai."
spine_turn_lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3361"]
spine_action: "Đổi cổng so với upstream đo trong cùng lần chạy trên cùng máy; baseline ghi sẵn chỉ còn báo độ trôi, không hạ baseline nào."
spine_action_lines: ["claude:c4caee3c#L3388"]
spine_outcome: Catchup run 41410567165 xanh; phát hành v0.17.2-vantt.3 với đủ 4 gói.
spine_outcome_lines: ["claude:c4caee3c#L3410", "claude:c4caee3c#L3415"]
spine_takeaway: Đừng so điểm eval giữa hai máy khác loại CPU; đo đối chứng trong cùng một lần chạy.
spine_takeaway_lines: ["claude:c4caee3c#L3361"]
completeness: 7
---

# Cùng model ONNX, CPU khác, điểm khác: cổng chất lượng đỏ vì baseline ghi trên máy khác

**Góc kể:** Obsidian Hybrid Search là công cụ tìm ghi chú Obsidian, và nhóm đang hoàn tất roadmap phát hành bản fork có cổng chất lượng đo bằng điểm eval. Nhóm tin baseline 0,735 là điểm cố định của model, nhưng cùng một model ONNX lượng tử cho điểm khác theo loại CPU: runner GitHub đo 0,728, lệch quá ngưỡng nên cổng đỏ. Cách sửa là so với bản upstream đo trong cùng lần chạy, không hạ baseline nào, và lượt catchup sau đó xanh. Ai đặt ngưỡng từ số đo trên máy khác có thể gặp đúng lỗi này.
**Bối cảnh:** Cổng chất lượng so nDCG@5 eval tiếng Anh không gói với baseline đã ghi trước đó.
**Chuyện gì xảy ra:** Trên máy agent điểm là 0,735, trên runner GitHub là 0,728, lệch hơn ngưỡng 0,005. Model lượng tử int8 cho số khác nhau theo loại CPU. Cách sửa: cổng so với upstream đo trong cùng lần chạy trên cùng máy; baseline ghi sẵn chỉ còn là cảnh báo trôi. Không hạ baseline nào. Sau sửa, catchup xanh và tag mới được đẩy.
**Bài học:** Đừng so điểm eval giữa hai máy khác loại CPU; đo đối chứng trong cùng một lần chạy.
**Artefact:** Bảng 0,735 và 0,728 đặt cạnh nhau.
**Góc người ngoài:** cách làm phổ biến là Nhiều người khi CI đỏ sẽ nới ngưỡng, bỏ test, hoặc đẩy lại vài lần cho đến khi xanh; ở đây khác ở Người đọc sẽ hỏi vì sao quyết định không hạ ngưỡng được giữ vững qua nhiều lần đỏ, và làm sao phân biệt lỗi thật với lỗi do máy chạy khác.
