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
hook: "Agent khách giữ khóa của chủ, giao việc cho tay gần như root"
tension: nho_ma_to
sides: ["Daemon khách chỉ làm việc nhỏ bằng khóa của chủ", "Khóa đó giao được việc cho agent có quyền gần như root"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một dự án điều phối agent AI cho team marketing muốn cho agent tự làm nhiều việc trên máy mà không gây hậu quả nghiêm trọng hay mất dữ liệu. Người làm tưởng token của chủ không nằm trên máy, nhưng bản phản biện cho thấy daemon của agent khách đăng nhập bằng đúng token đó, nên agent có thể giao việc cho tác vụ gần như root. Đáng nghe vì lời dặn trong prompt không đủ để chặn agent, vì nội dung web có thể ghi đè lời dặn đó; phải chặn bằng quyền hệ điều hành và danh tính riêng."
audience: dev dùng agent AI có quyền trên máy thật
spine_context: "Dự án điều phối agent AI cho team marketing, muốn agent tự làm SEO, GA4 và đọc số liệu trên máy."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L1794"]
spine_want: Cấp quyền để agent tự làm nhiều việc nhất mà không gây hậu quả nghiêm trọng hay mất dữ liệu.
spine_want_lines: ["claude:f0bf048d#L1794"]
spine_obstacle: "Agent đọc nội dung web có thể bị chèn lệnh, và bản phản biện thấy có đường leo từ agent lên quyền gần root."
spine_obstacle_lines: ["claude:f0bf048d#L1867", "claude:f0bf048d#L1891"]
spine_turn: "Tưởng token của chủ không nằm trên máy; hoá ra daemon của agent khách đăng nhập bằng đúng token đó, nên agent giao việc được cho tác vụ có quyền docker."
spine_turn_lines: ["claude:f0bf048d#L1867", "claude:f0bf048d#L1891"]
spine_action: "Viết tài liệu thiết kế quyền, nhờ agent khác phản biện, rồi sửa thành v2; chưa đụng vào máy."
spine_action_lines: ["claude:f0bf048d#L1884", "claude:f0bf048d#L1891"]
spine_outcome: "Tài liệu v2 chưa commit, trên máy chưa có thay đổi; đã nêu ba lỗ khẩn cấp và thứ tự xử lý từ giai đoạn 0 đến 4."
spine_outcome_lines: ["claude:f0bf048d#L1891"]
spine_takeaway: "Đừng để agent chạy bằng token của chủ; chặn bằng quyền hệ điều hành thay vì tin lời dặn trong prompt, vì nội dung web có thể ghi đè lời dặn đó."
spine_takeaway_lines: ["claude:f0bf048d#L1891"]
completeness: 7
---

# Chuỗi leo thang: agent khách giữ PAT chủ, giao việc cho System Operator có docker

**Góc kể:** Một dự án điều phối agent AI cho team marketing muốn cho agent tự làm nhiều việc trên máy mà không gây hậu quả nghiêm trọng hay mất dữ liệu. Người làm tưởng token của chủ không nằm trên máy, nhưng bản phản biện cho thấy daemon của agent khách đăng nhập bằng đúng token đó, nên agent có thể giao việc cho tác vụ gần như root. Đáng nghe vì lời dặn trong prompt không đủ để chặn agent, vì nội dung web có thể ghi đè lời dặn đó; phải chặn bằng quyền hệ điều hành và danh tính riêng.
**Bối cảnh:** Bản phản biện chỉ ra cách một agent bị điều khiển có thể đi tới quyền root trên máy.
**Chuyện gì xảy ra:** Daemon của agent khách đăng nhập bằng PAT của chủ, nên agent có thể giao việc cho System Operator. System Operator chạy dưới user có nhóm docker, tức gần như root. Daemon spike cũng chạy agent khác dưới cùng user. Thứ tự xử lý: dừng daemon đang rảnh, tắt mã dev, đổi daemon sang danh tính riêng, thu hồi PAT chủ.
**Bài học:** Đừng để agent chạy bằng token của chủ. Một chuỗi từ agent tới đặc quyền thường nằm ở một chỗ không ai nghi.
**Artefact:** Sơ đồ chuỗi leo thang dạng văn bản.
**Góc người ngoài:** cách làm phổ biến là Thường dặn agent trong prompt là đừng làm việc nguy hiểm, và dùng chung một token admin cho mọi tiến trình tự động; ở đây khác ở Phiên này coi lời dặn không đáng tin khi có prompt injection, nên cắt đường leo quyền bằng quyền hệ điều hành, danh tính Multica và không quyền ghi. Người đọc cần biết vì sao làm như vậy và cái giá là phải kéo bản vá về bằng tay.
