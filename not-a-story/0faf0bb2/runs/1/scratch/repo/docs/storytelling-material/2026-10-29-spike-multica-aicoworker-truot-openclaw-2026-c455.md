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
hook: "Thử khai man phiên bản để qua mặt, CLI vẫn thoát im lặng"
tension: cam_ma_van_lot
sides: ["Giả phiên bản 2026.5.5 bằng shim để qua kiểm tra", "CLI báo lỗi đường dẫn và thoát không output, 4 tiêu chí chưa kiểm được"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là bộ dựng công ty một người chạy bằng AI agent, nền Multica, và người làm đang cố cho Multica điều khiển agent của AICoworker qua CLI openclaw. Ban đầu họ tưởng chỉ cần sửa chuỗi phiên bản là chạy được, nên khai man openclaw lên 2026.5.5 bằng một wrapper. Hoá ra CLI còn lỗi 'Include path escapes config directory' và thoát không in gì, tức phiên bản chỉ là một trong ba chỗ lệch. Người làm ghi nhận là trượt chứ không che đi, và đây là bài học đáng nghe với ai tích hợp công cụ bên thứ ba: kiểm phiên bản thật trước, khai man chỉ làm lỗi lộ muộn hơn."
audience: dev tích hợp công cụ AI bên thứ ba
spine_context: "Dự án là bộ dựng công ty một người vận hành bằng AI agent, nền Multica; đang spike cho Multica điều khiển agent của AICoworker qua CLI openclaw."
spine_context_lines: [profile, "claude:0faf0bb2#L2772"]
spine_want: Muốn Multica điều khiển được agent của AICoworker qua CLI openclaw.
spine_want_lines: ["claude:0faf0bb2#L2772"]
spine_obstacle: Multica v0.7.1 từ chối vì openclaw 2026.3.13 thấp hơn bản tối thiểu 2026.5.5.
spine_obstacle_lines: ["claude:0faf0bb2#L3041"]
spine_turn: "Tưởng chỉ cần khai man phiên bản là chạy được; hoá ra CLI còn lỗi include path và định dạng output, phiên bản chỉ là một trong ba chỗ lệch."
spine_turn_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
spine_action: Chèn shim khai phiên bản 2026.5.5 vào wrapper openclaw rồi chạy lại issue.
spine_action_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3065"]
spine_outcome: "CLI báo 'Include path escapes config directory' và thoát không output; 4 tiêu chí chưa kiểm được, spike ghi nhận trượt."
spine_outcome_lines: ["claude:0faf0bb2#L3150"]
spine_takeaway: Kiểm phiên bản thật của bên được điều khiển trước khi tích hợp; khai man phiên bản chỉ làm lỗi lộ muộn hơn.
spine_takeaway_lines: ["claude:0faf0bb2#L3061", "claude:0faf0bb2#L3150"]
completeness: 7
---

# Spike Multica + AICoworker trượt: OpenClaw 2026.3.13 dưới phiên bản tối thiểu 2026.5.5 của Multica

**Góc kể:** Dự án là bộ dựng công ty một người chạy bằng AI agent, nền Multica, và người làm đang cố cho Multica điều khiển agent của AICoworker qua CLI openclaw. Ban đầu họ tưởng chỉ cần sửa chuỗi phiên bản là chạy được, nên khai man openclaw lên 2026.5.5 bằng một wrapper. Hoá ra CLI còn lỗi 'Include path escapes config directory' và thoát không in gì, tức phiên bản chỉ là một trong ba chỗ lệch. Người làm ghi nhận là trượt chứ không che đi, và đây là bài học đáng nghe với ai tích hợp công cụ bên thứ ba: kiểm phiên bản thật trước, khai man chỉ làm lỗi lộ muộn hơn.
**Bối cảnh:** Mục tiêu: để Multica điều khiển agent của AICoworker qua CLI openclaw. Spike đã chạy được phía Multica và phía AICoworker, nhưng không nối được.
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối: 'openclaw 2026.3.13 is below the minimum supported version 2026.5.5'. Thử khai man phiên bản bằng shim thì CLI báo 'Include path escapes config directory' và thoát không có output. Kết luận: 4 tiêu chí chưa kiểm được, nguyên nhân là phiên bản chứ không phải cấu hình. Sau đó dọn sạch stack, giữ lại agent mai.
**Bài học:** Ghim phiên bản CLI của bên được điều khiển là bước đầu của mọi tích hợp; khai man phiên bản chỉ làm lỗi lộ ra muộn hơn.
**Artefact:** Bảng ba đường đi tiếp (chờ nâng cấp, vá daemon, dùng OpenClaw độc lập) trong docs/spikes/2026-10-29-multica-spike.md.
**Góc người ngoài:** cách làm phổ biến là Thử tích hợp rồi báo 'chưa chạy được' hoặc cố sửa cho đến khi chạy; ít khi chốt tiêu chí trước rồi chấp nhận trượt như dữ liệu; ở đây khác ở Người đọc sẽ hỏi vì sao trượt Multica + AICoworker lại được ghi nhận rõ thay vì bỏ qua, và vì sao đổi sang Multica + Claude Code ngay sau đó không bị coi là đổi ý.
