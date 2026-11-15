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
hook: "Agent bị từ chối vì phiên bản 2026.3.13 thấp hơn mức tối thiểu 2026.5.5"
tension: cam_ma_van_lot
sides: ["Thử khai man phiên bản bằng shim để qua cổng kiểm tra", "CLI vẫn báo lỗi và thoát, 4 tiêu chí chưa kiểm được"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Spike Multica + AICoworker trượt: OpenClaw 2026.3.13 dưới phiên bản tối thiểu 2026.5.5 của Multica

**Bối cảnh:** Mục tiêu: để Multica điều khiển agent của AICoworker qua CLI openclaw. Spike đã chạy được phía Multica và phía AICoworker, nhưng không nối được.
**Chuyện gì xảy ra:** Lượt chạy đầu bị từ chối: 'openclaw 2026.3.13 is below the minimum supported version 2026.5.5'. Thử khai man phiên bản bằng shim thì CLI báo 'Include path escapes config directory' và thoát không có output. Kết luận: 4 tiêu chí chưa kiểm được, nguyên nhân là phiên bản chứ không phải cấu hình. Sau đó dọn sạch stack, giữ lại agent mai.
**Bài học:** Ghim phiên bản CLI của bên được điều khiển là bước đầu của mọi tích hợp; khai man phiên bản chỉ làm lỗi lộ ra muộn hơn.
**Artefact:** Bảng ba đường đi tiếp (chờ nâng cấp, vá daemon, dùng OpenClaw độc lập) trong docs/spikes/2026-10-29-multica-spike.md.
**Góc người ngoài:** cách làm phổ biến là Thử tích hợp rồi báo 'chưa chạy được' hoặc cố sửa cho đến khi chạy; ít khi chốt tiêu chí trước rồi chấp nhận trượt như dữ liệu; ở đây khác ở Người đọc sẽ hỏi vì sao trượt Multica + AICoworker lại được ghi nhận rõ thay vì bỏ qua, và vì sao đổi sang Multica + Claude Code ngay sau đó không bị coi là đổi ý.
