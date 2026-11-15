---
id: 2026-11-02-day-merge-khi-con-mot-test-40f9
code: M-S7GC
aliases: [M-S7GC]
date: 2026-11-02
repo: repo
status: raw
signals: [khac]
signal_note: "Agent tự nhận đã đẩy code khi chưa kiểm xanh, và sau đó kiểm chứng test không ổn định."
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2796", "claude:c4caee3c#L2811", "claude:c4caee3c#L2818", "claude:c4caee3c#L2819"]
hook: "Đẩy merge khi còn test đỏ vì chạy lại 3 lần đều xanh"
tension: tuong_ma_hoa_ra
sides: ["Ba lần chạy lại đều xanh", "Vẫn nên dừng trước khi đẩy"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đẩy merge khi còn một test đỏ

**Bối cảnh:** Merge một nhánh vào master trong lúc kiểm test song song.
**Chuyện gì xảy ra:** Merge được đẩy lên trong khi gói có một test đỏ. Agent chạy lại ba lần và cả ba đều xanh, nên kết luận đó là test chập chờn dưới tải nặng. Agent thừa nhận lẽ ra phải dừng trước khi đẩy.
**Bài học:** Chạy test trước khi đẩy, kể cả khi merge nhỏ. Test chập chờn vẫn phải được ghi nhận, không được bỏ qua.
