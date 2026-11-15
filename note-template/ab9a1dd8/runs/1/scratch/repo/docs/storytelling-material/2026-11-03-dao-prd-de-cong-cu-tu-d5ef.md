---
id: 2026-11-03-dao-prd-de-cong-cu-tu-d5ef
code: M-J96Z
aliases: [M-J96Z]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L615"]
hook: "Để init tự sửa file cấu hình người dùng: 300 dòng và một cái giá"
tension: chon_mot_mat_mot
sides: ["Init tự cài hook, người dùng khỏi làm tay", "Ghi lại file có thể làm đổi định dạng của người dùng"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: Dự án momentry đọc transcript các phiên làm việc với coding agent để nhặt chuyện đáng kể; đang chuẩn bị đóng gói và phân phối.
spine_context_lines: [profile, "claude:ab9a1dd8#L42"]
spine_want: "Người dùng chạy một lệnh là cài xong, init tự cài hook vào Claude Code và Codex."
spine_want_lines: ["claude:ab9a1dd8#L42", "claude:ab9a1dd8#L340"]
spine_obstacle: "PRD chốt công cụ không tự sửa file cấu hình của người dùng, vì sửa file chung có rủi ro."
spine_obstacle_lines: ["claude:ab9a1dd8#L256"]
spine_action: "Lập plan triển khai theo quyết định tự cài hook, rồi ghi quyết định vào checklist và tài liệu."
spine_action_lines: ["claude:ab9a1dd8#L345", "claude:ab9a1dd8#L615"]
spine_outcome: Quyết định đã được ghi vào checklist và plan.
spine_outcome_lines: ["claude:ab9a1dd8#L616"]
spine_takeaway: "Khi đảo một quyết định đã chốt, ghi rõ cái giá đi kèm và sửa tài liệu cùng lúc."
spine_takeaway_lines: ["claude:ab9a1dd8#L615"]
completeness: 6
---

# Đảo PRD: để công cụ tự cài hook vào file cấu hình của người dùng

**Bối cảnh:** PRD từng chốt công cụ không bao giờ tự sửa ~/.claude/settings.json hay file cấu hình Codex.
**Chuyện gì xảy ra:** Chủ đổi sang để init tự cài. Agent ước khoảng 200 đến 300 dòng code cộng test, phần khó là ghi file an toàn: sao lưu, từ chối khi file hỏng, ghi qua file tạm rồi đổi tên, và kiểm file không bị đổi giữa chừng. Cái giá được nêu rõ là có thể đổi định dạng nhẹ của file người dùng khi ghi lại. Plan được sửa để khớp quyết định mới.
**Bài học:** Khi đảo một quyết định đã chốt trong PRD, liệt kê cái giá đi kèm và sửa PRD cùng lúc để tài liệu không lệch code.
**Artefact:** Sơ đồ bốn bước ghi an toàn: sao lưu, kiểm đã đổi chưa, ghi tạm, đổi tên.
**Góc người ngoài:** cách làm phổ biến là Công cụ in đoạn JSON rồi bắt người dùng tự dán vào `settings.json`, hoặc hướng dẫn đọc tài liệu rồi tự sửa; ở đây khác ở Người dùng chạy một lệnh là xong; nhưng vì sửa file cấu hình dùng chung của người khác nên có sao lưu và nhận diện mục của mình. Người đọc sẽ muốn biết cách làm 'chỉ đụng phần của mình' an toàn.
