---
id: 2026-11-02-loi-ux-tu-chinh-cong-cu-c4b4
code: M-SQRC
aliases: [M-SQRC]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, nguoi_duyet_may_soan, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["claude:6a207191#L1074", "claude:6a207191#L1084", "claude:6a207191#L1102", "claude:6a207191#L1441", "claude:6a207191#L1489", "claude:6a207191#L1501", "claude:6a207191#L1507", "claude:6a207191#L1515"]
hook: "Gửi bản mới lên hub, trang vẫn hiện bản cũ là 'active'"
tension: tuong_ma_hoa_ra
sides: ["Gửi xong tưởng trang đã hiện bản mới", "Trang vẫn hiện bản cũ, không báo có bản chờ duyệt, ba bản gửi nằm chung hàng chờ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang viết skill hướng dẫn đóng gói và phân phối công cụ CLI, rồi đưa lên hub skillstation để agent dùng lại. Sau khi gửi bản mới, họ tưởng bản đang chạy sẽ giữ nguyên cho tới khi duyệt, nhưng trang skill vẫn hiện bản cũ là 'active' và không báo có bản chờ duyệt. Hoá ra bản active là bản đã duyệt từ trước, còn bản mới nằm riêng trong 'Waiting for review' mà trang không nhắc tới. Ai dùng quy trình gửi rồi duyệt nên kiểm tra trạng thái thật sau mỗi lần gửi, đừng chỉ tin trang đang hiện."
audience: dev dùng agent để đưa skill lên hub nội bộ
spine_context: "Người làm đang viết skill hướng dẫn đóng gói, cài đặt, cập nhật và cấu hình cho các công cụ CLI, rồi đưa lên hub skillstation để agent dùng lại."
spine_context_lines: ["claude:6a207191#L5", "claude:6a207191#L967"]
spine_want: Gửi bản mới lên hub và duyệt để agent dùng được bản đó.
spine_want_lines: ["claude:6a207191#L967", "claude:6a207191#L1489"]
spine_obstacle: "Gửi bản mới xong, trang skill vẫn hiện bản cũ là 'active' và không báo có bản đang chờ duyệt."
spine_obstacle_lines: ["claude:6a207191#L1489", "claude:6a207191#L1507"]
spine_turn: "Tưởng bản gửi chưa duyệt thì hub không được đổi trạng thái; hoá ra bản active là bản đã duyệt từ lần trước, còn bản mới nằm riêng ở 'Waiting for review' mà trang skill không nhắc tới."
spine_turn_lines: ["claude:6a207191#L1489", "claude:6a207191#L1503"]
spine_action: "Đối chiếu bản trên hub với thư mục skill trên máy, xác nhận nội dung giống nhau và routing trên hub là bản đã duyệt trước đó; sau đó đề xuất sửa skillstation để hiện bản chờ duyệt."
spine_action_lines: ["claude:6a207191#L1500", "claude:6a207191#L1503", "claude:6a207191#L1515"]
spine_outcome: Bản mới vẫn đang chờ duyệt; việc sửa giao diện để báo bản chờ duyệt được chuyển cho một skill frontend.
spine_outcome_lines: ["claude:6a207191#L1515", "claude:6a207191#L1525"]
spine_takeaway: "Sau mỗi thao tác gửi hay duyệt, kiểm tra trạng thái thật trên hub thay vì tin trang đang hiện; trang phải tự cho biết khi có bản chờ duyệt."
spine_takeaway_lines: ["claude:6a207191#L1515"]
completeness: 7
---

# Lỗi UX từ chính công cụ của mình: gợi ý cờ --user không tồn tại, và hub 'active' không phải bản vừa gửi

**Góc kể:** Người làm đang viết skill hướng dẫn đóng gói và phân phối công cụ CLI, rồi đưa lên hub skillstation để agent dùng lại. Sau khi gửi bản mới, họ tưởng bản đang chạy sẽ giữ nguyên cho tới khi duyệt, nhưng trang skill vẫn hiện bản cũ là 'active' và không báo có bản chờ duyệt. Hoá ra bản active là bản đã duyệt từ trước, còn bản mới nằm riêng trong 'Waiting for review' mà trang không nhắc tới. Ai dùng quy trình gửi rồi duyệt nên kiểm tra trạng thái thật sau mỗi lần gửi, đừng chỉ tin trang đang hiện.
**Bối cảnh:** Chủ dùng skillstation để đưa skill lên hub từ xa. Agent gặp hàng loạt trục trặc khi gửi và duyệt.
**Chuyện gì xảy ra:** Thông báo lỗi gợi ý cờ --user, nhưng connect không có cờ đó (skillstation 0.8.0 trên máy, hub 0.12.0). Sau khi kết nối toàn cục và đẩy bản gửi, trang skill vẫn hiện bản cũ là 'active' mà không báo có bản chờ duyệt. Ba bản gửi cùng một skill cùng nằm trong hàng chờ. Agent đã viết một thay đổi UI cho trang chi tiết và danh sách skill (229 test web qua), merge và push lên main, CI xanh.
**Bài học:** Thông báo lỗi và trạng thái 'đang dùng' phải nói rõ có bản đang chờ. Nếu không, người duyệt sẽ duyệt nhầm bản cũ.
**Artefact:** Ảnh chụp trang skill có dải 'An update to this skill is waiting for review' (che SUB-id và địa chỉ hub).
**Góc người ngoài:** cách làm phổ biến là Dev thường hoặc làm theo gợi ý của công cụ, hoặc dừng lại hỏi người khác; ít ai tự đối chiếu trạng thái thật trên đĩa sau mỗi thao tác cấu hình; ở đây khác ở Agent không đoán 'chắc đã xong', mà đo lại bằng bằng chứng (grep file, so phiên bản, chạy doctor) và báo rõ phần nào đã có, phần nào chưa. Người đọc sẽ muốn biết vì sao cách này tránh được lỗi 'tưởng đã kết nối'.
