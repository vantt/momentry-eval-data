---
id: 2026-10-21-ba-agent-song-song-cho-thay-fd46
code: M-81B9
aliases: [M-81B9]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L1448", "claude:9514b261#L1476", "claude:9514b261#L1482", "claude:9514b261#L1511", "claude:9514b261#L1572"]
hook: "332 trong 479 tài liệu nằm ở trạng thái tạm suốt 50 ngày, cảnh báo không bao giờ bắn"
tension: cam_ma_van_lot
sides: ["Có cảnh báo cho tài liệu để tạm quá lâu", "Code trừ chuỗi ngày ra NaN nên cảnh báo không bao giờ bắn"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là nền tảng để xây ứng dụng agent, và người làm đang dò xem đề xuất hệ thống tài liệu mới có trùng với Knowledge Registry đã có không. Cảnh báo tài liệu tạm quá lâu được tin là vẫn chạy, nhưng nó không bao giờ bắn: phép trừ ngày trên chuỗi ISO ra NaN, nên 332 trong 479 doc đã tạm khoảng 50 ngày mà không ai hay. Ai xây cảnh báo nên thử nó bằng một đầu vào biết trước là vi phạm, không chỉ tin nó đang chạy."
audience: dev xây cảnh báo hoặc kiểm tra tự động cho hệ thống tài liệu
spine_context: Forgent (fgOS) là nền tảng để xây ứng dụng agent; người làm đang dò xem đề xuất hệ thống tài liệu mới có trùng với Knowledge Registry đã có không.
spine_context_lines: [profile, "claude:9514b261#L1325"]
spine_want: Muốn biết cần xây mới Knowledge and Documentation Engine hay chỉ hoàn thiện Knowledge Registry có sẵn.
spine_want_lines: ["claude:9514b261#L1325", "claude:9514b261#L1572"]
spine_obstacle: "Knowledge Registry đã chạy nhưng dừng: không có sự kiện doc nào sau 2026-09-11."
spine_obstacle_lines: ["claude:9514b261#L1467"]
spine_turn: "Tưởng cảnh báo tài liệu tạm quá lâu vẫn đang bắt lỗi; hoá ra nó không bao giờ bắn, vì phép trừ ngày trên chuỗi ISO ra NaN."
spine_turn_lines: ["claude:9514b261#L1467", "claude:9514b261#L1572"]
spine_action: "Đọc lại code của cảnh báo và dữ liệu registry, xác nhận lỗi, rồi gộp ba báo cáo thành một bản tổng hợp."
spine_action_lines: ["claude:9514b261#L1476", "claude:9514b261#L1523"]
spine_outcome: "Lỗi được xác nhận: 332 doc vẫn tạm, khoảng 47–55 ngày mà không ai phát hiện; bản tổng hợp đã viết."
spine_outcome_lines: ["claude:9514b261#L1572"]
spine_takeaway: Cảnh báo so sánh sai kiểu dữ liệu có thể tắt im lặng; hãy thử cảnh báo bằng một đầu vào biết trước là vi phạm.
spine_takeaway_lines: ["claude:9514b261#L1572"]
completeness: 7
---

# Ba agent song song cho thấy thứ 'đề xuất mới' đã chạy thật: Knowledge Registry có 479 doc, 332 cái vẫn provisional

**Góc kể:** Forgent (fgOS) là nền tảng để xây ứng dụng agent, và người làm đang dò xem đề xuất hệ thống tài liệu mới có trùng với Knowledge Registry đã có không. Cảnh báo tài liệu tạm quá lâu được tin là vẫn chạy, nhưng nó không bao giờ bắn: phép trừ ngày trên chuỗi ISO ra NaN, nên 332 trong 479 doc đã tạm khoảng 50 ngày mà không ai hay. Ai xây cảnh báo nên thử nó bằng một đầu vào biết trước là vi phạm, không chỉ tin nó đang chạy.
**Bối cảnh:** Proposal của hệ thống tài liệu mô tả một Knowledge and Documentation Engine mới. Owner nghi trùng với cái đã có, nên agent chạy ba researcher quét plans, history và code.
**Chuyện gì xảy ra:** Knowledge Registry đã chạy, phủ 479 doc (khoảng 15% trong 3146 file .md). 332 doc đang provisional, 147 active. Cảnh báo doc-provisional-aged không bao giờ bắn: code trừ updatedAt là chuỗi ISO nên ra NaN. Từ đó 332 doc đã provisional khoảng 47–55 ngày mà không ai biết. Phần thật sự mới của engine chỉ còn sáu thứ chưa có mã.
**Bài học:** Một cảnh báo viết sai kiểu dữ liệu (chuỗi thay vì số) có thể tắt im lặng cả cơ chế cảnh báo; kiểm cảnh báo bằng cách cho nó một đầu vào biết trước là vi phạm.
**Artefact:** Bảng số: 479 doc, 332 provisional, 147 active, 365 role khác nhau, 3146 file .md. Không có chuỗi dữ liệu nhạy cảm.
