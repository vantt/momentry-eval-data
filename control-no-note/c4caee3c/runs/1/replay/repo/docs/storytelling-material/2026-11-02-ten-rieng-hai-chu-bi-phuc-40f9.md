---
id: 2026-11-02-ten-rieng-hai-chu-bi-phuc-40f9
code: M-MKN7
aliases: [M-MKN7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2733", "claude:c4caee3c#L2787", "claude:c4caee3c#L2789", "claude:c4caee3c#L2842"]
hook: "Một tên riêng hai chữ bị sửa thành từ thường"
tension: giup_ma_hai
sides: ["Phục hồi dấu để tìm kiếm tốt hơn", "Tên riêng bị đổi thành từ thường, điểm tụt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian, và người làm đang chỉnh cách nó tìm tiếng Việt khi gõ không dấu. Người làm nghi tuỳ chọn phục hồi dấu sai với câu có dấu một phần, và giả định lỗi nằm ở ngưỡng 50%. Ngưỡng đó đúng theo spec; lỗi nằm ở cách dựng câu gửi cho model nhúng, khiến 'Hội An' thành 'hội ăn'. Ai làm tìm kiếm tiếng Việt nên nhớ: khi lỗi nằm ở đầu vào thì đừng sửa ngưỡng, và viết test chứng minh lỗi trước."
audience: dev làm tìm kiếm hoặc RAG cho tiếng Việt
spine_context: "Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian, dạng plugin, MCP server và CLI, đang làm tìm kiếm tiếng Việt."
spine_context_lines: [profile]
spine_want: Muốn tuỳ chọn restoreForEmbedding đẩy nDCG@5 lên mà không hạng mục nào tụt.
spine_want_lines: ["claude:c4caee3c#L2789"]
spine_obstacle: "Câu có dấu một phần, như 'Hội An', bị phục hồi sai: chữ 'An' thành 'ăn'."
spine_obstacle_lines: ["claude:c4caee3c#L2787"]
spine_turn: "Nghi tuỳ chọn phục hồi dấu làm sai với câu có dấu một phần, và giả định nguyên nhân nằm ở ngưỡng 50%. Hoá ra ngưỡng đúng theo PRD; lỗi nằm ở cách dựng embedQuery."
spine_turn_lines: ["claude:c4caee3c#L2787", "claude:c4caee3c#L2789"]
spine_action: "Viết test thất bại trên mã cũ trước, rồi sửa restoredText: giữ nguyên chữ đã có dấu, chỉ phục hồi chữ không dấu khi vault không bao giờ viết nó trần và độ tin cậy đủ."
spine_action_lines: ["claude:c4caee3c#L2787"]
spine_outcome: "nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt; tuỳ chọn được bật mặc định."
spine_outcome_lines: ["claude:c4caee3c#L2789"]
spine_takeaway: "Khi lỗi nằm ở cách dựng đầu vào, đừng sửa ngưỡng; viết test chứng minh lỗi trước khi sửa."
spine_takeaway_lines: ["claude:c4caee3c#L2787"]
completeness: 7
---

# Tên riêng hai chữ bị phục hồi dấu thành từ thường, kéo nDCG@5 xuống

**Góc kể:** Obsidian Hybrid Search là công cụ tìm kiếm cho vault Obsidian, và người làm đang chỉnh cách nó tìm tiếng Việt khi gõ không dấu. Người làm nghi tuỳ chọn phục hồi dấu sai với câu có dấu một phần, và giả định lỗi nằm ở ngưỡng 50%. Ngưỡng đó đúng theo spec; lỗi nằm ở cách dựng câu gửi cho model nhúng, khiến 'Hội An' thành 'hội ăn'. Ai làm tìm kiếm tiếng Việt nên nhớ: khi lỗi nằm ở đầu vào thì đừng sửa ngưỡng, và viết test chứng minh lỗi trước.
**Bối cảnh:** Khi bật restoreForEmbedding, một câu có một chữ có dấu trên hai chữ được coi là chưa có dấu, nên chữ không dấu bị phục hồi theo từ phổ biến hơn trong vault.
**Chuyện gì xảy ra:** Model eval phát hiện một tên riêng hai chữ bị đổi sang từ thường. Ngưỡng 50% của PRD không sai, lỗi nằm ở cách dựng câu gửi cho embedder. Agent viết test thất bại trên mã cũ trước, rồi sửa để chỉ phục hồi chữ không dấu khi vault không bao giờ viết nó trần và độ tin cậy đủ. nDCG@5 tổng tăng từ 0,932 lên 0,954, không hạng mục nào tụt, và tuỳ chọn được bật mặc định.
**Bài học:** Đừng sửa ngưỡng khi lỗi nằm ở chỗ dựng đầu vào. Viết test chứng minh lỗi trước khi sửa.
**Artefact:** Bảng nDCG@5 trước và sau cho hạng mục liên quan.
