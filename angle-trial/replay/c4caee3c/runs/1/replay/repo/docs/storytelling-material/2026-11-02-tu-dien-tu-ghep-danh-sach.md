---
id: 2026-11-02-tu-dien-tu-ghep-danh-sach
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do, số trước sau, ràng buộc định hình thiết kế]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1685", "claude:c4caee3c#L2155", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Danh sách từ ghép MIT có thể mang nguồn GPL, nên đổi sang dữ liệu CC BY"
tension: tuong_ma_hoa_ra
sides: ["Danh sách giấy phép MIT trông an toàn", "Nguồn gốc có thể là GPL; học lại từ CC BY còn tốt hơn, 0,632 lên 0,983"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Ai dùng danh sách từ ghép trong một repo MIT đều nghĩ dữ liệu đó đã sạch giấy phép. Hoá ra khoảng 95% danh sách trùng với bộ Viet74K mang giấy phép GPL, nên giấy phép của bản chép không nói được nguồn gốc thật. Agent đã học lại danh sách từ dữ liệu CC BY, không chép mục nào, và kết quả vẫn tốt hơn: 0,983 so với 0,632 của bản gốc. Với ai làm dữ liệu mở, nên kiểm nguồn gốc chứ không chỉ đọc file giấy phép."
audience: dev làm dữ liệu hoặc thư viện mở cho tiếng Việt
---

# Từ điển từ ghép: danh sách MIT có thể mang nguồn GPL, đổi sang thống kê dữ liệu CC BY

**Góc kể:** Ai dùng danh sách từ ghép trong một repo MIT đều nghĩ dữ liệu đó đã sạch giấy phép. Hoá ra khoảng 95% danh sách trùng với bộ Viet74K mang giấy phép GPL, nên giấy phép của bản chép không nói được nguồn gốc thật. Agent đã học lại danh sách từ dữ liệu CC BY, không chép mục nào, và kết quả vẫn tốt hơn: 0,983 so với 0,632 của bản gốc. Với ai làm dữ liệu mở, nên kiểm nguồn gốc chứ không chỉ đọc file giấy phép.
**Bối cảnh:** Danh sách 22.574 từ ghép lấy từ một repo MIT, nhưng agent ước lượng phần lớn trùng với một danh sách GPL. Giấy phép của bản chép không phản ánh nguồn gốc.
**Chuyện gì xảy ra:** Agent đọc giấy phép từng nguồn, chọn ba bộ dữ liệu CC BY 4.0 và học bằng thống kê cặp âm tiết, ra 20.523 từ. Không chép mục nào từ danh sách cũ, chỉ dùng nó để chọn ngưỡng. vi-compound trên fixture khó tăng từ 0,632 lên 0,983, tốt hơn hoặc bằng danh sách cũ ở mọi hạng mục. Nguồn được ghi trong file ATTRIBUTION.
**Bài học:** Kiểm nguồn gốc dữ liệu chứ không chỉ giấy phép của bản chép; một danh sách MIT có thể mang nguồn GPL.
**Artefact:** Bảng so vi-compound giữa các phiên bản từ điển.
