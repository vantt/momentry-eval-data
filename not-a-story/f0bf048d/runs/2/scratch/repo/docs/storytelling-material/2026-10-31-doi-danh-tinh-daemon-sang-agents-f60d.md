---
id: 2026-10-31-doi-danh-tinh-daemon-sang-agents-f60d
code: M-9A43
aliases: [M-9A43]
date: 2026-10-31
repo: repo
status: raw
signals: [so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1983", "claude:f0bf048d#L1987", "claude:f0bf048d#L2400", "claude:f0bf048d#L2409", "claude:f0bf048d#L2435", "claude:f0bf048d#L2436", "claude:f0bf048d#L2457", "claude:f0bf048d#L2543", "claude:f0bf048d#L2550", "claude:f0bf048d#L2569"]
hook: "Thu hồi khóa chủ: tìm thấy ở 3 chỗ, chuyển 12 agent"
tension: tuong_ma_hoa_ra
sides: ["Tưởng khóa chủ chỉ nằm một chỗ", "Nó nằm ở 3 chỗ trong home, phải đổi khóa rồi mới thu hồi"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Multica chạy nhiều agent AI qua một daemon, và người làm đang muốn cấp quyền để chúng tự làm nhiều việc mà không mất dữ liệu. Ở bước đăng nhập, người làm tưởng chạy một lệnh là xong, nhưng script báo token của tài khoản bot phải được tạo trước và file đó chưa có. Sau khi chia sẻ runtime mới và chuyển agent sang, plan báo 0 thay đổi. Ai giao việc cho agent nên kiểm điều kiện của một bước trước khi tin rằng nó đã chạy."
audience: dev dùng agent AI để tự động hoá việc hằng ngày
spine_context: "Dự án Multica, nơi nhiều agent AI chạy công việc qua một daemon. Người làm đang cấp quyền để agent tự làm được nhiều việc mà không gây hậu quả hay mất dữ liệu."
spine_context_lines: ["claude:f0bf048d#L1794", "claude:f0bf048d#L1957"]
spine_want: Cấp quyền để agent tự động làm nhiều nhất có thể mà không gây hậu quả nghiêm trọng và không mất dữ liệu.
spine_want_lines: ["claude:f0bf048d#L1794"]
spine_obstacle: Script đăng nhập cho tài khoản bot dừng vì token của tài khoản đó chưa được tạo.
spine_obstacle_lines: ["claude:f0bf048d#L2400", "claude:f0bf048d#L2412"]
spine_turn: Tưởng chạy xong lệnh đăng nhập là đủ để chuyển agent sang runtime mới; hoá ra script đòi token phải được tạo trước.
spine_turn_lines: ["claude:f0bf048d#L2394", "claude:f0bf048d#L2400", "claude:f0bf048d#L2412"]
spine_action: "Chia sẻ runtime mới, chuyển agent sang đó bằng API, rồi chạy lại lệnh cập nhật từng phần sau khi thấy PUT chỉ cập nhật một phần."
spine_action_lines: ["claude:f0bf048d#L2433", "claude:f0bf048d#L2436", "claude:f0bf048d#L2454"]
spine_outcome: Hai agent kiểm tra trả 200; sau đó plan báo 0 thay đổi trong workspace.
spine_outcome_lines: ["claude:f0bf048d#L2457", "claude:f0bf048d#L2556"]
spine_takeaway: "Trước khi chạy một bước có điều kiện, kiểm xem điều kiện đó đã có chưa."
spine_takeaway_lines: ["claude:f0bf048d#L2400"]
completeness: 7
---

# Đổi danh tính daemon sang agents-opc: thu hồi PAT chủ, chuyển 12 agent

**Góc kể:** Dự án Multica chạy nhiều agent AI qua một daemon, và người làm đang muốn cấp quyền để chúng tự làm nhiều việc mà không mất dữ liệu. Ở bước đăng nhập, người làm tưởng chạy một lệnh là xong, nhưng script báo token của tài khoản bot phải được tạo trước và file đó chưa có. Sau khi chia sẻ runtime mới và chuyển agent sang, plan báo 0 thay đổi. Ai giao việc cho agent nên kiểm điều kiện của một bước trước khi tin rằng nó đã chạy.
**Bối cảnh:** Daemon chạy agent khách đăng nhập bằng PAT chủ. Cần đổi sang user Multica riêng mà không làm gián đoạn agent.
**Chuyện gì xảy ra:** Lệnh sudo lần hai báo lỗi vì file PAT đã bị lệnh lần đầu xoá sau khi dùng. Agent tạo user agents-opc, chia sẻ runtime mới cho chủ, chuyển 12 agent và hai agent của workspace khác sang runtime mới. Tìm thấy PAT chủ ở 3 chỗ trong home, tạo PAT mới, kiểm PAT mới dùng được, rồi thu hồi PAT cũ (trả về 204). Daemon spike là unit tạm nên không có lệnh bật lại.
**Bài học:** Tạo token mới và kiểm nó dùng được trước khi thu hồi token cũ. Ghi lại mọi chỗ token được lưu.
**Artefact:** Bảng số agent và runtime trước và sau chuyển, đã che id.
