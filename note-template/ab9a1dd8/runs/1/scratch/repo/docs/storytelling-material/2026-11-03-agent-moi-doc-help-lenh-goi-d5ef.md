---
id: 2026-11-03-agent-moi-doc-help-lenh-goi-d5ef
code: M-X6G7
aliases: [M-X6G7]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L1550", "claude:ab9a1dd8#L1960", "claude:ab9a1dd8#L1968", "claude:ab9a1dd8#L2230"]
hook: "Một lệnh gợi ý không chạy được làm agent mới vướng ngay vòng đầu"
tension: giup_ma_hai
sides: ["Help gợi ý cách sửa nguồn chặn", "Gợi ý chỉ là câu mô tả, agent không chạy được"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "momentry là công cụ đọc transcript các phiên làm việc với coding agent, đang làm bước cài đặt một lệnh cho người mới. Gợi ý sửa nguồn chặn riêng tư trông như lệnh chạy được, nhưng thực ra chỉ là câu văn, nên agent mới vướng ngay vòng thử đầu. Sau khi thêm lệnh privacy-add nhận tên làm đối số, vòng thử hội tụ ngay lần đầu, từ hai vòng xuống một. Ai viết CLI cho agent nên để ý: gợi ý lỗi phải là lệnh chạy được, và thử bằng agent mới là cách kiểm."
audience: dev viết CLI cho agent hoặc tài liệu cài đặt
spine_context: "momentry là công cụ đọc transcript các phiên làm việc với coding agent, đang làm bước cài đặt một lệnh cho người mới."
spine_context_lines: [profile, "claude:ab9a1dd8#L2230"]
spine_want: Một agent không có ngữ cảnh chỉ dùng --help và --json để đưa doctor tới trạng thái ok.
spine_want_lines: ["claude:ab9a1dd8#L2230"]
spine_obstacle: "Gợi ý sửa nguồn chặn riêng tư là câu văn, không chạy được, nên agent vướng ở vòng thử đầu."
spine_obstacle_lines: ["claude:ab9a1dd8#L2230"]
spine_turn: "Gợi ý lỗi trông như lệnh chạy được, hoá ra chỉ là câu mô tả."
spine_turn_lines: ["claude:ab9a1dd8#L1942", "claude:ab9a1dd8#L2230"]
spine_action: "Thêm lệnh config privacy-add nhận tên làm đối số, rồi chạy lại vòng thử."
spine_action_lines: ["claude:ab9a1dd8#L1953"]
spine_outcome: "Vòng agent hội tụ ngay vòng đầu, từ hai vòng xuống một."
spine_outcome_lines: ["claude:ab9a1dd8#L1557", "claude:ab9a1dd8#L1960"]
spine_takeaway: Gợi ý lỗi phải là lệnh chạy được; kiểm bằng cách cho một agent mới làm theo tài liệu.
spine_takeaway_lines: ["claude:ab9a1dd8#L1545", "claude:ab9a1dd8#L2230"]
completeness: 7
---

# Agent mới đọc --help: lệnh gợi ý phải chạy được, vòng thử hội tụ từ hai xuống một

**Góc kể:** momentry là công cụ đọc transcript các phiên làm việc với coding agent, đang làm bước cài đặt một lệnh cho người mới. Gợi ý sửa nguồn chặn riêng tư trông như lệnh chạy được, nhưng thực ra chỉ là câu văn, nên agent mới vướng ngay vòng thử đầu. Sau khi thêm lệnh privacy-add nhận tên làm đối số, vòng thử hội tụ ngay lần đầu, từ hai vòng xuống một. Ai viết CLI cho agent nên để ý: gợi ý lỗi phải là lệnh chạy được, và thử bằng agent mới là cách kiểm.
**Bối cảnh:** Một agent không có ngữ cảnh được giao cài momentry và đưa doctor tới trạng thái ok chỉ bằng --help và --json.
**Chuyện gì xảy ra:** Vòng thử đầu, agent vướng vì gợi ý sửa nguồn chặn là một câu mô tả như sửa bằng config set, không chạy được. Agent thêm lệnh config privacy-add nhận tên làm đối số. Sau đó vòng thử hội tụ ngay ở lần đầu, từ hai vòng xuống một vòng.
**Bài học:** Gợi ý lỗi phải là lệnh chạy được, không phải câu mô tả. Cách kiểm là cho một agent không có ngữ cảnh làm theo tài liệu.
**Artefact:** Output lỗi trước và sau khi sửa, che tên người dùng nếu có.
**Góc người ngoài:** cách làm phổ biến là Thông báo lỗi chỉ nói 'thiếu cấu hình', và agent phải đoán hoặc đọc README dài; ở đây khác ở Thiết kế CLI để máy đọc được và tự sửa lỗi. Người đọc sẽ hỏi làm sao kiểm 'agent có tự làm được không' bằng một vòng thử tự động.
