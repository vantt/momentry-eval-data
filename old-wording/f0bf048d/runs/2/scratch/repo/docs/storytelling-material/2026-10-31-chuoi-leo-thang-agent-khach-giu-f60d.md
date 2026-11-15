---
id: 2026-10-31-chuoi-leo-thang-agent-khach-giu-f60d
code: M-GNK7
aliases: [M-GNK7]
date: 2026-10-31
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1874", "claude:f0bf048d#L1891"]
hook: "Agent khách cầm PAT của chủ, giao việc cho user có docker gần như root"
tension: cam_ma_van_lot
sides: ["agent khách chỉ được làm việc khách", "PAT chủ cho nó sai user gần như root"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm dự án multica, cho team marketing có agent làm SEO, GA4 và đọc số liệu, đang thiết kế quyền để agent tự làm nhiều mà không mất dữ liệu. Bản nháp giả định PAT không nằm trên máy, nhưng phản biện chỉ ra opc-agent đang dùng PAT của chủ: một agent bị chèn lệnh từ trang web có thể giao việc cho System Operator chạy gần root. Đây là lý do nên chặn bằng quyền hệ điều hành thay vì chỉ dặn trong prompt."
audience: "dev dùng AI agent tự động hoá, quan tâm đến an toàn quyền hạn"
spine_context: "Một người làm dự án multica, cho team marketing có agent làm SEO, GA4 và đọc số liệu, đang thiết kế quyền để agent tự làm được nhiều việc."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1794"]
spine_want: Muốn agent tự làm nhiều nhất có thể mà không gây hậu quả nghiêm trọng và không mất dữ liệu.
spine_want_lines: ["claude:f0bf048d#L1794"]
spine_obstacle: Phản biện chỉ ra một agent bị chèn lệnh qua trang web có thể đi lên tới quyền root trên máy.
spine_obstacle_lines: ["claude:f0bf048d#L1867", "claude:f0bf048d#L1891"]
spine_turn: "Bản nháp giả định PAT không nằm trên máy; hoá ra opc-agent đang dùng PAT của chủ, nên agent có thể giao việc cho System Operator chạy gần root."
spine_turn_lines: ["claude:f0bf048d#L1867", "claude:f0bf048d#L1891"]
spine_action: "Viết bản nháp thiết kế quyền, nhờ một agent độc lập phản biện, rồi sửa thành bản v2."
spine_action_lines: ["claude:f0bf048d#L1861", "claude:f0bf048d#L1884", "claude:f0bf048d#L1891"]
spine_outcome: Trên máy chưa thay đổi gì; tài liệu chưa commit; có ba lỗ khẩn cấp và thứ tự xử lý theo giai đoạn.
spine_outcome_lines: ["claude:f0bf048d#L1891"]
spine_takeaway: Lời dặn trong prompt không phải ranh giới bảo mật; chặn bằng quyền hệ điều hành và danh tính riêng cho agent.
spine_takeaway_lines: ["claude:f0bf048d#L1891"]
completeness: 7
---

# Chuỗi leo thang: agent khách giữ PAT chủ, giao việc cho System Operator có docker

**Góc kể:** Một người làm dự án multica, cho team marketing có agent làm SEO, GA4 và đọc số liệu, đang thiết kế quyền để agent tự làm nhiều mà không mất dữ liệu. Bản nháp giả định PAT không nằm trên máy, nhưng phản biện chỉ ra opc-agent đang dùng PAT của chủ: một agent bị chèn lệnh từ trang web có thể giao việc cho System Operator chạy gần root. Đây là lý do nên chặn bằng quyền hệ điều hành thay vì chỉ dặn trong prompt.
**Bối cảnh:** Bản phản biện chỉ ra cách một agent bị điều khiển có thể đi tới quyền root trên máy.
**Chuyện gì xảy ra:** Daemon của agent khách đăng nhập bằng PAT của chủ, nên agent có thể giao việc cho System Operator. System Operator chạy dưới user có nhóm docker, tức gần như root. Daemon spike cũng chạy agent khác dưới cùng user. Thứ tự xử lý: dừng daemon đang rảnh, tắt mã dev, đổi daemon sang danh tính riêng, thu hồi PAT chủ.
**Bài học:** Đừng để agent chạy bằng token của chủ. Một chuỗi từ agent tới đặc quyền thường nằm ở một chỗ không ai nghi.
**Artefact:** Sơ đồ chuỗi leo thang dạng văn bản.
**Góc người ngoài:** cách làm phổ biến là Thường dặn agent trong prompt là đừng làm việc nguy hiểm, và dùng chung một token admin cho mọi tiến trình tự động; ở đây khác ở Phiên này coi lời dặn không đáng tin khi có prompt injection, nên cắt đường leo quyền bằng quyền hệ điều hành, danh tính Multica và không quyền ghi. Người đọc cần biết vì sao làm như vậy và cái giá là phải kéo bản vá về bằng tay.
