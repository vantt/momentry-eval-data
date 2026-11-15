---
id: 2026-11-02-chuan-hoa-init-doctor-doctor-la
date: 2026-11-02
repo: repo
status: raw
signals: [đảo quyết định có lý do]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L727", "claude:6a207191#L734", "claude:6a207191#L749", "claude:6a207191#L766", "claude:6a207191#L782", "claude:6a207191#L802", "claude:6a207191#L831", "claude:6a207191#L897"]
hook: "Bỏ lệnh setup, để doctor làm bộ máy kiểm tra duy nhất"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chuẩn hoá init/doctor: doctor là bộ máy duy nhất, init = doctor --fix cộng tạo mới

**Bối cảnh:** Sau khi đọc fgos, người dùng đồng ý mô hình: doctor là bộ máy duy nhất, mọi trạng thái mong muốn là một check có cách fix.
**Chuyện gì xảy ra:** Agent viết lại các file common. init là doctor --fix cộng quyền tạo mới. doctor chỉ đọc. doctor --fix không bao giờ biến một thư mục bất kỳ thành project. setup bỏ, chỉ giữ như alias ẩn của init. Thêm hai kiểu phân phối: A (một binary có update) và B (bộ cài và runtime như fgctl, update chỉ chuyển sang ctl upgrade). Viết lại các file 00, 03, 05, 07, 30, 40, 50, 60, 80, 85, 90 và SKILL, CONTRIBUTING, references. Bản này cũng sửa mâu thuẫn từ review: INS-13 dùng init, installer in Next với đường dẫn tuyệt đối.
**Bài học:** Khi một nhóm lệnh có nhiều đường cài đặt, chọn một bộ máy kiểm tra duy nhất và biến mọi lệnh khác thành cách gọi tới nó.
**Artefact:** Bảng hai kiểu phân phối A và B và việc của init, doctor, update.
