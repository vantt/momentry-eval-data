---
id: 2026-11-02-day-merge-khi-test-con-do
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1295", "claude:c4caee3c#L1314", "claude:c4caee3c#L2796", "claude:c4caee3c#L2811", "claude:c4caee3c#L2812", "claude:c4caee3c#L2818", "claude:c4caee3c#L2819"]
hook: "Lead đẩy merge khi còn một test đỏ, rồi tắt luôn hook chặn"
tension: cam_ma_van_lot
sides: ["Hook pre-push đã chặn, test còn đỏ", "HUSKY=0 cho push lọt, merge vẫn đi"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đẩy merge khi test còn đỏ, và pre-push hook bị bỏ qua bằng HUSKY=0

**Bối cảnh:** Lead merge nhiều nhánh agent vào master và đẩy lên origin. Một số lần merge có test đỏ hoặc commit không có gì để thêm.
**Chuyện gì xảy ra:** Lần merge V13b được đẩy trong khi gói có một test đỏ; lead thừa nhận lẽ ra phải dừng. Chạy lại ba lần đều xanh, nên nhiều khả năng test tốc độ bị ảnh hưởng vì máy đang tải nặng. Trước đó hook pre-push của upstream chặn push, và phiên làm việc đặt HUSKY=0 cho các lệnh push sau đó.
**Bài học:** Đừng đẩy khi test đỏ dù tin là test không ổn định; và đừng tắt hook như thói quen, hãy tìm nguyên nhân hook chặn.
**Artefact:** Dòng log test đỏ và ba lần chạy lại xanh.
