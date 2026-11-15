---
id: 2026-11-02-tu-dien-tu-ghep-va-tach
date: 2026-11-02
repo: repo
status: raw
signals: [Ràng buộc định hình thiết kế, Đảo quyết định có lý do, "Số trước, số sau"]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1637", "claude:c4caee3c#L1672", "claude:c4caee3c#L2851", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Thay danh sách từ cũ bằng 20.523 từ tự học, điểm vẫn vọt"
tension: it_ma_nhieu
sides: ["không chép mục nào từ danh sách cũ", "vi-compound từ 0,632 lên 0,983"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép và tách từ: từ danh sách GPL sang thống kê CC BY

**Bối cảnh:** Từ điển cặp âm tiết ban đầu lấy từ một repo MIT nhưng repo không ghi nguồn gốc danh sách. Kiểm tra cho thấy khoảng 95 phần trăm trùng với một danh sách GPL.
**Chuyện gì xảy ra:** Tách từ bằng view seg đưa nDCG@5 từ 0,909 lên 0,932, và trên bộ câu từ ghép khó từ 0,79 lên 0,86. Sau đó agent học lại từ thống kê cặp âm tiết trên ba bộ dữ liệu CC BY 4.0, được 20.523 từ, không chép mục nào từ danh sách cũ. Trên bộ câu từ ghép khó, vi-compound tăng từ 0,632 lên 0,983.
**Bài học:** Giấy phép của dữ liệu đi kèm gói phải được kiểm từng nguồn, không tin nhãn của repo.
**Artefact:** Bảng nguồn dữ liệu và giấy phép, không có mục từ nào.
