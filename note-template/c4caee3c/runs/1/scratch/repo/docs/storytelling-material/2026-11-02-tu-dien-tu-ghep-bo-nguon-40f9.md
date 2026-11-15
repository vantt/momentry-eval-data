---
id: 2026-11-02-tu-dien-tu-ghep-bo-nguon-40f9
code: M-A7B4
aliases: [M-A7B4]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2155", "claude:c4caee3c#L2862", "claude:c4caee3c#L2875"]
hook: "Bỏ nguồn không rõ, học lại 20.523 từ từ dữ liệu CC BY"
tension: it_ma_nhieu
sides: ["Bỏ danh sách nguồn không rõ giấy phép", "Làm lại bằng dữ liệu sạch, vi-compound 0,632 lên 0,983"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Từ điển từ ghép: bỏ nguồn không rõ, học lại từ dữ liệu CC BY

**Bối cảnh:** Từ điển từ ghép ban đầu lấy từ một danh sách trên GitHub có giấy phép MIT, nhưng nguồn gốc của danh sách không được ghi rõ và phần lớn trùng với một bộ từ điển GPL.
**Chuyện gì xảy ra:** Chủ dự án yêu cầu danh sách mới phải học bằng thống kê từ corpus có giấy phép rõ ràng, còn pyvi chỉ dùng để chọn tham số. Agent học 20.523 từ từ ba bộ CC BY 4.0, đọc giấy phép từng bộ trên trang gốc. Danh sách mới bằng hoặc tốt hơn ở mọi hạng mục. vi-compound trên bộ khó tăng từ 0,632 lên 0,983. Script dựng lại tạo ra file giống hệt từng byte.
**Bài học:** Đừng bundle dữ liệu nếu nguồn gốc chưa rõ. Ghi giấy phép và cách tạo dữ liệu, và giữ script để tái tạo.
**Artefact:** File ghi nguồn và giấy phép của từng bộ dữ liệu (không có nội dung).
