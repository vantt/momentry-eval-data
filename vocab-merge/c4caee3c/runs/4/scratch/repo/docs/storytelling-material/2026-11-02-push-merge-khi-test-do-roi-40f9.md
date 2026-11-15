---
id: 2026-11-02-push-merge-khi-test-do-roi-40f9
code: M-9JSF
aliases: [M-9JSF]
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2796", "claude:c4caee3c#L2811", "claude:c4caee3c#L2818", "claude:c4caee3c#L2819"]
hook: "Push merge khi test đỏ, chạy lại ba lần đều xanh 459/459"
tension: tuong_ma_hoa_ra
sides: ["test đỏ báo có lỗi thật", "chạy lại ba lần đều xanh, nghi test tốc độ chớp hỏng"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Push merge khi test đỏ rồi mới kiểm

**Bối cảnh:** Merge nhánh V13b vào master kèm một test đỏ trong gói. Agent đã push trước khi kiểm lại.
**Chuyện gì xảy ra:** Agent tự nhận đó là sai quy trình. Chạy lại ba lần đều xanh 459/459, nên nghi test tốc độ bị chớp hỏng khi máy tải nặng.
**Bài học:** Chạy test và tsc trước khi push merge; ghi nhận test chớp hỏng dưới tải thay vì bỏ qua.
