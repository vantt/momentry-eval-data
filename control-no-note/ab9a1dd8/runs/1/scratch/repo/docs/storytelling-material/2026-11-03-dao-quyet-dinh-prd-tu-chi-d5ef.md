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
hook: "Chọn tự ghi settings.json, đảo PRD ở 3 mục"
tension: khac
sides: ["PRD ban đầu chỉ in đoạn hook cho người dùng", "Chủ dự án chọn tự cài, tốn 200 đến 300 dòng"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị để người dùng cài đặt chỉ bằng một lệnh. Người làm tin rằng in đoạn hook để người dùng tự dán là đủ và an toàn, vì công cụ không tự sửa file cấu hình chung của Claude Code. Một lượt rà soát cho thấy người mới, hay một agent chỉ đọc --help, không tự đi tới lần chạy đầu thành công, nên người làm đảo và chọn để công cụ tự cài. Ai làm công cụ cho dev đều có thể gặp bẫy này: an toàn trên giấy chưa chắc dễ dùng."
audience: "dev làm công cụ CLI hoặc dùng coding agent, muốn đóng gói công cụ cho người khác cài"
spine_context: "Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị để người dùng cài đặt chỉ bằng một lệnh."
spine_context_lines: [profile]
spine_want: "Người dùng cài và chạy được công cụ bằng một lệnh, theo ưu tiên trải nghiệm người dùng."
spine_want_lines: ["claude:ab9a1dd8#L42"]
spine_obstacle: "Bản hiện tại chỉ in đoạn hook để người dùng tự dán, chưa có cài đặt, doctor hay phiên bản; người mới không đi tới lần chạy đầu được."
spine_obstacle_lines: ["claude:ab9a1dd8#L236"]
spine_turn: "Tưởng in đoạn hook để người dùng tự dán là đủ và an toàn; hoá ra người mới không tự đi tới lần chạy đầu, nên người làm đảo và chọn để công cụ tự ghi hook."
spine_turn_lines: ["claude:ab9a1dd8#L236", "claude:ab9a1dd8#L256"]
spine_action: "Chọn tự cài hook và mẫu /bip, có --dry-run và sao lưu; chuyển mã thoát về chuẩn và ghi các đổi này vào checklist và plan."
spine_action_lines: ["claude:ab9a1dd8#L340", "claude:ab9a1dd8#L615", "claude:ab9a1dd8#L616"]
spine_outcome: Checklist và plan đã ghi quyết định đảo; trong phiên không thấy PRD được sửa hay code được viết.
spine_outcome_lines: ["claude:ab9a1dd8#L615", "claude:ab9a1dd8#L616"]
spine_takeaway: "Khi đảo một quyết định đã chốt, sửa tài liệu gốc trong cùng lượt; nếu không, tài liệu sẽ nói ngược với code."
spine_takeaway_lines: ["claude:ab9a1dd8#L300"]
completeness: 7
---

# Đảo quyết định PRD: từ 'chỉ in đoạn hook' sang 'công cụ tự ghi vào settings.json'

**Góc kể:** Dự án momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent, và đang chuẩn bị để người dùng cài đặt chỉ bằng một lệnh. Người làm tin rằng in đoạn hook để người dùng tự dán là đủ và an toàn, vì công cụ không tự sửa file cấu hình chung của Claude Code. Một lượt rà soát cho thấy người mới, hay một agent chỉ đọc --help, không tự đi tới lần chạy đầu thành công, nên người làm đảo và chọn để công cụ tự cài. Ai làm công cụ cho dev đều có thể gặp bẫy này: an toàn trên giấy chưa chắc dễ dùng.
**Bối cảnh:** PRD mục 3.2 và 6.4 ghi công cụ không bao giờ tự sửa ~/.claude/settings.json; người dùng tự dán đoạn in ra.
**Chuyện gì xảy ra:** Agent đưa hai phương án và ước việc tự cài khoảng 200 đến 300 dòng cộng test. Chủ dự án chọn tự cài, có --dry-run và sao lưu trước khi ghi. Phương án chỉ in được giữ lại dưới dạng doctor kiểm hook hỏng. Quyết định này đảo PRD ở 3 mục và được ghi vào plan.
**Bài học:** Khi một quyết định đã chốt trong PRD bị đảo, sửa PRD ngay trong cùng lượt. Nếu không, tài liệu sẽ nói ngược với code.
**Artefact:** Bảng hai cột đánh đổi của phương án in và phương án tự cài.
