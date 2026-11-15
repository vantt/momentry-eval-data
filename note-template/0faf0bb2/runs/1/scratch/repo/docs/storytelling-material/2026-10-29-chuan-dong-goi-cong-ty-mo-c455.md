---
id: 2026-10-29-chuan-dong-goi-cong-ty-mo-c455
code: M-GCPW
aliases: [M-GCPW]
date: 2026-10-29
repo: repo
status: raw
signals: [khac]
signal_note: "Đây là kết quả đọc mã để chọn định dạng đóng gói: một chuẩn mở được kiểm chứng ở đúng một hệ thống, nên không đủ làm nền."
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3830", "claude:0faf0bb2#L3836", "claude:0faf0bb2#L3844", "claude:0faf0bb2#L3897", "claude:0faf0bb2#L3927"]
hook: "Cả chuẩn đóng gói công ty mở, chỉ một nền tảng làm được"
tension: khac
sides: ["Chuẩn mở thì ai cũng hiện thực được", "Chỉ Paperclip đóng gói được cả công ty, và vẫn thiếu workflow nhiều bước"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "fgOPC là bộ dựng công ty một người chạy bằng agent AI trên Multica, và nhóm đang tìm cách đóng gói cả một công ty OPC để deploy lại trên nhiều nền tảng. Lúc đầu có nhận định Multica dựng được workflow theo cột, nhưng đọc mã thì cột chỉ là danh sách trạng thái, không gắn người xử lý hay chỉ dẫn, và Multica chỉ đóng gói được skill. Ai chọn nền tảng cho quy trình nhiều bước nên kiểm tra điều này trước, đừng tin tên cột trên bảng."
audience: dev dựng quy trình cho agent AI trên nền tảng có sẵn
spine_context: fgOPC là bộ dựng công ty một người chạy bằng agent AI trên Multica; đang nghiên cứu cách đóng gói một công ty OPC để triển khai lại trên nhiều nền tảng.
spine_context_lines: [profile]
spine_want: Muốn đóng gói cả công ty OPC và deploy lại mà không tạo trùng.
spine_want_lines: ["claude:0faf0bb2#L3927"]
spine_obstacle: Chưa có hệ thống nào đóng gói được cả công ty OPC; Multica chỉ đóng gói được skill.
spine_obstacle_lines: ["claude:0faf0bb2#L3927"]
spine_turn: "Tưởng cột trên bảng Multica là workflow chạy được; hoá ra template chỉ là danh sách cột, không có người xử lý hay chỉ dẫn."
spine_turn_lines: ["claude:0faf0bb2#L3889", "claude:0faf0bb2#L3956"]
spine_action: "Đọc scripts/workflow.py và mã template, mô hình bước của Multica để trả lời câu hỏi cột có dựng được workflow không."
spine_action_lines: ["claude:0faf0bb2#L3889", "claude:0faf0bb2#L3976"]
spine_outcome: "Workflow, agent và squad của Multica không export được; CLI không có lệnh workflow."
spine_outcome_lines: ["claude:0faf0bb2#L3889"]
spine_takeaway: "Trước khi chọn nền tảng cho quy trình nhiều bước, kiểm tra cột có người xử lý và chỉ dẫn, đừng tin tên cột."
spine_takeaway_lines: ["claude:0faf0bb2#L3889"]
completeness: 7
---

# Chuẩn đóng gói công ty mở: chỉ Paperclip thực hiện được

**Góc kể:** fgOPC là bộ dựng công ty một người chạy bằng agent AI trên Multica, và nhóm đang tìm cách đóng gói cả một công ty OPC để deploy lại trên nhiều nền tảng. Lúc đầu có nhận định Multica dựng được workflow theo cột, nhưng đọc mã thì cột chỉ là danh sách trạng thái, không gắn người xử lý hay chỉ dẫn, và Multica chỉ đóng gói được skill. Ai chọn nền tảng cho quy trình nhiều bước nên kiểm tra điều này trước, đừng tin tên cột trên bảng.
**Bối cảnh:** Nghiên cứu cách đóng gói một công ty OPC (agent, team, project, task, skill) để triển khai lại trên nhiều nền tảng.
**Chuyện gì xảy ra:** Agent Companies v1 là chuẩn markdown mở, mở rộng SKILL.md, gồm COMPANY, TEAM, AGENTS, PROJECT và TASK. Chỉ Paperclip hiện thực chuẩn này: đóng gói và nhập được cả công ty, nhưng không có workflow nhiều bước. AICoworker đóng gói được một agent (.agent) kèm kiểm tra secret. Multica chỉ đóng gói được skill. Đề xuất là gói OPC = chuẩn trên + phần mở rộng WORKFLOW.md, deploy lại không tạo trùng.
**Bài học:** Khi chọn chuẩn đóng gói, đếm xem bao nhiêu hệ thống thực sự đọc và ghi được nó. Chuẩn chưa có ai hiện thực thì chưa đáng làm nền.
**Artefact:** Bảng ba cột (đóng được gì, thiếu gì) trong tài liệu nghiên cứu.
