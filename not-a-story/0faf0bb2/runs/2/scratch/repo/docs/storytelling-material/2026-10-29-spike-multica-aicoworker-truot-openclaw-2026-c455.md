---
id: 2026-10-29-spike-multica-aicoworker-truot-openclaw-2026-c455
code: M-A8R9
aliases: [M-A8R9]
date: 2026-10-29
repo: repo
status: raw
signals: [dao_quyet_dinh, so_truoc_so_sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
hook: "Phiên bản 2026.3.13 thấp hơn mức tối thiểu 2026.5.5, 4 tiêu chí chưa kiểm được"
tension: nho_ma_to
sides: ["Cấu hình đúng, chỉ cần chạy thử", "Số phiên bản quá thấp chặn ngay từ lượt đầu, khai man bằng shim cũng không qua"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một bộ dựng công ty một người bằng AI agent, nền Multica, và đợt này đang cố để Multica điều khiển được agent của AICoworker qua CLI openclaw. Người làm đã thử khai man phiên bản CLI bằng một lớp shim, tin rằng như vậy sẽ qua được kiểm tra. Hoá ra OpenClaw 2026.3.13 thấp hơn mức tối thiểu 2026.5.5 và việc khai man không qua được, nên spike trượt ở chính điểm này. Ai đang tích hợp hai công cụ qua CLI nên ghim và kiểm phiên bản trước khi viết code nối."
audience: dev tích hợp công cụ AI qua CLI
spine_context: "Bộ dựng công ty một người bằng AI agent, nền Multica; đang spike nối Multica với AICoworker."
spine_context_lines: [profile, "claude:0faf0bb2#L2772"]
spine_want: Muốn Multica điều khiển được agent của AICoworker qua CLI openclaw.
spine_want_lines: ["claude:0faf0bb2#L3150"]
spine_obstacle: "Lượt chạy đầu bị từ chối: OpenClaw 2026.3.13 dưới bản tối thiểu 2026.5.5."
spine_obstacle_lines: ["claude:0faf0bb2#L3041"]
spine_turn: "Tưởng khai man phiên bản bằng shim là qua được kiểm tra; hoá ra phiên bản và lỗi include chặn lại, nên khai man không qua."
spine_turn_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
spine_action: Khai man phiên bản bằng shim và gọi lại; sau đó dọn Multica và giữ agent mai.
spine_action_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3160"]
spine_outcome: Spike trượt; 4 tiêu chí chưa kiểm được; phía AICoworker chạy được khi gọi thẳng openclaw.
spine_outcome_lines: ["claude:0faf0bb2#L3150"]
spine_takeaway: Ghim và kiểm phiên bản CLI của bên được điều khiển trước khi tích hợp; khai man chỉ làm lỗi lộ muộn hơn.
spine_takeaway_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
completeness: 7
---

# Spike Multica + AICoworker trượt: OpenClaw 2026.3.13 dưới phiên bản tối thiểu 2026.5.5 của Multica

**Góc kể:** Dự án là một bộ dựng công ty một người bằng AI agent, nền Multica, và đợt này đang cố để Multica điều khiển được agent của AICoworker qua CLI openclaw. Người làm đã thử khai man phiên bản CLI bằng một lớp shim, tin rằng như vậy sẽ qua được kiểm tra. Hoá ra OpenClaw 2026.3.13 thấp hơn mức tối thiểu 2026.5.5 và việc khai man không qua được, nên spike trượt ở chính điểm này. Ai đang tích hợp hai công cụ qua CLI nên ghim và kiểm phiên bản trước khi viết code nối.
**Bối cảnh:** Mục tiêu: để Multica điều khiển agent của AICoworker qua CLI openclaw. Spike đã chạy được phía Multica và phía AICoworker, nhưng không nối được.
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối: 'openclaw 2026.3.13 is below the minimum supported version 2026.5.5'. Thử khai man phiên bản bằng shim thì CLI báo 'Include path escapes config directory' và thoát không có output. Kết luận: 4 tiêu chí chưa kiểm được, nguyên nhân là phiên bản chứ không phải cấu hình. Sau đó dọn sạch stack, giữ lại agent mai.
**Bài học:** Ghim phiên bản CLI của bên được điều khiển là bước đầu của mọi tích hợp; khai man phiên bản chỉ làm lỗi lộ ra muộn hơn.
**Artefact:** Bảng ba đường đi tiếp (chờ nâng cấp, vá daemon, dùng OpenClaw độc lập) trong docs/spikes/2026-10-29-multica-spike.md.
**Góc người ngoài:** cách làm phổ biến là Thử tích hợp rồi báo 'chưa chạy được' hoặc cố sửa cho đến khi chạy; ít khi chốt tiêu chí trước rồi chấp nhận trượt như dữ liệu; ở đây khác ở Người đọc sẽ hỏi vì sao trượt Multica + AICoworker lại được ghi nhận rõ thay vì bỏ qua, và vì sao đổi sang Multica + Claude Code ngay sau đó không bị coi là đổi ý.
