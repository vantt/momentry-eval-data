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
---

# Cùng model ONNX, CPU khác, điểm khác: cổng chất lượng đỏ vì baseline ghi trên máy khác

**Bối cảnh:** Cổng chất lượng so nDCG@5 eval tiếng Anh không gói với baseline đã ghi trước đó.
**Chuyện gì xảy ra:** Trên máy agent điểm là 0,735, trên runner GitHub là 0,728, lệch hơn ngưỡng 0,005. Model lượng tử int8 cho số khác nhau theo loại CPU. Cách sửa: cổng so với upstream đo trong cùng lần chạy trên cùng máy; baseline ghi sẵn chỉ còn là cảnh báo trôi. Không hạ baseline nào. Sau sửa, catchup xanh và tag mới được đẩy.
**Bài học:** Đừng so điểm eval giữa hai máy khác loại CPU; đo đối chứng trong cùng một lần chạy.
**Artefact:** Bảng 0,735 và 0,728 đặt cạnh nhau.
**Góc người ngoài:** cách làm phổ biến là Nhiều người khi CI đỏ sẽ nới ngưỡng, bỏ test, hoặc đẩy lại vài lần cho đến khi xanh; ở đây khác ở Người đọc sẽ hỏi vì sao quyết định không hạ ngưỡng được giữ vững qua nhiều lần đỏ, và làm sao phân biệt lỗi thật với lỗi do máy chạy khác.
