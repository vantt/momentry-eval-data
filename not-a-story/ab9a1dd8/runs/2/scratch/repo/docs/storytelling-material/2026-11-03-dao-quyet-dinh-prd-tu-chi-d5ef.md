---
id: 2026-11-03-dao-quyet-dinh-prd-tu-chi-d5ef
code: M-W7CX
aliases: [M-W7CX]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:ab9a1dd8#L251", "claude:ab9a1dd8#L256", "claude:ab9a1dd8#L300", "claude:ab9a1dd8#L340", "claude:ab9a1dd8#L615"]
hook: "Tự ghi settings.json tốn 200-300 dòng, nhưng chủ dự án vẫn chọn, đảo PRD 3 mục"
tension: chon_mot_mat_mot
sides: ["Chỉ in đoạn hook thì rẻ và an toàn", "Tự cài tốn 200-300 dòng nhưng người dùng đỡ khổ"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang cố đưa nó tới tay người mới chỉ cần một lệnh là chạy được. Ban đầu thiết kế để công cụ chỉ in ra đoạn hook rồi người dùng tự dán vào cấu hình, vì nghĩ vậy là an toàn. Kiểm toán cho thấy cách đó dễ hỏng im lặng khi đổi phiên bản Node hay chuyển thư mục, nên người làm chọn để công cụ tự cài và đảo luôn quyết định đã chốt trong PRD. Ai đóng gói công cụ CLI cho dev đều gặp đúng bài toán này: đừng bắt người dùng tự sửa file cấu hình chung rồi tin rằng nó vẫn chạy."
audience: dev đóng gói công cụ CLI cho người dùng
spine_context: "momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị đóng gói để người mới cài và chạy được."
spine_context_lines: [profile]
spine_want: Người mới đi từ con số 0 tới lần chạy đầu thành công mà không cần đọc code.
spine_want_lines: ["claude:ab9a1dd8#L42", "claude:ab9a1dd8#L236"]
spine_obstacle: "Phần phân phối gần như chưa có; `init` lỗi với cờ `--yes`, và `list`/`check` báo thiếu hộp ngay sau quick start."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_turn: "Tưởng in đoạn hook cho người dùng tự dán là đủ an toàn; hoá ra hook có thể hỏng im lặng khi đổi Node hoặc chuyển thư mục, và không có gì báo."
spine_turn_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L256"]
spine_action: "Đề xuất giữ chế độ chỉ in và thêm `doctor`; người làm chọn tự cài hook, lập plan đóng gói và ghi việc đảo quyết định PRD."
spine_action_lines: ["claude:ab9a1dd8#L340", "claude:ab9a1dd8#L342", "claude:ab9a1dd8#L615"]
spine_outcome: "Plan đóng gói và checklist đã được ghi; quyết định PRD mục 3.2, 6.4, 12 được ghi là đã đảo."
spine_outcome_lines: ["claude:ab9a1dd8#L601", "claude:ab9a1dd8#L615"]
spine_takeaway: "Khi đảo một quyết định đã chốt trong PRD, sửa PRD ngay trong cùng lượt để tài liệu không nói ngược với code."
spine_takeaway_lines: ["claude:ab9a1dd8#L300", "claude:ab9a1dd8#L615"]
completeness: 7
---

# Đảo quyết định PRD: từ 'chỉ in đoạn hook' sang 'công cụ tự ghi vào settings.json'

**Góc kể:** Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang cố đưa nó tới tay người mới chỉ cần một lệnh là chạy được. Ban đầu thiết kế để công cụ chỉ in ra đoạn hook rồi người dùng tự dán vào cấu hình, vì nghĩ vậy là an toàn. Kiểm toán cho thấy cách đó dễ hỏng im lặng khi đổi phiên bản Node hay chuyển thư mục, nên người làm chọn để công cụ tự cài và đảo luôn quyết định đã chốt trong PRD. Ai đóng gói công cụ CLI cho dev đều gặp đúng bài toán này: đừng bắt người dùng tự sửa file cấu hình chung rồi tin rằng nó vẫn chạy.
**Bối cảnh:** PRD mục 3.2 và 6.4 ghi công cụ không bao giờ tự sửa ~/.claude/settings.json; người dùng tự dán đoạn in ra.
**Chuyện gì xảy ra:** Agent đưa hai phương án và ước việc tự cài khoảng 200 đến 300 dòng cộng test. Chủ dự án chọn tự cài, có --dry-run và sao lưu trước khi ghi. Phương án chỉ in được giữ lại dưới dạng doctor kiểm hook hỏng. Quyết định này đảo PRD ở 3 mục và được ghi vào plan.
**Bài học:** Khi một quyết định đã chốt trong PRD bị đảo, sửa PRD ngay trong cùng lượt. Nếu không, tài liệu sẽ nói ngược với code.
**Artefact:** Bảng hai cột đánh đổi của phương án in và phương án tự cài.
