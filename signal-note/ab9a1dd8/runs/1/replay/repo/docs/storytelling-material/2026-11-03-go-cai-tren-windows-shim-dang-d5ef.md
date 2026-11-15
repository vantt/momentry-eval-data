---
id: 2026-11-03-go-cai-tren-windows-shim-dang-d5ef
code: M-JH28
aliases: [M-JH28]
date: 2026-11-03
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1574", "claude:ab9a1dd8#L1575", "claude:ab9a1dd8#L1588", "claude:ab9a1dd8#L2138", "claude:ab9a1dd8#L2151", "claude:ab9a1dd8#L2152"]
hook: "Gỡ cài Windows: shim đang chạy không xoá được, thư mục cache bị sót"
tension: cam_ma_van_lot
sides: ["Điều kiện an toàn chặn xoá thư mục không tên momentry", "Thư mục tên cache bị sót khi purge"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang chuẩn bị gói cài đặt cho nó. Khi viết lệnh gỡ cài, họ muốn gỡ đúng phần của momentry và giữ dữ liệu trừ khi người dùng chọn --purge. Họ tin điều kiện an toàn 'chỉ xoá thư mục có tên momentry' là đủ, nhưng thư mục cache bên trong tên là 'cache' nên --purge bỏ sót nó. Ai viết lệnh xoá theo tên đều có thể dính đúng lỗi này, nên phải kiểm cả thư mục cha."
audience: dev viết lệnh cài đặt và gỡ cài
spine_context: "Momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang chuẩn bị gói phân phối cho nó."
spine_context_lines: [profile, "claude:ab9a1dd8#L664"]
spine_want: "Gỡ đúng phần của momentry, giữ hộp chuyện và cấu hình, chỉ xoá cache khi có --purge."
spine_want_lines: ["claude:ab9a1dd8#L2133"]
spine_obstacle: File shim đang chạy trên Windows không xoá được ngay.
spine_obstacle_lines: ["claude:ab9a1dd8#L1588"]
spine_turn: Tưởng điều kiện 'tên thư mục chứa momentry' là đủ để bảo vệ; hoá ra thư mục cache tên 'cache' nằm trong momentry nên --purge bỏ sót nó.
spine_turn_lines: ["claude:ab9a1dd8#L2138", "claude:ab9a1dd8#L2151"]
spine_action: Thêm xoá trễ cho shim trên Windows; nới điều kiện an toàn để nhận thêm thư mục cha tên momentry.
spine_action_lines: ["claude:ab9a1dd8#L1575", "claude:ab9a1dd8#L2152"]
spine_outcome: "Chạy lại: 232 test qua, 0 test đỏ; các sửa riêng cho Windows chưa được chạy."
spine_outcome_lines: ["claude:ab9a1dd8#L2155", "claude:ab9a1dd8#L2160"]
spine_takeaway: Điều kiện an toàn khi xoá theo tên dễ bỏ sót thư mục đúng; kiểm cả thư mục cha và viết test purge cho từng hệ điều hành.
spine_takeaway_lines: ["claude:ab9a1dd8#L2151", "claude:ab9a1dd8#L2160"]
completeness: 7
---

# Gỡ cài trên Windows: shim đang chạy không xoá được ngay, và thư mục cache tên cache bị bỏ sót

**Góc kể:** Momentry là công cụ đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể, và người làm đang chuẩn bị gói cài đặt cho nó. Khi viết lệnh gỡ cài, họ muốn gỡ đúng phần của momentry và giữ dữ liệu trừ khi người dùng chọn --purge. Họ tin điều kiện an toàn 'chỉ xoá thư mục có tên momentry' là đủ, nhưng thư mục cache bên trong tên là 'cache' nên --purge bỏ sót nó. Ai viết lệnh xoá theo tên đều có thể dính đúng lỗi này, nên phải kiểm cả thư mục cha.
**Bối cảnh:** Uninstall phải gỡ đúng phần của momentry và giữ dữ liệu trừ khi có --purge.
**Chuyện gì xảy ra:** Trên Windows, file shim đang chạy không xoá được ngay, nên agent thêm cơ chế xoá trễ sau khi lệnh thoát. Điều kiện an toàn yêu cầu tên thư mục chứa momentry, nên thư mục cache tên cache bị bỏ sót khi --purge; phải nới điều kiện thêm thư mục cha tên momentry.
**Bài học:** Điều kiện an toàn khi xoá theo tên dễ bỏ sót thư mục đúng. Kiểm cả thư mục cha và viết test purge cho từng hệ điều hành.
**Artefact:** Kết quả gỡ cài: giữ hộp chuyện và cấu hình, xoá cache khi có --purge.
