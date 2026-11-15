---
id: 2026-10-29-chon-nen-ui-circle-dep-hon-c455
code: M-GGB6
aliases: [M-GGB6]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3279", "claude:0faf0bb2#L3288", "claude:0faf0bb2#L3290", "claude:0faf0bb2#L3329"]
hook: "Circle đẹp hơn, nhưng 60 trang động và không tiếng Việt khiến mình đổi ý"
tension: chon_mot_mat_mot
sides: ["Circle đẹp hơn hẳn", "Kaneo có tiếng Việt, API thật và build ra file tĩnh"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Bộ dựng công ty một người chạy bằng đội agent AI đang cần một nền giao diện có sẵn, và Circle được đề xuất vì đẹp, gọn kiểu Linear. Kiểm tra kỹ mới thấy Circle dùng Next.js, khó đưa lên Cloudflare dạng file tĩnh và không có tiếng Việt, trong khi Kaneo web build ra file tĩnh và đã có vi-VN. Ai chọn nền UI cho sản phẩm cần đa ngôn ngữ hay deploy tĩnh nên xét hạ tầng và i18n trước, vẻ đẹp xét sau."
audience: dev chọn nền UI cho app cần đa ngôn ngữ hoặc deploy tĩnh
spine_context: "Bộ dựng công ty một người chạy bằng đội agent AI, nền Multica tự host, đang chọn nền giao diện có sẵn."
spine_context_lines: [profile]
spine_want: Tìm ứng cử viên nền UI có sẵn để so với gr8r và dựng giao diện cho dự án.
spine_want_lines: ["claude:0faf0bb2#L3204"]
spine_obstacle: "Circle đẹp hơn, nhưng dùng Next.js khó đưa lên Cloudflare dạng tĩnh và không có tiếng Việt."
spine_obstacle_lines: ["claude:0faf0bb2#L3290"]
spine_turn: "Tưởng Circle là nền phù hợp; hoá ra Kaneo web build ra file tĩnh và có sẵn vi-VN, còn Circle thì không."
spine_turn_lines: ["claude:0faf0bb2#L3271", "claude:0faf0bb2#L3290"]
spine_action: "Kiểm tra cấu hình Next.js của Circle và danh sách i18n của Kaneo, rồi đổi đề xuất sang Kaneo web."
spine_action_lines: ["claude:0faf0bb2#L3280", "claude:0faf0bb2#L3287"]
spine_outcome: "Đề xuất chốt là Kaneo web làm nền, mượn màn hình từ Circle."
spine_outcome_lines: ["claude:0faf0bb2#L3290"]
spine_takeaway: "Chọn nền UI theo chi phí đưa lên hạ tầng và độ phủ i18n trước, rồi mới xét độ đẹp."
spine_takeaway_lines: ["claude:0faf0bb2#L3290"]
completeness: 7
---

# Chọn nền UI: Circle đẹp hơn nhưng Kaneo có tiếng Việt và API thật, đổi khỏi đề xuất Circle

**Góc kể:** Bộ dựng công ty một người chạy bằng đội agent AI đang cần một nền giao diện có sẵn, và Circle được đề xuất vì đẹp, gọn kiểu Linear. Kiểm tra kỹ mới thấy Circle dùng Next.js, khó đưa lên Cloudflare dạng file tĩnh và không có tiếng Việt, trong khi Kaneo web build ra file tĩnh và đã có vi-VN. Ai chọn nền UI cho sản phẩm cần đa ngôn ngữ hay deploy tĩnh nên xét hạ tầng và i18n trước, vẻ đẹp xét sau.
**Bối cảnh:** Circle (MIT, khoảng 4,6k sao) được đề xuất làm nền UI vì phong cách gọn kiểu Linear.
**Chuyện gì xảy ra:** Kiểm tra cho thấy Circle dùng Next.js, khó xuất tĩnh lên Workers vì có khoảng 60 trang route động, và không có i18n. Kaneo web là SPA Vite, build ra file tĩnh, có vi-VN.json cùng 20 ngôn ngữ, và đã nối API qua Hono RPC. Mình đổi đề xuất sang Kaneo web và mượn màn hình từ Circle.
**Bài học:** Chọn nền UI theo chi phí đưa lên hạ tầng và độ phủ i18n trước, rồi mới xét độ đẹp.
**Artefact:** Bảng hai cột Circle và Kaneo.
