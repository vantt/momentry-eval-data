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
hook: "Tưởng setup chỉ là bí danh của doctor, hoá ra làm thêm 5 việc"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng tưởng setup chỉ là bí danh của doctor", "setup âm thầm làm thêm 5 việc doctor không làm"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang gom cách đóng gói và phân phối công cụ dòng lệnh của nhiều dự án thành một skill dùng chung cho agent, trong đó có fgos. Họ tưởng setup chỉ là bí danh của doctor, nhưng đọc code thấy setup còn ghi rc, tạo config, cài git hook, cài Claude hook và copy skill. Người nghe nên quan tâm vì tên lệnh có thể đánh lừa, nên đọc code trước khi gộp hay bỏ lệnh trông thừa."
audience: dev xây công cụ dòng lệnh và dùng agent để làm packaging
spine_context: "Người làm gom cách đóng gói và phân phối các công cụ dòng lệnh của nhiều dự án thành một skill dùng chung cho agent, trong đó có fgos."
spine_context_lines: ["claude:6a207191#L5"]
spine_want: "Muốn chuẩn hoá install, update, config và doctor, và làm rõ setup, init, doctor của fgos."
spine_want_lines: ["claude:6a207191#L5", "claude:6a207191#L701"]
spine_obstacle: "Ba lệnh init, setup và doctor --fix chồng chéo nhau, không rõ lệnh nào làm gì."
spine_obstacle_lines: ["claude:6a207191#L727"]
spine_turn: "Tưởng init và setup chỉ là bí danh của doctor; đọc code thì setup còn ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill, những việc doctor không làm."
spine_turn_lines: ["claude:6a207191#L701", "claude:6a207191#L727"]
spine_action: "Đọc code fgos, đề xuất doctor là bộ máy duy nhất, init là doctor --fix cộng quyền tạo mới, và bỏ setup. Người làm đồng ý và bắt đầu đổi tên, viết lại các file chuẩn."
spine_action_lines: ["claude:6a207191#L709", "claude:6a207191#L727", "claude:6a207191#L732", "claude:6a207191#L734"]
spine_takeaway: "Trước khi chuẩn hoá một lệnh trông thừa, đọc code xem nó có làm việc riêng không, đừng đoán từ tên."
spine_takeaway_lines: ["claude:6a207191#L727"]
completeness: 6
---

# fgos tưởng là alias của doctor, hoá ra setup làm thêm 5 việc doctor không làm

**Góc kể:** Người làm đang gom cách đóng gói và phân phối công cụ dòng lệnh của nhiều dự án thành một skill dùng chung cho agent, trong đó có fgos. Họ tưởng setup chỉ là bí danh của doctor, nhưng đọc code thấy setup còn ghi rc, tạo config, cài git hook, cài Claude hook và copy skill. Người nghe nên quan tâm vì tên lệnh có thể đánh lừa, nên đọc code trước khi gộp hay bỏ lệnh trông thừa.
**Bối cảnh:** Chủ nghĩ init và setup chỉ là alias của doctor. Khi đọc code fgos, agent thấy setup làm nhiều việc hơn doctor --fix.
**Chuyện gì xảy ra:** fgos có ba lệnh chồng chéo: init, setup và doctor --fix. Lệnh setup ghi dòng source vào rc, tạo config, cài git hook, cài Claude hook và copy skill, trong khi doctor --fix chỉ chạy các fix đã đăng ký. Mô tả của chính lệnh setup thừa nhận điều này. Quyết định chuẩn hoá: doctor là bộ máy duy nhất, init = doctor --fix cộng quyền tạo mới, setup bỏ.
**Bài học:** Trước khi chuẩn hoá một lệnh 'thừa', đọc code xem nó có làm việc riêng không. Đừng đoán từ tên lệnh.
**Artefact:** Bảng ba lệnh init/setup/doctor --fix và việc từng lệnh thực sự làm (che đường dẫn nội bộ).
