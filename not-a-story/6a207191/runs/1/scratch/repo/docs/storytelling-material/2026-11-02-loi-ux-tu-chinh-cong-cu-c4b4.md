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
hook: "Công cụ gợi ý cờ --user, nhưng cờ đó không hề tồn tại"
tension: giup_ma_hai
sides: ["Thông báo lỗi sinh ra để chỉ đường cho người dùng", "Nó chỉ tới một cờ không có, và hub vẫn hiện bản cũ là 'active'"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm bộ hướng dẫn đóng gói và phân phối cho các dự án CLI, đóng thành skill để agent dùng, rồi đưa lên hub skillstation. Họ tin rằng bản mới chỉ thay bản đang chạy sau khi bấm duyệt, nhưng trang skill vẫn hiện bản cũ là active và không báo có bản mới đang chờ. Agent đối chiếu và thấy bản active là của một lần duyệt trước, còn giao diện không cho thấy điều đó. Ai chia sẻ skill qua hub nên kiểm tra trạng thái thật trước khi tin là đã cập nhật."
audience: người dùng và người duyệt skill trên hub
spine_context: "Người làm đang đóng thành skill các hướng dẫn đóng gói và phân phối rút từ nhiều dự án CLI, để agent dùng cho dự án sau."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: Đưa skill lên hub skillstation để được duyệt và dùng.
spine_want_lines: ["claude:6a207191#L967"]
spine_obstacle: Lệnh gợi ý cờ --user không tồn tại. Skillstation trên máy là 0.8.0 còn hub là 0.12.0.
spine_obstacle_lines: ["claude:6a207191#L1074", "claude:6a207191#L1102"]
spine_turn: "Tưởng bản mới gửi lên chỉ thay bản đang chạy sau khi bấm duyệt. Hoá ra trang skill vẫn hiện bản cũ là active, và bản đó là của một lần duyệt trước."
spine_turn_lines: ["claude:6a207191#L1489", "claude:6a207191#L1503"]
spine_action: "Agent so bản hub đang phục vụ với thư mục skill trên máy, rồi gửi bản mới kèm skill.yaml."
spine_action_lines: ["claude:6a207191#L1483", "claude:6a207191#L1501"]
spine_outcome: "Bản mới đang chờ duyệt với mã SUB-, nhưng trang skill không báo có bản chờ duyệt. Người xem phải vào mục Waiting for review."
spine_outcome_lines: ["claude:6a207191#L1480", "claude:6a207191#L1515"]
spine_takeaway: "Trang skill phải nói rõ là có bản đang chờ duyệt, nếu không người duyệt dễ duyệt nhầm bản cũ."
spine_takeaway_lines: ["claude:6a207191#L1515"]
completeness: 7
---

# Lỗi UX từ chính công cụ của mình: gợi ý cờ --user không tồn tại, và hub 'active' không phải bản vừa gửi

**Góc kể:** Một người làm bộ hướng dẫn đóng gói và phân phối cho các dự án CLI, đóng thành skill để agent dùng, rồi đưa lên hub skillstation. Họ tin rằng bản mới chỉ thay bản đang chạy sau khi bấm duyệt, nhưng trang skill vẫn hiện bản cũ là active và không báo có bản mới đang chờ. Agent đối chiếu và thấy bản active là của một lần duyệt trước, còn giao diện không cho thấy điều đó. Ai chia sẻ skill qua hub nên kiểm tra trạng thái thật trước khi tin là đã cập nhật.
**Bối cảnh:** Chủ dùng skillstation để đưa skill lên hub từ xa. Agent gặp hàng loạt trục trặc khi gửi và duyệt.
**Chuyện gì xảy ra:** Thông báo lỗi gợi ý cờ --user, nhưng connect không có cờ đó (skillstation 0.8.0 trên máy, hub 0.12.0). Sau khi kết nối toàn cục và đẩy bản gửi, trang skill vẫn hiện bản cũ là 'active' mà không báo có bản chờ duyệt. Ba bản gửi cùng một skill cùng nằm trong hàng chờ. Agent đã viết một thay đổi UI cho trang chi tiết và danh sách skill (229 test web qua), merge và push lên main, CI xanh.
**Bài học:** Thông báo lỗi và trạng thái 'đang dùng' phải nói rõ có bản đang chờ. Nếu không, người duyệt sẽ duyệt nhầm bản cũ.
**Artefact:** Ảnh chụp trang skill có dải 'An update to this skill is waiting for review' (che SUB-id và địa chỉ hub).
**Góc người ngoài:** cách làm phổ biến là Dev thường hoặc làm theo gợi ý của công cụ, hoặc dừng lại hỏi người khác; ít ai tự đối chiếu trạng thái thật trên đĩa sau mỗi thao tác cấu hình; ở đây khác ở Agent không đoán 'chắc đã xong', mà đo lại bằng bằng chứng (grep file, so phiên bản, chạy doctor) và báo rõ phần nào đã có, phần nào chưa. Người đọc sẽ muốn biết vì sao cách này tránh được lỗi 'tưởng đã kết nối'.
