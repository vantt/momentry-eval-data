---
id: 2026-11-02-thu-loi-co-y-de-kiem
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:6a207191#L290", "claude:6a207191#L292", "claude:6a207191#L422", "claude:6a207191#L423", "claude:6a207191#L424", "claude:6a207191#L440", "claude:6a207191#L441", "claude:6a207191#L533", "claude:6a207191#L536", "claude:6a207191#L855", "claude:6a207191#L856"]
hook: "Chèn lỗi cố ý UPD-99 để chứng minh lint thật sự bắt được lỗi"
tension: khac
sides: ["Lint báo exit 1 vì thiếu shellcheck, không phải vì lỗi thật", "Phải tự gài lỗi giả mới biết lint có canh gác"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử lỗi cố ý để kiểm script: lint bắt ID sai, check đường dẫn bắt glob không khớp

**Bối cảnh:** Skill có hai script tự kiểm: một kiểm cấu trúc, một kiểm các đường dẫn tham chiếu tới code thật bằng gh api trên GitHub.
**Chuyện gì xảy ra:** Lần kiểm tham chiếu đầu báo hai đường dẫn không tồn tại: một glob health*.go không khớp file nào và một file bị gọi sai tên, agent sửa cả hai. Lint lần đầu trả exit 1 vì máy thiếu shellcheck, agent nói rõ điều đó chứ không coi là đạt. Để chắc lint bắt được lỗi thật, agent chèn ID UPD-99 vào tham chiếu, lint báo unknown rule. Dải CMD-19..23 bị báo thiếu CMD-22 và CMD-23.
**Bài học:** Kiểm tra chính bộ kiểm tra: cài một lỗi có chủ đích và xem nó có bị bắt không. Khi exit khác 0 do thiếu công cụ thì nói rõ điều đó.
**Artefact:** Đầu ra lint có dòng ERROR do lỗi cố ý tạo ra.
