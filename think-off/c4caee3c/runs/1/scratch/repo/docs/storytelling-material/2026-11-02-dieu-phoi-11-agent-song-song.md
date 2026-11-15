---
id: 2026-11-02-dieu-phoi-11-agent-song-song
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L87", "claude:c4caee3c#L902", "claude:c4caee3c#L945", "claude:c4caee3c#L1199", "claude:c4caee3c#L1426", "claude:c4caee3c#L1434", "claude:c4caee3c#L1570", "claude:c4caee3c#L2929"]
hook: "11 agent chạy song song, nhưng hai bản vá cùng sửa cli.ts nên đảo thứ tự là vỡ"
tension: hop_ma_tan
sides: ["11 agent làm song song cho nhanh", "Hai bản vá cùng sửa một file, đảo thứ tự là xung đột"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Điều phối 11 agent song song: worktree, xung đột và thứ tự chuỗi bản vá

**Bối cảnh:** Roadmap gồm khoảng 25 việc. Lead mở tới 11 agent cùng lúc, mỗi agent một worktree, rồi tự ghép kết quả vào master.
**Chuyện gì xảy ra:** Chuỗi bản vá phải áp đúng thứ tự, vì P03 và P00 cùng sửa cli.ts nên lỗi xung đột khi đảo. Lead dựng nhánh ghép riêng, tái tạo chuỗi theo đúng thứ tự, rồi chạy full gate. Một lần merge bị huỷ vì có thay đổi chưa commit; việc merge nhánh V18 phải giao lại cho chính agent giải xung đột.
**Bài học:** Chuỗi bản vá đè lên nhau thì phải có thứ tự rõ và một nhánh ghép kiểm định, không phải nối vào cuối.
**Artefact:** Sơ đồ thứ tự chuỗi bản vá, chỉ tên bản vá, không kèm nội dung.
