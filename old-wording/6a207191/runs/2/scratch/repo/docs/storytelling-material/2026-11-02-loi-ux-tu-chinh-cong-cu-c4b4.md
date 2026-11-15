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
hook: "Lỗi gợi ý cờ --user không tồn tại, hub vẫn hiện bản cũ là 'active'"
tension: tuong_ma_hoa_ra
sides: ["Đã gửi bản mới lên hub, tưởng bản mới đang chạy", "Trang vẫn hiện bản cũ là active, bản mới nằm im trong hàng chờ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lỗi UX từ chính công cụ của mình: gợi ý cờ --user không tồn tại, và hub 'active' không phải bản vừa gửi

**Bối cảnh:** Chủ dùng skillstation để đưa skill lên hub từ xa. Agent gặp hàng loạt trục trặc khi gửi và duyệt.
**Chuyện gì xảy ra:** Thông báo lỗi gợi ý cờ --user, nhưng connect không có cờ đó (skillstation 0.8.0 trên máy, hub 0.12.0). Sau khi kết nối toàn cục và đẩy bản gửi, trang skill vẫn hiện bản cũ là 'active' mà không báo có bản chờ duyệt. Ba bản gửi cùng một skill cùng nằm trong hàng chờ. Agent đã viết một thay đổi UI cho trang chi tiết và danh sách skill (229 test web qua), merge và push lên main, CI xanh.
**Bài học:** Thông báo lỗi và trạng thái 'đang dùng' phải nói rõ có bản đang chờ. Nếu không, người duyệt sẽ duyệt nhầm bản cũ.
**Artefact:** Ảnh chụp trang skill có dải 'An update to this skill is waiting for review' (che SUB-id và địa chỉ hub).
**Góc người ngoài:** cách làm phổ biến là Dev thường hoặc làm theo gợi ý của công cụ, hoặc dừng lại hỏi người khác; ít ai tự đối chiếu trạng thái thật trên đĩa sau mỗi thao tác cấu hình; ở đây khác ở Agent không đoán 'chắc đã xong', mà đo lại bằng bằng chứng (grep file, so phiên bản, chạy doctor) và báo rõ phần nào đã có, phần nào chưa. Người đọc sẽ muốn biết vì sao cách này tránh được lỗi 'tưởng đã kết nối'.
