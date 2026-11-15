---
id: 2026-11-05-momentry-co-quy-tac-mot-cua-c4b4
code: M-HBZS
aliases: [M-HBZS]
date: 2026-11-05
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L2255", "claude:6a207191#L2324", "claude:6a207191#L2333", "claude:6a207191#L2393"]
hook: "Thêm 3 quy tắc, nâng 1 lên bắt buộc: khoá riêng không vào repo"
tension: none
sides: []
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Momentry có quy tắc một cửa config; skill thiếu, thêm CMD-22 đến CMD-24

**Bối cảnh:** Chủ dự án nhắc có quy tắc mới về config trong repo momentry, và hỏi skill đã có quy chuẩn này chưa.
**Chuyện gì xảy ra:** Quy tắc mới: mọi thiết lập đổi qua một lệnh config, thiết lập riêng dự án thêm cờ --project. Skill chỉ có các mảnh rời. Agent thêm ba rule và nâng CFG-12 từ MAY lên MUST: file của repo không được ghi khoá riêng của máy. Số quy tắc từ 212 lên 215, và các đường dẫn tham chiếu đều tồn tại.
**Bài học:** Quy chuẩn tốt có thể học từ dự án khác. Khi đưa về skill chung, cần tách rõ ba phần: lệnh, phạm vi dự án và bảo vệ file của repo.
**Artefact:** Bảng đối chiếu quy tắc của momentry với skill. Cần che tên file nội bộ.
