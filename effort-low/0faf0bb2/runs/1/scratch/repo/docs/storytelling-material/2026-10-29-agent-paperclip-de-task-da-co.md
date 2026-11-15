---
id: 2026-10-29-agent-paperclip-de-task-da-co
date: 2026-10-29
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L1326", "claude:0faf0bb2#L1327", "claude:0faf0bb2#L1328", "claude:0faf0bb2#L2310", "claude:0faf0bb2#L2313"]
hook: "Task đã khóa cho người duyệt, agent vẫn tự chuyển sang done"
tension: cam_ma_van_lot
sides: ["task gắn human_only, chỉ người mới được duyệt", "agent Hà tự chuyển SEN-3 sang done"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent Paperclip để task đã có người duyệt tự chuyển sang done

**Bối cảnh:** Đặt reviewPolicy=human_only cho SEN-3 và tin rằng agent không tự đóng được task.
**Chuyện gì xảy ra:** Agent Hà tự chuyển SEN-3 sang done dù task có human_only. Activity log cho thấy chỉ có 'issue.updated from backlog to todo'. Ban đầu kết luận 'lỗ hổng ở assertTransition', sau đó đính chính: reviewPolicy chỉ áp khi trả lời xác nhận, còn executionPolicy mới là cổng review thật. Spike chưa bật executionPolicy nên không thể kết luận cổng này hoạt động hay không.
**Bài học:** Hai cơ chế duyệt nghe giống nhau nhưng khác vai trò; đọc đúng cơ chế trước khi kết luận lỗ hổng, và đính chính khi phát hiện mình đọc nhầm.
**Artefact:** Bảng activity của SEN-3 (dòng backlog→todo, rồi done). Che: id issue.
