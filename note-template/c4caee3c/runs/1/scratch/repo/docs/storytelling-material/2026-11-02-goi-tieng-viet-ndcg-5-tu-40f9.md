---
id: 2026-11-02-goi-tieng-viet-ndcg-5-tu-40f9
code: M-5SVF
aliases: [M-5SVF]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L1114", "claude:c4caee3c#L1283", "claude:c4caee3c#L1640", "claude:c4caee3c#L1672", "claude:c4caee3c#L2187"]
hook: "Gói tiếng Việt đưa nDCG@5 từ 0,666 lên 0,932"
tension: it_ma_nhieu
sides: ["Từng module nhỏ cộng dồn", "Điểm tăng 0,27 mà không hạng mục nào tụt"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ tìm kiếm cục bộ cho ghi chú Obsidian đang thêm gói tiếng Việt, và các agent AI làm việc song song trên đó. Một agent đã cho rằng mục 3.5 của PRD sai, rồi ghi nhận định đó vào plan. Đọc lại thì PRD đúng: bỏ dấu được với chữ một dấu, còn chữ hai dấu và đ thì không. Ai dùng AI để kiểm tra tài liệu nên đọc lại nguồn trước khi tin một lỗi do AI báo."
audience: dev dùng AI agent để viết và kiểm tra tài liệu thiết kế
spine_context: "Một công cụ tìm kiếm cục bộ cho ghi chú Obsidian, đang thêm gói tiếng Việt do các agent AI làm song song."
spine_context_lines: [profile]
spine_turn: "Agent cho rằng mục 3.5 của PRD sai; đọc lại thì PRD đúng: bỏ dấu được với chữ một dấu, còn chữ hai dấu và đ thì không."
spine_turn_lines: ["claude:c4caee3c#L1264"]
spine_action: "Sửa ghi chú trong plan cho khớp với PRD, không sửa PRD."
spine_action_lines: ["claude:c4caee3c#L1264"]
spine_outcome: PRD giữ nguyên; nhận định sai đã được rút lại.
spine_outcome_lines: ["claude:c4caee3c#L1264"]
spine_takeaway: "Khi agent báo tài liệu sai, đọc lại đoạn gốc trước khi sửa theo nhận định đó."
spine_takeaway_lines: ["claude:c4caee3c#L1264"]
completeness: 5
---

# Gói tiếng Việt: nDCG@5 từ 0,666 lên 0,932 qua từng module

**Góc kể:** Một công cụ tìm kiếm cục bộ cho ghi chú Obsidian đang thêm gói tiếng Việt, và các agent AI làm việc song song trên đó. Một agent đã cho rằng mục 3.5 của PRD sai, rồi ghi nhận định đó vào plan. Đọc lại thì PRD đúng: bỏ dấu được với chữ một dấu, còn chữ hai dấu và đ thì không. Ai dùng AI để kiểm tra tài liệu nên đọc lại nguồn trước khi tin một lỗi do AI báo.
**Bối cảnh:** Gói tiếng Việt được chia thành nhiều module: chuẩn hoá, phục hồi dấu, alias, tách từ, từ điển.
**Chuyện gì xảy ra:** Baseline upstream nDCG@5 là 0,666. Module đầu tiên đưa lên 0,813. Alias đưa Hit@1 của hạng mục alias từ 0,60 lên 0,93. Tách từ đưa tổng lên 0,932, và vi-compound lên 1,00. Các hạng mục khác không tụt.
**Bài học:** Đo từng module riêng và ghi bảng tăng trưởng. Một con số tổng duy nhất che mất module nào thật sự có ích.
**Artefact:** Bảng nDCG@5 và Hit@5 theo từng giai đoạn (không chứa câu hỏi).
