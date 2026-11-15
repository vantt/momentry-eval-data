---
id: 2026-11-02-loi-nam-ca-o-spec-python-3c6e
code: M-1PRG
aliases: [M-1PRG]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1091"]
hook: "Build lỗi giữa chừng, index sai mãi, test parity vẫn xanh"
tension: tuong_ma_hoa_ra
sides: ["Parity xanh nên ai cũng tưởng bản Rust đúng", "Bản Python gốc cũng có lỗi này, nên parity không thể bắt"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh giúp Claude Desktop hỏi về graph của vault Obsidian đang được chuyển lõi từ Python sang Rust. Parity với bản Python xanh, tức bản Rust giống bản Python, nhưng review độc lập chỉ ra lỗi: build lỗi giữa chừng khiến index sai mãi, và bản Python cũng có lỗi này nên parity không bắt được. Ai dựa vào test so sánh với bản gốc để tin bản mới đúng nên đọc chuyện này."
audience: dev port code hoặc viết test so sánh với bản cũ
spine_context: "Một công cụ dòng lệnh để Claude Desktop hỏi về graph của vault Obsidian, đang thay lõi Python bằng lõi Rust."
spine_context_lines: [profile]
spine_want: "Hoàn tất plan port lõi sang Rust, và bản Rust phải khớp bản Python."
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Build lỗi giữa chừng khiến index sai mãi, vì note và edges được ghi ở hai transaction riêng."
spine_obstacle_lines: ["claude:2dfb5915#L1038"]
spine_turn: "Tưởng parity xanh nghĩa là bản Rust đúng; hoá ra parity chỉ chứng minh giống bản Python, mà bản Python cũng có lỗi này nên parity không bắt được."
spine_turn_lines: ["claude:2dfb5915#L1038", "claude:2dfb5915#L1093"]
spine_action: "Thêm cờ dirty trong meta, khoá file cho build đồng thời, đổi transaction ghi thành IMMEDIATE, rồi chạy lại parity."
spine_action_lines: ["claude:2dfb5915#L1091", "claude:2dfb5915#L1093"]
spine_outcome: "Parity kg-solo chạy lại: 64 mục, 0 lệch chưa có tên, 44 mục chưa có."
spine_outcome_lines: ["claude:2dfb5915#L1093"]
spine_takeaway: "Parity với bản gốc chỉ chứng minh giống bản gốc, không chứng minh đúng; vẫn cần review độc lập."
spine_takeaway_lines: ["claude:2dfb5915#L1038"]
completeness: 7
---

# Lỗi nằm cả ở spec Python: build lỗi giữa chừng khiến index sai mãi

**Góc kể:** Một công cụ dòng lệnh giúp Claude Desktop hỏi về graph của vault Obsidian đang được chuyển lõi từ Python sang Rust. Parity với bản Python xanh, tức bản Rust giống bản Python, nhưng review độc lập chỉ ra lỗi: build lỗi giữa chừng khiến index sai mãi, và bản Python cũng có lỗi này nên parity không bắt được. Ai dựa vào test so sánh với bản gốc để tin bản mới đúng nên đọc chuyện này.
**Bối cảnh:** Review phase 09 tìm ra lỗi build không nguyên tử, và bản Python có cùng lỗi.
**Chuyện gì xảy ra:** Bản ghi note được commit trong transaction đầu, còn edges ở transaction sau. Nếu build lỗi giữa chừng, lần build tiếp theo không thấy note nào đổi nên không tính lại edges, và index sai mãi cho tới khi chạy --full. Parity không bắt được vì bản Python cũng làm vậy. Fix thêm cờ dirty trong meta và khoá file cho build đồng thời.
**Bài học:** Parity so với bản gốc chỉ chứng minh được là giống bản gốc, không chứng minh là đúng. Review độc lập vẫn cần.
