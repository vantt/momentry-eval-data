---
id: 2026-11-02-chay-lai-mot-agent-da-dung
date: 2026-11-02
repo: repo
status: raw
signals: [khác]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3426", "claude:c4caee3c#L3442", "claude:c4caee3c#L3452", "claude:c4caee3c#L3464"]
hook: "Agent dừng im lặng giữa chừng, lead phát hiện nhờ không thấy tiến trình nào"
tension: none
sides: []
strength: 0
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy lại một agent đã dừng giữa chừng mà không báo

**Bối cảnh:** Agent review cuối (V14) dừng không báo lại, báo cáo vẫn là bản cũ.
**Chuyện gì xảy ra:** Lead kiểm tiến trình thấy không có gì chạy, gửi SendMessage yêu cầu tiếp tục; agent quay lại và báo lỗi npm 12 trong test. Việc đã xong vẫn được giữ trên nhánh.
**Bài học:** Kiểm tiến trình thật thay vì tin trạng thái agent; gửi lệnh tiếp tục có ngữ cảnh đầy đủ.
**Artefact:** Không cần.
