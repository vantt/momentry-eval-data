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
hook: "Gợi ý sửa lỗi là một câu văn, agent mới không biết gõ gì"
tension: giup_ma_hai
sides: ["Lỗi privacy có báo cách sửa bằng tiếng Việt", "Không có lệnh chạy được nên vòng đầu hội tụ mất 2 vòng, thêm lệnh thì xong ngay vòng đầu"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: none
spine_context: "momentry nhặt những chuyện đáng kể từ phiên làm việc với coding agent. Đang làm vòng test agent-native cho CLI: một agent mới chỉ đọc --help và --json, phải tự đưa doctor về ok."
spine_context_lines: [profile]
spine_obstacle: Vòng agent-native mất 2 vòng mới hội tụ.
spine_obstacle_lines: ["claude:ab9a1dd8#L1557"]
spine_action: Sửa đường trả lỗi để trường fix lấy gợi ý từ kết quả lệnh.
spine_action_lines: ["claude:ab9a1dd8#L1953"]
spine_outcome: Vòng agent-native hội tụ ngay vòng đầu với lệnh privacy-add.
spine_outcome_lines: ["claude:ab9a1dd8#L1960"]
spine_takeaway: Mỗi thông báo lỗi nên kèm đúng một lệnh chạy được; gợi ý bằng câu văn không đủ để agent mới tự sửa.
spine_takeaway_lines: ["claude:ab9a1dd8#L1942", "claude:ab9a1dd8#L1960"]
completeness: 5
---

# Agent mới vướng vì gợi ý sửa lỗi là một câu văn, không phải lệnh chạy được

**Bối cảnh:** Vòng test agent-native: một agent mới chỉ đọc --help và --json, phải tự cài và đưa doctor về ok.
**Chuyện gì xảy ra:** Ở vòng đầu, lỗi privacy báo cách sửa bằng một câu tiếng Việt, không có lệnh để chạy. Vòng hội tụ trước đó mất 2 vòng. Agent thêm 'config privacy-add' với đối số là tên cần chặn. Sau đó vòng test hội tụ ngay ở vòng đầu.
**Bài học:** Mỗi thông báo lỗi nên kèm đúng một lệnh chạy được. Test bằng một agent mới là cách thấy câu gợi ý nào vô dụng.
**Artefact:** Đầu ra lỗi privacy trước và sau khi sửa. Che tên trong ví dụ.
