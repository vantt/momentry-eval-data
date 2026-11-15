---
id: 2026-11-06-truoc-khi-de-xuat-dia-diem-f922
code: M-KTDT
aliases: [M-KTDT]
date: 2026-11-06
repo: repo
status: raw
signals: []
source: "chat Claude, claude:5a1e7c06"
sessions: ["claude:5a1e7c06"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:5a1e7c06#L12", "claude:5a1e7c06#L13"]
hook: "AI hỏi đúng một con số: ngân sách dự phòng có vượt 22 triệu không"
tension: it_ma_nhieu
sides: ["Có thể khuyến nghị ngay dựa trên giả định", "Một con số quyết định loại hẳn phương án nên phải hỏi trước"]
strength: 2
stakes: 2
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một nhóm đang chuẩn bị đêm nhạc Gió Mùa vào 15/11 và đã bán 300 vé. Người làm tin rằng sân thượng Lầu Bảy vẫn tổ chức được, nhưng đội phòng cháy kiểm tra và đình chỉ sân thượng ít nhất một tháng. Đáng để quan tâm vì vé đã bán nên mỗi lựa chọn thay thế đều có giá: Kho Gạo chỉ chứa 220 chỗ, còn 80 vé phải xử lý."
audience: người tổ chức sự kiện nhỏ tự lo địa điểm
spine_context: "Một nhóm đang chuẩn bị đêm nhạc Gió Mùa vào 15/11, đã bán 300 vé."
spine_context_lines: ["claude:5a1e7c06#L1", "claude:5a1e7c06#L9"]
spine_want: Giữ được đêm nhạc đúng ngày 15/11 cho 300 khán giả đã mua vé.
spine_want_lines: ["claude:5a1e7c06#L1", "claude:5a1e7c06#L9"]
spine_obstacle: "Sân thượng Lầu Bảy bị đội phòng cháy đình chỉ, ít nhất một tháng, đúng lúc phải trả lời trước 17h."
spine_obstacle_lines: ["claude:5a1e7c06#L9"]
spine_turn: Tưởng sân thượng Lầu Bảy dùng được cho 15/11; hoá ra bị đình chỉ ít nhất một tháng sau kiểm tra PCCC.
spine_turn_lines: ["claude:5a1e7c06#L9"]
spine_action: "So hai địa điểm thay thế rồi chọn Kho Gạo (220 chỗ, 15 triệu) thay vì NVH Thanh Niên (350 chỗ, 37 triệu kèm sân khấu)."
spine_action_lines: ["claude:5a1e7c06#L11", "claude:5a1e7c06#L12", "claude:5a1e7c06#L15"]
spine_outcome: "Chốt Kho Gạo; 80 vé vượt sức chứa cần xử lý bằng hoàn tiền tự nguyện, hạn trả lời 48 tiếng."
spine_outcome_lines: ["claude:5a1e7c06#L14", "claude:5a1e7c06#L15"]
spine_takeaway: "Trước khi bán vé, xác nhận địa điểm còn giấy phép và không nằm trong diện kiểm tra, vì một lần đình chỉ có thể lấy mất cả buổi diễn."
spine_takeaway_lines: ["claude:5a1e7c06#L9"]
completeness: 7
---

# Trước khi đề xuất địa điểm, agent hỏi một con số quyết định (ngân sách dự phòng còn bao nhiêu) và nói rõ ngưỡng 22 triệu sẽ loại phương án nào.

**Góc kể:** Một nhóm đang chuẩn bị đêm nhạc Gió Mùa vào 15/11 và đã bán 300 vé. Người làm tin rằng sân thượng Lầu Bảy vẫn tổ chức được, nhưng đội phòng cháy kiểm tra và đình chỉ sân thượng ít nhất một tháng. Đáng để quan tâm vì vé đã bán nên mỗi lựa chọn thay thế đều có giá: Kho Gạo chỉ chứa 220 chỗ, còn 80 vé phải xử lý.
**Chuyện gì xảy ra:** Trước khi đề xuất địa điểm, agent hỏi một con số quyết định (ngân sách dự phòng còn bao nhiêu) và nói rõ ngưỡng 22 triệu sẽ loại phương án nào.
**Góc người ngoài:** cách làm phổ biến là Đưa ra khuyến nghị ngay dựa trên giả định, hoặc liệt kê ưu nhược điểm rồi để người dùng tự chọn; ở đây khác ở Agent chỉ ra đúng biến số làm đảo ngược quyết định và hỏi đúng biến số đó. User trả lời một câu là có đáp án, không cần đọc lại cả bảng so sánh.
