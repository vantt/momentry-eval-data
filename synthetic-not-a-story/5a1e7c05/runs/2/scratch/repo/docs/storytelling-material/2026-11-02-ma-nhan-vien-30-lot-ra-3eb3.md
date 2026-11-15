---
id: 2026-11-02-ma-nhan-vien-30-lot-ra-3eb3
code: M-458A
aliases: [M-458A]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo, rang_buoc_thiet_ke]
source: "chat Claude, claude:5a1e7c05"
sessions: ["claude:5a1e7c05"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:5a1e7c05#L34", "claude:5a1e7c05#L35", "claude:5a1e7c05#L36", "claude:5a1e7c05#L37", "claude:5a1e7c05#L38", "claude:5a1e7c05#L39", "claude:5a1e7c05#L40", "claude:5a1e7c05#L41", "claude:5a1e7c05#L42", "claude:5a1e7c05#L43", "claude:5a1e7c05#L44"]
hook: "Mã của 4 nhân viên bị dùng 247 lần bởi 163 số điện thoại"
tension: cam_ma_van_lot
sides: ["Mã giảm 30% chỉ dành cho 4 nhân viên trong tiệm", "Lọt lên nhóm Facebook, 163 số lạ dùng, thất thoát khoảng 8 triệu"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một tiệm bánh nhỏ ở Đà Lạt đang dùng AI agent để xem lại cả năm bán hàng và tìm chỗ thất thoát. Chủ tiệm tin mã giảm 30% chỉ nằm trong tay 4 nhân viên, nhưng mã đã được dùng 247 lần với 163 số điện thoại khác nhau. Hoá ra mã được đăng lên một nhóm Facebook, và lỗi nằm ở cơ chế: mã chung ai cũng dùng được, thu ngân không kiểm người dùng. Ai từng dùng mã giảm giá dùng chung nên đọc vì lỗ hổng này không cần ai làm sai mới xảy ra."
audience: dev dùng AI hằng ngày muốn biết agent giúp việc kinh doanh thật
spine_context: Một tiệm bánh nhỏ ở Đà Lạt đang dùng AI agent để xem lại cả năm bán hàng từ KiotViet.
spine_context_lines: ["claude:5a1e7c05#L1"]
spine_want: "Muốn biết có ai dùng mã giảm giá trên 10% không, vì quy định chỉ cho giảm tối đa 10% cho khách."
spine_want_lines: ["claude:5a1e7c05#L34"]
spine_obstacle: "Mã NV30 (giảm 30%, chỉ dành cho nhân viên) đã dùng 247 lần với 163 số điện thoại, trong khi tiệm chỉ có 4 nhân viên."
spine_obstacle_lines: ["claude:5a1e7c05#L36", "claude:5a1e7c05#L38"]
spine_turn: Chủ tiệm tin mã chỉ nằm trong tay 4 nhân viên; hoá ra khách lạ đã dùng mã vì mã được đăng lên nhóm Facebook.
spine_turn_lines: ["claude:5a1e7c05#L38", "claude:5a1e7c05#L40"]
spine_action: "Agent quét lịch sử dùng mã và đọc ghi chú thu ngân, rồi đề xuất thay mã chung bằng giảm giá gắn với từng nhân viên; chủ tiệm tắt mã NV30."
spine_action_lines: ["claude:5a1e7c05#L35", "claude:5a1e7c05#L39", "claude:5a1e7c05#L41", "claude:5a1e7c05#L43", "claude:5a1e7c05#L44"]
spine_outcome: Mã NV30 bị tắt ngay tối đó; ước tính khoảng 8 triệu tiền giảm ngoài quy định.
spine_outcome_lines: ["claude:5a1e7c05#L41", "claude:5a1e7c05#L44"]
spine_takeaway: Mã giảm giá dùng chung cho nhân viên là lối đi vòng; nên gắn quyền giảm giá với từng người có tên.
spine_takeaway_lines: ["claude:5a1e7c05#L41", "claude:5a1e7c05#L43"]
completeness: 7
---

# Mã nhân viên 30% lọt ra ngoài: 212 lần dùng trong hai tháng, từ 4 nhân viên

**Góc kể:** Một tiệm bánh nhỏ ở Đà Lạt đang dùng AI agent để xem lại cả năm bán hàng và tìm chỗ thất thoát. Chủ tiệm tin mã giảm 30% chỉ nằm trong tay 4 nhân viên, nhưng mã đã được dùng 247 lần với 163 số điện thoại khác nhau. Hoá ra mã được đăng lên một nhóm Facebook, và lỗi nằm ở cơ chế: mã chung ai cũng dùng được, thu ngân không kiểm người dùng. Ai từng dùng mã giảm giá dùng chung nên đọc vì lỗ hổng này không cần ai làm sai mới xảy ra.
**Bối cảnh:** Tiệm quy định giảm giá khách tối đa 10%, còn mã 30% chỉ dành cho nhân viên mua bánh mang về nhà. Agent quét lịch sử dùng mã trong KiotViet.
**Chuyện gì xảy ra:** Mã NV30 đã dùng 247 lần với 163 số điện thoại khác nhau, trong khi tiệm chỉ có 4 nhân viên. Lượt dùng tháng 6-8 chỉ 7-17 lần mỗi tháng, nhưng tháng 9 lên 98 và tháng 10 là 114. Ghi chú thu ngân cho thấy khách nói có thấy mã trên một nhóm Facebook, ước tính khoảng 8 triệu tiền giảm ngoài quy định. Chủ tiệm tắt mã ngay trong tối đó.
**Bài học:** Mã giảm giá dùng chung cho nhân viên là lối đi vòng; nên gắn quyền giảm giá với từng người có tên thay vì một mã mà ai có cũng dùng được.
**Artefact:** Bảng số lần dùng mã theo tháng, đã che số điện thoại và nội dung ghi chú của thu ngân.
**Góc người ngoài:** cách làm phổ biến là Người quản lý thường đi tìm ai làm lộ, rồi nhắc nhở hoặc phạt người đó; ở đây khác ở Agent tập trung vào cơ chế, cụ thể là mã dùng chung và thu ngân không kiểm tra người dùng. Cách này xử lý được lỗ hổng mà không cần bắt lỗi ai, và người đọc sẽ muốn biết vì sao agent chọn hướng này.
