---
id: 2026-11-03-agent-moi-vuong-vi-goi-y-d5ef
code: M-AEGN
aliases: [M-AEGN]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968"]
hook: "Lỗi chỉ cho cách sửa bằng lời, agent mới chẳng biết gõ gì"
tension: giup_ma_hai
sides: ["Lỗi privacy có kèm gợi ý sửa", "Gợi ý là câu văn, không phải lệnh chạy được"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang thử xem một agent mới có tự dùng được CLI của nó không. Ở vòng đầu, lỗi privacy chỉ nói cách sửa bằng một câu tiếng Việt, nên agent không có lệnh nào để chạy và vòng test mất 2 vòng mới hội tụ. Sau khi thêm lệnh privacy-add và đưa lệnh chạy được vào thông báo lỗi, vòng test hội tụ ngay vòng đầu. Ai làm CLI cho agent nên để ý: câu gợi ý dễ hiểu với người đọc có thể vô dụng với máy."
audience: dev làm CLI cho agent và người build in public
spine_context: "Momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang thử xem một agent mới có tự dùng được CLI của nó không."
spine_context_lines: [profile, "claude:ab9a1dd8#L1549"]
spine_want: Muốn agent mới đưa doctor về trạng thái ok chỉ bằng --help và --json.
spine_want_lines: ["claude:ab9a1dd8#L1549"]
spine_obstacle: "Lỗi privacy chỉ báo cách sửa bằng một câu, không có lệnh nào để chạy."
spine_obstacle_lines: ["claude:ab9a1dd8#L1942"]
spine_turn: Tưởng gợi ý bằng câu văn là đủ; hoá ra agent mới cần đúng một lệnh chạy được.
spine_turn_lines: ["claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960"]
spine_action: "Thêm lệnh privacy-add nhận tên cần chặn, và đưa lệnh chạy được vào trường fix của lỗi."
spine_action_lines: ["claude:ab9a1dd8#L1953"]
spine_outcome: "Vòng agent-native hội tụ ngay vòng đầu, trước đó mất 2 vòng."
spine_outcome_lines: ["claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960"]
spine_takeaway: Mỗi thông báo lỗi nên kèm đúng một lệnh chạy được; test bằng agent mới để thấy gợi ý nào vô dụng.
spine_takeaway_lines: ["claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960"]
completeness: 7
---

# Agent mới vướng vì gợi ý sửa lỗi là một câu văn, không phải lệnh chạy được

**Góc kể:** Momentry nhặt chuyện đáng kể từ phiên làm việc với coding agent, và người làm đang thử xem một agent mới có tự dùng được CLI của nó không. Ở vòng đầu, lỗi privacy chỉ nói cách sửa bằng một câu tiếng Việt, nên agent không có lệnh nào để chạy và vòng test mất 2 vòng mới hội tụ. Sau khi thêm lệnh privacy-add và đưa lệnh chạy được vào thông báo lỗi, vòng test hội tụ ngay vòng đầu. Ai làm CLI cho agent nên để ý: câu gợi ý dễ hiểu với người đọc có thể vô dụng với máy.
**Bối cảnh:** Vòng test agent-native: một agent mới chỉ đọc --help và --json, phải tự cài và đưa doctor về ok.
**Chuyện gì xảy ra:** Ở vòng đầu, lỗi privacy báo cách sửa bằng một câu tiếng Việt, không có lệnh để chạy. Vòng hội tụ trước đó mất 2 vòng. Agent thêm 'config privacy-add' với đối số là tên cần chặn. Sau đó vòng test hội tụ ngay ở vòng đầu.
**Bài học:** Mỗi thông báo lỗi nên kèm đúng một lệnh chạy được. Test bằng một agent mới là cách thấy câu gợi ý nào vô dụng.
**Artefact:** Đầu ra lỗi privacy trước và sau khi sửa. Che tên trong ví dụ.
