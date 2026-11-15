---
id: 2026-11-02-read-pkm-tu-doc-file-thay-3c6e
code: M-GYCY
aliases: [M-GYCY]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, dao_quyet_dinh]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:2dfb5915#L3144", "claude:2dfb5915#L3170"]
hook: "Index mất 10 phút, trong lúc đó agent không đọc được note nào"
tension: chon_mot_mat_mot
sides: ["Giữ thiết kế gốc: OHS đọc note", "pkm tự đọc file để luôn dùng được, plan lệch thiết kế"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh giúp Claude Desktop hỏi về graph vault Obsidian đang chuyển lõi sang Rust, và người làm muốn tool đọc thân note luôn dùng được. Plan ban đầu giao việc đọc này cho OHS, nhưng OHS chỉ đọc được note đã index, nên trong lúc index (có thể khoảng 10 phút) agent không đọc được note nào. Hai agent phản đối, người dùng đồng ý để pkm tự đọc file trong vault, và plan lệch khỏi thiết kế ban đầu. Ai dựng tool cho agent nên nhớ: tool không cần index thì đừng để nó phụ thuộc vào index."
audience: dev xây tool cho agent và người làm công cụ MCP
spine_context: "Một công cụ dòng lệnh giúp Claude Desktop hỏi về graph của vault Obsidian, đang chuyển lõi sang Rust."
spine_context_lines: [profile]
spine_want: Muốn tool đọc thân note luôn dùng được cho agent.
spine_want_lines: ["claude:2dfb5915#L3144"]
spine_obstacle: "OHS chỉ đọc được note đã index, nên lúc khởi động hoặc index (có thể khoảng 10 phút) agent không đọc được note nào."
spine_obstacle_lines: ["claude:2dfb5915#L3144", "claude:2dfb5915#L3160"]
spine_turn: "Tưởng việc đọc note chuyển sang OHS là ổn theo plan; hoá ra OHS không đọc được trong lúc index, và note vừa sửa có thể trả bản cũ."
spine_turn_lines: ["claude:2dfb5915#L3144", "claude:2dfb5915#L3160"]
spine_action: "Hai agent đề xuất pkm tự đọc file trong vault, người dùng đồng ý và giao agent làm tiếp bộ tool."
spine_action_lines: ["claude:2dfb5915#L3170", "claude:2dfb5915#L3175"]
spine_outcome: Việc đọc note lệch khỏi plan phase 17; agent tiếp tục làm trên nhánh phase 17.
spine_outcome_lines: ["claude:2dfb5915#L3170", "claude:2dfb5915#L3180"]
spine_takeaway: Tool không cần index thì đừng để nó phụ thuộc vào index.
spine_takeaway_lines: ["claude:2dfb5915#L3160"]
completeness: 7
---

# read: pkm tự đọc file thay vì chuyển qua OHS

**Góc kể:** Một công cụ dòng lệnh giúp Claude Desktop hỏi về graph vault Obsidian đang chuyển lõi sang Rust, và người làm muốn tool đọc thân note luôn dùng được. Plan ban đầu giao việc đọc này cho OHS, nhưng OHS chỉ đọc được note đã index, nên trong lúc index (có thể khoảng 10 phút) agent không đọc được note nào. Hai agent phản đối, người dùng đồng ý để pkm tự đọc file trong vault, và plan lệch khỏi thiết kế ban đầu. Ai dựng tool cho agent nên nhớ: tool không cần index thì đừng để nó phụ thuộc vào index.
**Bối cảnh:** Plan phase 17 ghi read chuyển tiếp sang OHS, nhưng hai agent đều phản đối.
**Chuyện gì xảy ra:** OHS chỉ đọc được note đã index, nên trong lúc khởi động hoặc index có thể mất khoảng 10 phút mà agent không đọc được note nào. Agent đề nghị pkm tự đọc file trong vault, luôn dùng được. Người dùng đồng ý, và plan lệch khỏi thiết kế ban đầu.
**Bài học:** Tool không cần index thì đừng để nó phụ thuộc vào index. Ghi rõ lệch khỏi plan khi người duyệt đổi quyết định.
