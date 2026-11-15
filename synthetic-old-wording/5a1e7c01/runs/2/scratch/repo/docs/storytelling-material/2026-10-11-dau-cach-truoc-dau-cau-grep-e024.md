---
id: 2026-10-11-dau-cach-truoc-dau-cau-grep-e024
code: M-F145
aliases: [M-F145]
date: 2026-10-11
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:5a1e7c01"
sessions: ["claude:5a1e7c01"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:5a1e7c01#L66", "claude:5a1e7c01#L67", "claude:5a1e7c01#L68", "claude:5a1e7c01#L69", "claude:5a1e7c01#L70", "claude:5a1e7c01#L71", "claude:5a1e7c01#L72"]
hook: "Sửa dấu cách trước dấu câu, tiện tay đổi luôn lời chào hai dòng"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Chủ bản tin đang viết số 48 của Thư Chủ Nhật, một bản tin email hằng tuần."
spine_context_lines: ["claude:5a1e7c01#L1"]
spine_want: Soát toàn bài để xoá mọi dấu cách thừa trước dấu câu.
spine_want_lines: ["claude:5a1e7c01#L66"]
spine_obstacle: "Grep tìm thấy hai dòng còn dấu cách trước dấu câu: một trong bài và một ở lời chào cuối thư."
spine_obstacle_lines: ["claude:5a1e7c01#L68"]
spine_action: "Dùng sed xoá dấu cách trước dấu câu trong toàn bài, rồi đếm lại bằng grep."
spine_action_lines: ["claude:5a1e7c01#L69"]
spine_outcome: Đếm lại ra 0 dòng vi phạm.
spine_outcome_lines: ["claude:5a1e7c01#L70"]
spine_takeaway: "Soát dấu câu bằng grep trước, sed sau, rồi đếm lại để có con số 0 làm bằng chứng."
spine_takeaway_lines: ["claude:5a1e7c01#L69", "claude:5a1e7c01#L70"]
completeness: 6
---

# Dấu cách trước dấu câu: grep tìm trước, sed sửa sau, đếm lại ra 0

**Bối cảnh:** Chủ bản tin muốn soát toàn bài để tìm dấu cách thừa trước dấu câu, đặc biệt ở lời chào cuối thư.
**Chuyện gì xảy ra:** Agent dùng grep để tìm được hai dòng vi phạm, một dòng trong bài và một dòng ở lời chào. Sau đó chạy sed để xoá dấu cách trước mọi dấu câu, rồi chạy lại grep đếm và nhận kết quả 0. Trong lúc sửa, agent đổi lời chào thành hai dòng để gọn hơn trên điện thoại, và chủ bản tin đồng ý.
**Bài học:** Soát dấu câu bằng grep trước, sed sau, rồi đếm lại; con số 0 là bằng chứng chắc hơn việc đọc bằng mắt.
**Artefact:** Đầu ra grep gồm số dòng và nội dung vi phạm (che đoạn văn), kèm dòng kết quả đếm bằng 0.
