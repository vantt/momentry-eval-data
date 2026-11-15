---
id: 2026-11-02-fgos-co-ba-lenh-init-setup-c4b4
code: M-PB1C
aliases: [M-PB1C]
date: 2026-11-02
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L727", "claude:6a207191#L732", "claude:6a207191#L735", "claude:6a207191#L749", "claude:6a207191#L802", "claude:6a207191#L897"]
hook: "Ba lệnh tưởng là một, đọc code mới biết mỗi lệnh làm khác"
tension: tuong_ma_hoa_ra
sides: ["setup tưởng chỉ là tên gọi khác của doctor", "Nó còn ghi file rc, cài hook; gộp lại bỏ 18 quy tắc"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án fgos là một hệ phân phối lớn gồm bộ cài fgctl và runtime, đang cần làm rõ ba lệnh init, setup, doctor. Người làm tin setup chỉ là tên gọi khác của doctor, nhưng đọc code thì setup còn ghi file rc, tạo config và cài hook. Ai viết CLI có nhiều lệnh chồng nhau nên đọc code trước khi tin vào alias."
audience: dev xây CLI có nhiều lệnh init/setup/doctor
spine_context: "Hệ fgos gồm fgctl, bộ cài và nâng cấp, và fgos, bộ triển khai runtime. Đang chuẩn hoá cách phân phối cho các dự án."
spine_context_lines: ["claude:6a207191#L701"]
spine_want: "Muốn làm rõ và chuẩn hoá init, setup, doctor cho fgos và các hệ phân phối khác."
spine_want_lines: ["claude:6a207191#L701"]
spine_obstacle: Ba lệnh chồng chéo nên người dùng và agent không biết chạy lệnh nào.
spine_obstacle_lines: ["claude:6a207191#L727"]
spine_turn: "Tưởng setup chỉ là tên gọi khác của doctor; hoá ra setup còn ghi file rc, tạo config và cài hook."
spine_turn_lines: ["claude:6a207191#L701", "claude:6a207191#L727"]
spine_action: "Thiết kế lại: doctor chỉ đọc, doctor --fix chỉ sửa cái đã có, init bằng doctor --fix cộng quyền tạo mới, setup bỏ đi."
spine_action_lines: ["claude:6a207191#L897"]
spine_outcome: Script kiểm tra cấu trúc qua với 212 quy tắc.
spine_outcome_lines: ["claude:6a207191#L892"]
spine_takeaway: "Trước khi chuẩn hoá lệnh, đọc code để biết lệnh thực sự làm gì; giả định về alias thường sai."
spine_takeaway_lines: ["claude:6a207191#L727"]
completeness: 7
---

# fgos có ba lệnh init, setup, doctor chồng nhau; chốt doctor là bộ máy duy nhất

**Góc kể:** Dự án fgos là một hệ phân phối lớn gồm bộ cài fgctl và runtime, đang cần làm rõ ba lệnh init, setup, doctor. Người làm tin setup chỉ là tên gọi khác của doctor, nhưng đọc code thì setup còn ghi file rc, tạo config và cài hook. Ai viết CLI có nhiều lệnh chồng nhau nên đọc code trước khi tin vào alias.
**Bối cảnh:** Hệ fgos gồm fgctl, bộ cài và upgrade, và fgos, bộ deploy runtime. Chủ dự án giả định init và setup chỉ là alias của doctor.
**Chuyện gì xảy ra:** Đọc code thì setup không phải alias: setup bằng doctor --fix cộng thêm ghi file rc, tạo config, cài git hook và Claude hook. init gọi các fix của doctor rồi tạo thư mục .fgos. Thiết kế mới: doctor chỉ đọc, doctor --fix chỉ sửa cái đã có, init bằng doctor --fix cộng quyền tạo mới, setup bỏ hoặc giữ làm alias ẩn. Sau khi viết lại, số quy tắc từ 230 còn 212.
**Bài học:** Trước khi chuẩn hoá lệnh, đọc code để biết lệnh thực sự làm gì. Giả định về alias thường sai.
**Artefact:** Bảng bốn lệnh và việc thật của từng lệnh. Không có thông tin cần che.
