---
id: 2026-10-29-loi-gemini-3-pro-no-longer-c455
code: M-8SHY
aliases: [M-8SHY]
date: 2026-10-29
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1519", "claude:0faf0bb2#L1574"]
hook: "Ba lỗi trong một lần thử, mỗi lỗi thuộc về một tầng khác nhau"
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

# Lỗi 'Gemini 3 Pro no longer available' và sự cố tự đóng task: hai bằng chứng cho ranh giới giữa lớp điều phối và lớp runtime

**Bối cảnh:** Chủ hỏi agent chạy theo cơ chế của Paperclip hay AICoworker. Câu trả lời tách hai lớp: lớp điều phối và lớp suy nghĩ.
**Chuyện gì xảy ra:** Lỗi model thuộc OpenClaw, lỗi 422 khi chuyển in_review thiếu đường duyệt là luật của Paperclip, còn việc agent đoán bừa endpoint là do chưa có skill trong workspace OpenClaw. Ba lỗi cùng một lần spike cho thấy ranh giới rõ ràng.
**Bài học:** Khi agent hỏng, phân biệt lỗi thuộc lớp nào trước khi sửa; mỗi lớp có chủ và cách sửa riêng.
**Artefact:** Bảng 'việc nào thuộc bên nào' trong câu trả lời (không cần che).
