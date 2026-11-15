---
id: 2026-10-31-ba-mat-xich-tu-trang-web-f60d
code: M-X1AC
aliases: [M-X1AC]
date: 2026-10-31
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1891", "claude:f0bf048d#L1984", "claude:f0bf048d#L2284"]
hook: "Từ một trang web độc đến quyền root chỉ cách ba mắt xích"
tension: nho_ma_to
sides: ["Ba cấu hình có vẻ vô hại", "Nối lại thành đường tới quyền root"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm đang dựng hệ agent cho team marketing trên Multica, gồm agent SEO, GA4 và phân tích số liệu, và muốn agent tự làm nhiều việc mà không làm hỏng dữ liệu. Khi rà quyền, người làm đánh dấu mã đăng nhập dev 6 ký tự còn nằm trong cấu hình là lỗ khẩn cấp, vì nghĩ nó vẫn có thể mở cửa vào máy. Kiểm lại thì phiên làm song song đã xoá mã đó từ trước. Ai dựng hệ nhiều agent nên kiểm xem lỗ còn mở hay không trước khi báo động."
audience: dev dựng hệ nhiều agent và tự động hoá
spine_context: "Team marketing dựng hệ agent trên Multica (agent SEO, GA4, phân tích số liệu) và đang rà quyền để agent chạy trên máy."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1794"]
spine_want: Muốn agent tự làm được nhiều việc mà không gây hậu quả nghiêm trọng hoặc mất dữ liệu.
spine_want_lines: ["claude:f0bf048d#L1794"]
spine_obstacle: "Agent chạy dưới danh tính của chủ máy, nên có đường leo quyền từ trang web độc tới root."
spine_obstacle_lines: ["claude:f0bf048d#L1891"]
spine_turn: "Tưởng mã đăng nhập dev 6 ký tự còn có thể đăng nhập được thành chủ máy; hoá ra commit của phiên song song đã xoá nó từ trước, biến đã trống trong container."
spine_turn_lines: ["claude:f0bf048d#L1891", "claude:f0bf048d#L2284"]
spine_action: "Dừng hai daemon, tạo user agents-opc chỉ là member của hai workspace, rồi kiểm biến mã dev."
spine_action_lines: ["claude:f0bf048d#L1983", "claude:f0bf048d#L2284"]
spine_outcome: "Mã dev đã tắt; đăng nhập bằng email vẫn còn nhưng bị giới hạn thử sai. Giai đoạn 0 xong 3/5 bước; PAT của chủ vẫn còn trong opc-agent, chờ chủ chạy sudo."
spine_outcome_lines: ["claude:f0bf048d#L2284"]
spine_takeaway: "Trước khi báo động một lỗ, kiểm xem nó còn mở không; trong hệ nhiều phiên song song, lỗ có thể đã được vá."
spine_takeaway_lines: ["claude:f0bf048d#L2284"]
completeness: 7
---

# Ba mắt xích từ trang web độc tới quyền root

**Góc kể:** Một người làm đang dựng hệ agent cho team marketing trên Multica, gồm agent SEO, GA4 và phân tích số liệu, và muốn agent tự làm nhiều việc mà không làm hỏng dữ liệu. Khi rà quyền, người làm đánh dấu mã đăng nhập dev 6 ký tự còn nằm trong cấu hình là lỗ khẩn cấp, vì nghĩ nó vẫn có thể mở cửa vào máy. Kiểm lại thì phiên làm song song đã xoá mã đó từ trước. Ai dựng hệ nhiều agent nên kiểm xem lỗ còn mở hay không trước khi báo động.
**Bối cảnh:** Agent SEO đọc web bên ngoài, nên có thể bị chèn lệnh qua nội dung trang.
**Chuyện gì xảy ra:** Chuỗi leo thang gồm ba mắt xích: daemon của agent khách dùng PAT của chủ, agent đó giao được việc cho System Operator, và System Operator chạy dưới user có quyền docker, tương đương root. Trước khi làm gì, kiểm thấy hai daemon đều rảnh, không có task. Dừng cả hai, tạo user agents-opc chỉ là member của các workspace khách, rồi thu hồi PAT cũ. Đóng được mắt xích đầu tiên, còn mắt xích thứ ba phải đợi tách user riêng.
**Bài học:** Mỗi daemon chạy agent phải dùng danh tính không có quyền quản trị. Cắt quyền bằng cách đổi danh tính, không bằng lời dặn trong instructions.
**Artefact:** Sơ đồ ba mắt xích, không ghi token hay đường dẫn home.
