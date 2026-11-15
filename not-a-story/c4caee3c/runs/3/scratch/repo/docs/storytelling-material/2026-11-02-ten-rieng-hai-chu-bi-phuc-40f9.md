---
id: 2026-11-02-ten-rieng-hai-chu-bi-phuc-40f9
code: M-MKN7
aliases: [M-MKN7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2733", "claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842"]
hook: "Tên riêng hai chữ bị phục hồi thành từ thường"
tension: giup_ma_hai
sides: ["Phục hồi dấu để tìm kiếm tốt hơn", "Tên riêng bị đổi thành từ thường, nDCG@5 tụt"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tên riêng hai chữ bị phục hồi dấu thành từ thường, kéo nDCG@5 xuống

**Bối cảnh:** Khi bật restoreForEmbedding, một câu có một chữ có dấu trên hai chữ được coi là chưa có dấu, nên chữ không dấu bị phục hồi theo từ phổ biến hơn trong vault.
**Chuyện gì xảy ra:** Model eval phát hiện một tên riêng hai chữ bị đổi sang từ thường. Ngưỡng 50% của PRD không sai, lỗi nằm ở cách dựng câu gửi cho embedder. Agent viết test thất bại trên mã cũ trước, rồi sửa để chỉ phục hồi chữ không dấu khi vault không bao giờ viết nó trần và độ tin cậy đủ. nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, và tuỳ chọn được bật mặc định.
**Bài học:** Đừng sửa ngưỡng khi lỗi nằm ở chỗ dựng đầu vào. Viết test chứng minh lỗi trước khi sửa.
**Artefact:** Bảng nDCG@5 trước và sau cho hạng mục liên quan.
