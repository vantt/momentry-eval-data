---
id: 2026-11-02-tu-dien-tu-ghep-danh-sach-40f9
code: M-MHZ7
aliases: [M-MHZ7]
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1685", "claude:c4caee3c#L2155", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Danh sách MIT có thể mang nguồn GPL, nên học lại từ dữ liệu CC BY"
tension: nho_ma_to
sides: ["danh sách ghi giấy phép MIT, trông an toàn", "nguồn gốc có thể GPL, phải làm lại 20.523 từ"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép: danh sách MIT có thể mang nguồn GPL, đổi sang thống kê dữ liệu CC BY

**Bối cảnh:** Danh sách 22.574 từ ghép lấy từ một repo MIT, nhưng agent ước lượng phần lớn trùng với một danh sách GPL. Giấy phép của bản chép không phản ánh nguồn gốc.
**Chuyện gì xảy ra:** Agent đọc giấy phép từng nguồn, chọn ba bộ dữ liệu CC BY 4.0 và học bằng thống kê cặp âm tiết, ra 20.523 từ. Không chép mục nào từ danh sách cũ, chỉ dùng nó để chọn ngưỡng. vi-compound trên fixture khó tăng từ 0,632 lên 0,983, tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục. Nguồn được ghi trong file ATTRIBUTION.
**Bài học:** Kiểm nguồn gốc dữ liệu chứ không chỉ giấy phép của bản chép; một danh sách MIT có thể mang nguồn GPL.
**Artefact:** Bảng so vi-compound giữa các phiên bản từ điển.
