---
id: 2026-11-05-quy-tac-config-mot-cua-tu
date: 2026-11-05
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2264", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2358", "claude:6a207191#L2385", "claude:6a207191#L2401", "claude:6a207191#L2407"]
hook: "Quy tắc rút từ dự án thật nâng skill từ 212 lên 215 rule"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Quy tắc config một cửa từ dự án momentry được đưa vào skill như ứng viên mới

**Bối cảnh:** Dự án momentry vừa thêm quy tắc: mọi cài đặt, kể cả cài đặt riêng từng dự án, chỉ được đổi qua lệnh config.
**Chuyện gì xảy ra:** Agent đọc commit trong momentry và đối chiếu với skill. Skill thiếu quy tắc cấm cờ lẻ, thiếu --project, show chưa ghi nguồn giá trị, và CFG-12 còn là MAY. Agent thêm CMD-22 (MUST), CMD-23 (SHOULD), CMD-24 (MUST), nâng CFG-12 lên MUST, và số rule tăng từ 212 lên 215. Theo CONTRIBUTING, cách mới chưa chạy với người dùng nên được ghi là chưa chứng minh.
**Bài học:** Một quy tắc từ dự án khác đáng được chép vào bộ chuẩn, nhưng cần ghi rõ mức độ đã kiểm chứng để không coi nó là chân lý.
**Artefact:** Ba dòng CMD-22 đến CMD-24 đã rút gọn, dán cạnh một ví dụ lệnh config show --project.
