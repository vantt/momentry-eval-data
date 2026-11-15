---
id: 2026-11-02-mau-tham-chieu-chon-sai-ngon
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L690", "claude:6a207191#L897"]
hook: "Go CLI bị trỏ sang mẫu Rust, trong khi có sẵn mẫu Go"
tension: giup_ma_hai
sides: ["Skill chỉ mẫu tham chiếu để làm theo", "Mẫu là code Rust, còn dự án Go cùng loại có sẵn"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Mẫu tham chiếu chọn sai ngôn ngữ: Go CLI bị trỏ sang code Rust

**Bối cảnh:** Skill có nguyên tắc 'Proven ways first': khi có code mẫu đã chạy thì phải chép từ đó. Nhưng mẫu được chọn theo tiêu chí nào?
**Chuyện gì xảy ra:** Reviewer chỉ ra một Go CLI sẽ được trỏ tới code Rust của mdview, trong khi skillstation (Go, có MCP proxy) là dự án cùng loại. GO-03 còn khuyên goreleaser dù skillstation không dùng. Agent thêm bảng 'Start from' theo loại dự án vào references.md, thêm cột ngôn ngữ, và đổi GO-03 sang pipeline của skillstation.
**Bài học:** Mẫu tham chiếu phải chọn theo cả ngôn ngữ lẫn loại ứng dụng, đừng chỉ dựa vào việc nó có sẵn.
**Artefact:** Bảng 'Start from' theo loại dự án.
