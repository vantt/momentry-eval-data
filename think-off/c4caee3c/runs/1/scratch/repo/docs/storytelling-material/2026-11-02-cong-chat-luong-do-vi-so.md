---
id: 2026-11-02-cong-chat-luong-do-vi-so
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3349", "claude:c4caee3c#L3371", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "Chênh 0,007 điểm giữa hai loại CPU làm cổng chất lượng đỏ"
tension: nho_ma_to
sides: ["Lệch 0,007 điểm do loại CPU khác nhau", "Cả cổng chất lượng đỏ dù mã không sai"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Cổng chất lượng đỏ vì số baseline ghi trên máy khác loại CPU

**Bối cảnh:** Cổng chất lượng so điểm nDCG@5 của bản không có gói với một baseline đã ghi trước đó, sai số tối đa 0,005.
**Chuyện gì xảy ra:** Trên máy agent, điểm eval tiếng Anh upstream là 0,735, còn runner GitHub đo được 0,728, vượt ngưỡng 0,005 và làm catchup đỏ. ONNX lượng tử hoá cho số hơi khác nhau theo loại CPU. Sửa đổi: cổng so với upstream được đo ngay trong cùng lần chạy, trên cùng máy; baseline đã ghi chỉ còn dùng để báo độ trôi. Cùng nguyên nhân sau đó cũng khiến bước so sánh gói Intel chỉ ổn định trên một loại CPU.
**Bài học:** Số đo phụ thuộc phần cứng không nên là mốc chốt pass hoặc fail; hãy đo đối chứng trong cùng một lần chạy.
**Artefact:** Bảng 0,735 và 0,728 cạnh nhau, không kèm tên máy.
