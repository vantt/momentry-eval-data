---
id: 2026-11-02-ranh-gioi-fork-va-repo-du-40f9
code: M-0AB1
aliases: [M-0AB1]
date: 2026-11-02
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, nguoi_duyet_may_soan]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2238", "claude:c4caee3c#L2320", "claude:c4caee3c#L2372", "claude:c4caee3c#L2382", "claude:c4caee3c#L2411"]
hook: "Agent đề xuất làm trong fork, người dùng hỏi lại: việc này thuộc repo nào"
tension: nguoi_dung_may_sai
sides: ["Agent đề xuất làm một phần L13 và L22 trong lõi", "Người dùng hỏi từng mục rồi kết luận cả hai thuộc repo dự án"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án Obsidian Hybrid Search là công cụ tìm kiếm chạy trên máy cho vault Obsidian, và người làm đang dựng một fork chỉ chứa cơ chế dùng chung. Agent đề xuất làm một phần hai mục gợi ý khi viết và sổ câu tìm trong lõi fork, cho rằng việc đó đúng chỗ. PRD thật ra đã ghi cả hai thuộc repo dự án, vì chỉ plugin mới thấy được việc gõ và bấm mở note. Người làm hỏi từng mục rồi cập nhật PRD, để không đưa logic sản phẩm vào fork."
audience: dev làm plugin hoặc công cụ có nhiều repo
spine_context: Obsidian Hybrid Search là công cụ tìm kiếm chạy cục bộ cho vault Obsidian; người làm đang dựng một fork chỉ chứa cơ chế dùng chung.
spine_context_lines: [profile]
spine_want: Hoàn tất các mục bắt buộc của roadmap trong plan.
spine_want_lines: ["claude:c4caee3c#L11"]
spine_obstacle: "L13 cần mã chạy trong Obsidian, CLI và MCP không làm được. L22 cần biết người dùng có mở note từ kết quả tìm hay không."
spine_obstacle_lines: ["claude:c4caee3c#L2250"]
spine_turn: Agent tưởng có thể làm một phần L13 và L22 trong lõi fork; PRD đã ghi cả hai thuộc repo dự án.
spine_turn_lines: ["claude:c4caee3c#L2228", "claude:c4caee3c#L2250"]
spine_action: "Người dùng hỏi từng mục, rồi agent cập nhật PRD mục 14.2: L13 và L22 thuộc repo dự án."
spine_action_lines: ["claude:c4caee3c#L2394", "claude:c4caee3c#L2404"]
spine_outcome: Thay đổi đã commit và push ở a50f7d1; fork không còn việc cho L13 và L22.
spine_outcome_lines: ["claude:c4caee3c#L2405", "claude:c4caee3c#L2411"]
spine_takeaway: "Đọc cột phía làm trong PRD trước khi đề xuất đưa việc vào fork, và quyết ranh giới repo trước khi viết code."
spine_takeaway_lines: ["claude:c4caee3c#L2228", "claude:c4caee3c#L2411"]
completeness: 7
---

# Ranh giới fork và repo dự án: hai việc L13 và L22 không thuộc fork

**Góc kể:** Dự án Obsidian Hybrid Search là công cụ tìm kiếm chạy trên máy cho vault Obsidian, và người làm đang dựng một fork chỉ chứa cơ chế dùng chung. Agent đề xuất làm một phần hai mục gợi ý khi viết và sổ câu tìm trong lõi fork, cho rằng việc đó đúng chỗ. PRD thật ra đã ghi cả hai thuộc repo dự án, vì chỉ plugin mới thấy được việc gõ và bấm mở note. Người làm hỏi từng mục rồi cập nhật PRD, để không đưa logic sản phẩm vào fork.
**Bối cảnh:** PRD 9.0 quy định fork chỉ chứa cơ chế chung cho mọi người dùng OHS, không chứa logic sản phẩm.
**Chuyện gì xảy ra:** Agent ban đầu đề xuất làm một phần của hai việc gợi ý khi viết và sổ câu tìm trong lõi. Người dùng hỏi lại từng mục (plugin hay lõi, thuộc repo nào), rồi quyết định cả hai thuộc repo dự án. PRD mục 14.2 được cập nhật đúng như vậy.
**Bài học:** Quyết ranh giới repo trước khi viết mã. Hỏi 'thuộc repo nào' sớm để không đưa logic sản phẩm vào fork.
