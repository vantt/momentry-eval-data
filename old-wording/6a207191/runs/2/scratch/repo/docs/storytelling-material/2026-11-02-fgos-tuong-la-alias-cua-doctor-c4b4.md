---
id: 2026-11-02-fgos-tuong-la-alias-cua-doctor-c4b4
code: M-VY55
aliases: [M-VY55]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L727", "claude:6a207191#L732"]
hook: "Tưởng setup chỉ là alias của doctor, hoá ra nó làm thêm 5 việc"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng tưởng setup chỉ là alias của doctor", "Thực tế setup làm thêm 5 việc doctor không làm"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang gom cách đóng gói và phân phối của nhiều dự án CLI thành một bộ skill chuẩn, và cần làm rõ ba lệnh init, setup, doctor của fgos. Ban đầu họ tưởng setup chỉ là bí danh của doctor. Đọc code mới thấy setup còn làm năm việc doctor không làm: ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill. Dev xây CLI có nhiều lệnh cài đặt nên cần biết, vì lệnh trông trùng có thể đang làm việc riêng."
audience: dev xây công cụ CLI có nhiều lệnh cài đặt và cập nhật
spine_context: "Người làm đang gom cách đóng gói và phân phối của nhiều dự án CLI (mdview, skillstation, herdr-go, forgent, fgos) thành một bộ skill chuẩn."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: "Làm rõ và chuẩn hoá init, setup và doctor, để fgos và các hệ khác có một cách làm thống nhất."
spine_want_lines: ["claude:6a207191#L701"]
spine_obstacle: "Init, setup và doctor --fix chồng chéo nhau, nên người dùng và agent không biết nên chạy lệnh nào."
spine_obstacle_lines: ["claude:6a207191#L727"]
spine_turn: "Tưởng setup chỉ là bí danh của doctor; hoá ra setup còn ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill, những việc doctor --fix không làm."
spine_turn_lines: ["claude:6a207191#L701", "claude:6a207191#L727"]
spine_action: "Chốt doctor là bộ máy duy nhất, init bằng doctor --fix cộng quyền tạo mới, và bỏ setup. Bắt đầu đổi tên skill rồi viết lại các file common."
spine_action_lines: ["claude:6a207191#L727", "claude:6a207191#L732", "claude:6a207191#L734", "claude:6a207191#L735"]
spine_takeaway: "Trước khi gộp một lệnh có vẻ thừa, hãy đọc code xem nó có làm việc riêng không, đừng đoán từ tên lệnh."
spine_takeaway_lines: ["claude:6a207191#L727"]
completeness: 6
---

# fgos tưởng là alias của doctor, hoá ra setup làm thêm 5 việc doctor không làm

**Góc kể:** Người làm đang gom cách đóng gói và phân phối của nhiều dự án CLI thành một bộ skill chuẩn, và cần làm rõ ba lệnh init, setup, doctor của fgos. Ban đầu họ tưởng setup chỉ là bí danh của doctor. Đọc code mới thấy setup còn làm năm việc doctor không làm: ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill. Dev xây CLI có nhiều lệnh cài đặt nên cần biết, vì lệnh trông trùng có thể đang làm việc riêng.
**Bối cảnh:** Chủ nghĩ init và setup chỉ là alias của doctor. Khi đọc code fgos, agent thấy setup làm nhiều việc hơn doctor --fix.
**Chuyện gì xảy ra:** fgos có ba lệnh chồng chéo: init, setup và doctor --fix. Lệnh setup ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill, trong khi doctor --fix chỉ chạy các fix đã đăng ký. Mô tả của chính lệnh setup thừa nhận điều này. Quyết định chuẩn hoá: doctor là bộ máy duy nhất, init = doctor --fix cộng quyền tạo mới, setup bỏ.
**Bài học:** Trước khi chuẩn hoá một lệnh 'thừa', đọc code xem nó có làm việc riêng không. Đừng đoán từ tên lệnh.
**Artefact:** Bảng ba lệnh init/setup/doctor --fix và việc từng lệnh thực sự làm (che đường dẫn nội bộ).
