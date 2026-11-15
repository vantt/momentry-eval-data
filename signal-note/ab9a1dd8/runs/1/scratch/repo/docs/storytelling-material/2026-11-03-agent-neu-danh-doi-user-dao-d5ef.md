---
id: 2026-11-03-agent-neu-danh-doi-user-dao-d5ef
code: M-R7EF
aliases: [M-R7EF]
date: 2026-11-03
repo: repo
status: raw
signals: [dao_quyet_dinh, khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L256", "claude:ab9a1dd8#L264", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L615"]
hook: "Agent khuyên chỉ in lệnh, user chọn tự cài hook thay"
tension: nguoi_dung_may_sai
sides: ["Agent đề xuất chỉ in và kiểm hook ở chế độ đọc", "User chọn init tự ghi hook, thêm 200-300 dòng code"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "Dự án momentry nhặt những chuyện đáng kể từ transcript phiên làm việc với coding agent, và đang chuẩn bị đóng gói để người khác cài dùng được."
spine_context_lines: [profile, "claude:ab9a1dd8#L236"]
spine_want: "Người mới, hoặc một agent chỉ đọc --help, đi từ con số 0 tới lần chạy đầu thành công."
spine_want_lines: ["claude:ab9a1dd8#L236"]
spine_obstacle: "Chưa có lệnh cài, cập nhật hay doctor; init --yes báo lỗi, và hook ghi cứng đường dẫn Node tuyệt đối."
spine_obstacle_lines: ["claude:ab9a1dd8#L232", "claude:ab9a1dd8#L236"]
spine_action: "Chọn để init tự cài hook và mẫu /bip, rồi lập plan triển khai qua ak-plan."
spine_action_lines: ["claude:ab9a1dd8#L340", "claude:ab9a1dd8#L342"]
spine_outcome: Plan đã được ghi vào thư mục plans; chưa có mã nào được triển khai.
spine_outcome_lines: ["claude:ab9a1dd8#L601"]
completeness: 5
---

# Agent nêu đánh đổi, user đảo quyết định PRD: hook tự cài thay vì chỉ in

**Bối cảnh:** PRD đã chốt công cụ chỉ in đoạn cấu hình hook để user tự dán vào settings. Agent được hỏi bốn điểm cần quyết.
**Chuyện gì xảy ra:** Agent đề xuất giữ chỉ in và thêm doctor kiểm hook ở chế độ chỉ đọc. User chọn tự cài: init tự ghi hook cho Claude và Codex, có --dry-run. Agent ước việc này khoảng 200 đến 300 dòng code cộng test, và phải sửa PRD ở mục 3.2, 6.4 và 12 cho khớp.
**Bài học:** Khi đảo một quyết định đã chốt trong PRD, liệt kê ngay mục PRD nào phải sửa cùng lúc để không còn hai nguồn sự thật.
**Artefact:** Bảng hai phương án chỉ in và tự cài kèm đánh đổi.
