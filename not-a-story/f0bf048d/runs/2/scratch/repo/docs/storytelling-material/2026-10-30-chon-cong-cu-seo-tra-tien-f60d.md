---
id: 2026-10-30-chon-cong-cu-seo-tra-tien-f60d
code: M-7WY5
aliases: [M-7WY5]
date: 2026-10-30
repo: repo
status: raw
signals: [so_truoc_so_sau, dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1373", "claude:f0bf048d#L1388", "claude:f0bf048d#L1414", "claude:f0bf048d#L1439", "claude:f0bf048d#L1460"]
hook: "Nạp $50 cho DataForSEO, mỗi khách chỉ tốn $2-5"
tension: chon_mot_mat_mot
sides: ["Serper rẻ hơn nhưng chỉ có kết quả Google, không có search volume", "DataForSEO nạp tối thiểu $50 nhưng đủ dữ liệu, bỏ serper"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng bộ agent marketing, và bộ SEO cần dữ liệu từ khoá, thứ hạng và backlink. Trợ lý AI ban đầu đề xuất serper.dev vì rẻ, nhưng serper chỉ trả kết quả Google, không có search volume. Khi tính giá từng lượt, DataForSEO hoá ra rẻ hơn serper và có thêm dữ liệu; ước tính $2-5 mỗi khách mỗi tháng là do trợ lý tự tính, không phải số nhà cung cấp. Dev dùng API trả theo lượt nên cần cách tính chi phí này trước khi mua."
audience: "dev dùng AI xây agent marketing, cần chọn API trả theo lượt"
spine_context: "Người làm đang dựng bộ agent marketing cho team, gồm SEO, social, content và ads."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1282"]
spine_want: Muốn bộ SEO bật được từ miễn phí đến trả tiền.
spine_want_lines: ["claude:f0bf048d#L1439"]
spine_obstacle: "Serper rẻ nhưng chỉ trả kết quả Google, không có search volume."
spine_obstacle_lines: ["claude:f0bf048d#L1388"]
spine_turn: "Tưởng serper là lựa chọn SERP rẻ và đủ dùng; hoá ra DataForSEO rẻ hơn mỗi lượt và có thêm search volume, backlink, crawl."
spine_turn_lines: ["claude:f0bf048d#L1388", "claude:f0bf048d#L1414"]
spine_action: "Kiểm giá DataForSEO trên trang giá, tự ước tính lượng dùng mỗi khách, rồi đổi đề xuất sang chỉ dùng DataForSEO."
spine_action_lines: ["claude:f0bf048d#L1393", "claude:f0bf048d#L1400", "claude:f0bf048d#L1414"]
spine_outcome: Có bảng giá từng dịch vụ và ước tính khoảng $2-5 mỗi khách mỗi tháng; $50 đủ cho khoảng 10 khách trong vài tháng. User yêu cầu hỗ trợ từ miễn phí đến trả tiền (DataForSEO).
spine_outcome_lines: ["claude:f0bf048d#L1414", "claude:f0bf048d#L1439"]
spine_takeaway: "So công cụ trả theo lượt bằng giá từng đơn vị và lượng dùng thực tế, ghi rõ đó là ước tính tự tính. Một lần đọc trang giá không xác nhận được giá SERP, nên kiểm lại trước khi tin."
spine_takeaway_lines: ["claude:f0bf048d#L1412", "claude:f0bf048d#L1414"]
completeness: 7
---

# Chọn công cụ SEO trả tiền: DataForSEO nạp $50, ước $2-5 mỗi khách

**Góc kể:** Người làm đang dựng bộ agent marketing, và bộ SEO cần dữ liệu từ khoá, thứ hạng và backlink. Trợ lý AI ban đầu đề xuất serper.dev vì rẻ, nhưng serper chỉ trả kết quả Google, không có search volume. Khi tính giá từng lượt, DataForSEO hoá ra rẻ hơn serper và có thêm dữ liệu; ước tính $2-5 mỗi khách mỗi tháng là do trợ lý tự tính, không phải số nhà cung cấp. Dev dùng API trả theo lượt nên cần cách tính chi phí này trước khi mua.
**Bối cảnh:** Bộ SEO cần dữ liệu từ khoá, SERP và backlink. Ban đầu cân nhắc serper.dev, rồi chuyển sang DataForSEO.
**Chuyện gì xảy ra:** Serper rẻ (2.500 lượt miễn phí, sau đó khoảng $1 cho 1.000 lượt) nhưng chỉ trả kết quả Google, không có search volume. DataForSEO nạp tối thiểu $50, không hết hạn, SERP từ $0.0006 mỗi lượt, có MCP chính thức. Agent ước tính $2-5 mỗi khách mỗi tháng, ghi rõ đây là ước tính tự tính. Kết luận: chỉ dùng DataForSEO, bỏ serper. Bộ SEO có hai mức: miễn phí mặc định và add-on trả phí bật theo từng khách.
**Bài học:** So sánh công cụ bằng giá từng đơn vị và lượng dùng thực tế, không chỉ bằng giá gói. Ghi rõ ước tính không phải số của nhà cung cấp.
**Artefact:** Bảng giá từng dịch vụ và bảng ước tính lượng dùng mỗi tháng.
**Góc người ngoài:** cách làm phổ biến là Thường đăng ký gói trả phí theo đề xuất hoặc bật cho tất cả; ở đây khác ở Phiên này ước tính $2-5 mỗi khách mỗi tháng, chỉ bật cho khách có add-on, và plan báo lỗi nếu add-on không có bộ nào cung cấp. Người đọc cần biết cách tính chi phí trước khi mua.
