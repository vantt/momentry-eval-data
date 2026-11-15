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
tension: khac
sides: ["Thiết kế gốc: chuyển việc đọc qua OHS", "OHS chỉ đọc note đã index, nên pkm tự đọc file và plan lệch thiết kế"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ dòng lệnh giúp Claude Desktop hỏi graph của vault Obsidian, và đang chuyển sang lõi Rust. Plan phase 17 định để việc đọc nội dung note đi qua OHS, tưởng vậy là đủ. Nhưng OHS chỉ trả note đã index, nên lúc khởi động hay index (có thể khoảng 10 phút) agent không đọc được note nào. Người làm chốt để `pkm` tự đọc file .md trong vault, luôn dùng được, và ghi rõ chỗ lệch khỏi plan. Ai xây công cụ đọc dữ liệu qua index nên quan tâm vì tool không cần index mà phụ thuộc vào index thì sẽ đứng khi index chưa xong."
audience: dev xây công cụ đọc dữ liệu qua index
spine_context: "Một công cụ dòng lệnh giúp Claude Desktop hỏi graph của vault Obsidian, đang chuyển bản Python sang lõi Rust."
spine_context_lines: [profile]
spine_want: Muốn tool `read` đọc được nội dung note; câu hỏi là ai sẽ đọc file.
spine_want_lines: ["claude:2dfb5915#L3144"]
spine_obstacle: OHS chỉ đọc được note đã index; lúc khởi động hoặc index (có thể khoảng 10 phút với vault lớn) agent không đọc được note nào và nhận lỗi `ohs_not_ready`.
spine_obstacle_lines: ["claude:2dfb5915#L3160"]
spine_turn: "Plan ghi chuyển việc đọc sang OHS, tưởng vậy là đủ; hoá ra OHS không có gì để trả trong lúc đang index."
spine_turn_lines: ["claude:2dfb5915#L3144", "claude:2dfb5915#L3160"]
spine_action: Hai agent đề xuất để `pkm` tự đọc file .md trong vault; người làm đồng ý và giao agent làm bộ 13 tool theo thiết kế đó.
spine_action_lines: ["claude:2dfb5915#L3160", "claude:2dfb5915#L3170", "claude:2dfb5915#L3175"]
spine_outcome: "Nền phase 17 đã xong trên nhánh, CI xanh, bộ so khớp vẫn 0 lệch."
spine_outcome_lines: ["claude:2dfb5915#L3160"]
spine_takeaway: Tool không cần index thì đừng để nó phụ thuộc vào index.
spine_takeaway_lines: ["claude:2dfb5915#L3160"]
completeness: 7
---

# read: pkm tự đọc file thay vì chuyển qua OHS

**Góc kể:** Dự án là một công cụ dòng lệnh giúp Claude Desktop hỏi graph của vault Obsidian, và đang chuyển sang lõi Rust. Plan phase 17 định để việc đọc nội dung note đi qua OHS, tưởng vậy là đủ. Nhưng OHS chỉ trả note đã index, nên lúc khởi động hay index (có thể khoảng 10 phút) agent không đọc được note nào. Người làm chốt để `pkm` tự đọc file .md trong vault, luôn dùng được, và ghi rõ chỗ lệch khỏi plan. Ai xây công cụ đọc dữ liệu qua index nên quan tâm vì tool không cần index mà phụ thuộc vào index thì sẽ đứng khi index chưa xong.
**Bối cảnh:** Plan phase 17 ghi read chuyển tiếp sang OHS, nhưng hai agent đều phản đối.
**Chuyện gì xảy ra:** OHS chỉ đọc được note đã index, nên trong lúc khởi động hoặc index có thể mất khoảng 10 phút mà agent không đọc được note nào. Agent đề nghị pkm tự đọc file trong vault, luôn dùng được. Người dùng đồng ý, và plan lệch khỏi thiết kế ban đầu.
**Bài học:** Tool không cần index thì đừng để nó phụ thuộc vào index. Ghi rõ lệch khỏi plan khi người duyệt đổi quyết định.
