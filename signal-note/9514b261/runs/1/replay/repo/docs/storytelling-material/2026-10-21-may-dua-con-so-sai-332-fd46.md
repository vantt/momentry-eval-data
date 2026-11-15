---
id: 2026-10-21-may-dua-con-so-sai-332-fd46
code: M-J53X
aliases: [M-J53X]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L1432", "claude:9514b261#L1447", "claude:9514b261#L1448", "claude:9514b261#L1457"]
hook: "Báo cáo ghi 332/332 vẫn tạm, đếm lại thì là 332 trên 479"
tension: tuong_ma_hoa_ra
sides: ["Báo cáo nói toàn bộ 332 doc đã migrate vẫn provisional", "Đếm lại: 479 doc, 332 provisional, 147 active"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Forgent (fgOS) là nền tảng để xây ứng dụng agent, và người làm đang định xây một 'Knowledge and Documentation Engine' để quản lý tài liệu. Họ tưởng đây là phần mới, nhưng khi quét lịch sử và danh sách việc đã có thì phần lớn đã trùng với Knowledge Registry: phần thật sự mới chỉ là đồ thị quan hệ, supersession cấp điều khoản và vocabulary loại thẩm quyền. Ai đang lên kế hoạch một hệ thống mới nên quét những thứ đã có trước khi đặt tên cho nó."
audience: dev dùng AI để lên kế hoạch hệ thống mới
spine_context: Forgent (fgOS) là nền tảng để xây ứng dụng agent; người làm đang cân nhắc một 'Knowledge and Documentation Engine' (KDE) để quản lý tài liệu.
spine_context_lines: [profile, "claude:9514b261#L1325"]
spine_want: Muốn biết KDE có trùng với thứ đã có không trước khi xây tiếp.
spine_want_lines: ["claude:9514b261#L1325"]
spine_obstacle: "Phần đã có nằm rải ở plans, reports, work items và history, và Knowledge Registry chỉ phủ tài liệu end-user."
spine_obstacle_lines: ["claude:9514b261#L1325", "claude:9514b261#L1467"]
spine_turn: "Tưởng KDE là phần mới; hoá ra phần lớn đã có trong Knowledge Registry, phần thật sự mới chỉ là đồ thị có kiểu, supersession cấp điều khoản và vocabulary loại thẩm quyền."
spine_turn_lines: ["claude:9514b261#L1253", "claude:9514b261#L1427"]
spine_action: "Dựng ba agent quét plans/reports, docs/history và journals, work items cùng mã, rồi gộp kết quả thành báo cáo."
spine_action_lines: ["claude:9514b261#L1325", "claude:9514b261#L1467"]
spine_outcome: "KDE chồng nặng với Knowledge Registry (tsk-28x), lớp decision (tsk-1lv) và enduser-docs-index; registry phủ khoảng 15% trong 3146 file .md của docs/."
spine_outcome_lines: ["claude:9514b261#L1427", "claude:9514b261#L1467"]
spine_takeaway: "Trước khi đặt tên và xây một hệ thống mới, quét lịch sử và danh sách việc đã có, vì rất dễ xây lại thứ đã tồn tại."
spine_takeaway_lines: ["claude:9514b261#L1253"]
completeness: 7
---

# Máy đưa con số sai ('332/332 provisional'), người đếm lại thì ra 332 trên 147

**Góc kể:** Forgent (fgOS) là nền tảng để xây ứng dụng agent, và người làm đang định xây một 'Knowledge and Documentation Engine' để quản lý tài liệu. Họ tưởng đây là phần mới, nhưng khi quét lịch sử và danh sách việc đã có thì phần lớn đã trùng với Knowledge Registry: phần thật sự mới chỉ là đồ thị quan hệ, supersession cấp điều khoản và vocabulary loại thẩm quyền. Ai đang lên kế hoạch một hệ thống mới nên quét những thứ đã có trước khi đặt tên cho nó.
**Bối cảnh:** Một researcher agent báo số liệu trong báo cáo. Agent chính dùng báo cáo đó để gộp kết luận cho owner.
**Chuyện gì xảy ra:** Báo cáo ghi '332/332 doc đã migrate vẫn provisional'. Agent chính đếm lại trong doc-registry.json và chỉ ra 479 doc, 332 provisional, 147 active. Con số tổng đúng, nhưng cách diễn đạt của báo cáo không khớp dữ liệu.
**Bài học:** Với báo cáo do agent viết, đếm lại con số trước khi đưa cho người ra quyết định; mỗi con số là một lần kiểm riêng.
**Artefact:** Hai dòng so sánh: 'báo cáo ghi 332/332' và 'đếm lại được 332 provisional + 147 active = 479'.
**Góc người ngoài:** cách làm phổ biến là Nhận báo cáo của subagent rồi chuyển nguyên văn cho người dùng, hoặc tin con số và kết luận của AI khác vì nó nghe hợp lý; ở đây khác ở Agent coi mỗi số là thứ phải đo lại. Nó ghi rõ phần nào đã kiểm và phần nào chỉ là suy luận, nên người đọc biết con số nào đáng tin. Người đọc sẽ hỏi vì sao không tin ngay báo cáo của agent con.
