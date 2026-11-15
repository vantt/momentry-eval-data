---
id: 2026-11-02-gia-thuyet-setup-la-alias-cua
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L701", "claude:6a207191#L709", "claude:6a207191#L719", "claude:6a207191#L727"]
hook: "Tưởng setup chỉ là alias của doctor, hóa ra làm thêm 5 việc"
tension: tuong_ma_hoa_ra
sides: ["Giả thuyết setup chỉ là alias của doctor", "Setup còn ghi rc, git hook, Claude hook, copy skill"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Giả thuyết 'setup là alias của doctor' sai: setup còn ghi thêm 5 thứ ngoài doctor

**Bối cảnh:** fgos là một hệ lớn, còn fgctl là bộ cài và nâng cấp chứ không phải binary. Người dùng đoán init và setup chỉ là alias của doctor.
**Chuyện gì xảy ra:** Đọc code cho thấy giả thuyết sai. fgctl init chạy tuần tự fgos init, doctor --fix rồi doctor. Lệnh setup cũ gọi cùng các fix, cộng thêm năm việc doctor không làm: ghi dòng source vào rc, tạo file cấu hình, cài git hook, cài Claude hook, copy skill. Chính help của setup ghi rằng doctor --fix chỉ chạy các fix đã đăng ký. Từ đó thiết kế chuyển sang một bộ máy kiểm tra duy nhất.
**Bài học:** Trước khi chuẩn hoá một nhóm lệnh, đọc xem từng lệnh thực sự ghi gì. Giả định 'alias' phải kiểm bằng code.
**Artefact:** Bảng các lệnh init, fgctl init, setup, doctor --fix và việc thực tế của từng lệnh.
