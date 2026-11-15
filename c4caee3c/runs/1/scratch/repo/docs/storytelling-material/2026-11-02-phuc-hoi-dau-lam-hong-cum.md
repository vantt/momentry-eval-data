---
id: 2026-11-02-phuc-hoi-dau-lam-hong-cum
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, Đảo quyết định có lý do]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842", "claude:c4caee3c#L2919"]
hook: "Phục hồi dấu biến tên riêng thành từ thông dụng hơn"
tension: giup_ma_hai
sides: ["Phục hồi dấu để hiểu câu tốt hơn", "Tên riêng bị đổi thành từ phổ biến"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phục hồi dấu làm hỏng cụm có tên riêng: âm tiết không dấu đổi sang từ phổ biến

**Bối cảnh:** Khi câu truy vấn có một phần âm tiết có dấu, các âm tiết không dấu được phục hồi dấu theo từ phổ biến hơn trong vault.
**Chuyện gì xảy ra:** Một cụm tên riêng hai âm tiết, một có dấu, bị phục hồi âm tiết còn lại thành từ thường gặp hơn. Ngưỡng 50 phần trăm đúng theo PRD nên giữ nguyên. Agent sửa cách ghép câu gửi model nhúng: từ đã gõ có dấu không bao giờ đổi, và chỉ phục hồi khi vault không bao giờ viết từ đó trần và xác suất đủ cao. Sau sửa, bật nhánh nghĩa mặc định làm nDCG@5 tổng từ 0,932 lên 0,954, vi-snippet đạt 15/15.
**Bài học:** Lỗi thường nằm ở cách ghép đầu vào chứ không nằm ở ngưỡng đã đúng.
**Artefact:** Bảng so sánh tắt và bật tuỳ chọn theo hạng mục.
