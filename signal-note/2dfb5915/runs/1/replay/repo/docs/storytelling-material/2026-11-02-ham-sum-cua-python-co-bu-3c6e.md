---
id: 2026-11-02-ham-sum-cua-python-co-bu-3c6e
code: M-HSG7
aliases: [M-HSG7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1650"]
hook: "Phải copy cả lỗi làm tròn của Python để điểm lệch bằng 0"
tension: giup_ma_hai
sides: ["Thuật toán cộng có bù sai số chính xác hơn", "Bản Rust phải bắt chước đúng nó mới khớp từng bit"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án là một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, và người làm đang viết lại lõi bằng Rust để thay bản Python, với yêu cầu kết quả giống hệt. Người làm tưởng phép cộng số thực thông thường là đủ để khớp điểm; hoá ra Python 3.14 cộng có bù sai số, nên bản Rust phải chép đúng thuật toán ấy. Ai port code số học sang ngôn ngữ khác và cần khớp từng bit nên để ý chỗ này."
audience: dev port code số học sang ngôn ngữ khác và cần khớp kết quả từng bit
spine_context: "Dự án là một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust để thay bản Python."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: "Muốn bản Rust cho kết quả giống hệt bản Python trên cùng dữ liệu, đến từng điểm số."
spine_want_lines: ["claude:2dfb5915#L1650"]
spine_obstacle: Cộng số thực theo cách thông thường cho điểm lệch ở bit cuối cùng so với Python.
spine_obstacle_lines: ["claude:2dfb5915#L1650"]
spine_turn: "Tưởng phép cộng thông thường là đủ; hoá ra Python 3.14 cộng có bù sai số, nên phải chép đúng thuật toán của CPython."
spine_turn_lines: ["claude:2dfb5915#L1650"]
spine_action: "Chép thuật toán cộng có bù sai số của CPython vào hàm py_sum, và khớp thứ tự cạnh, hàng đợi và cách làm tròn với Python."
spine_action_lines: ["claude:2dfb5915#L1650"]
spine_outcome: "15 lời gọi golden và 400 lời gọi sinh ngẫu nhiên đều khớp từng bit, chênh lệch điểm bằng 0."
spine_outcome_lines: ["claude:2dfb5915#L1650"]
spine_takeaway: "Khi port để khớp kết quả số, cần kiểm tra cách ngôn ngữ cộng số thực, không chỉ thuật toán."
spine_takeaway_lines: ["claude:2dfb5915#L1650"]
completeness: 7
---

# Hàm sum của Python có bù sai số: copy đúng thuật toán để điểm related khớp đến từng bit

**Góc kể:** Dự án là một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, và người làm đang viết lại lõi bằng Rust để thay bản Python, với yêu cầu kết quả giống hệt. Người làm tưởng phép cộng số thực thông thường là đủ để khớp điểm; hoá ra Python 3.14 cộng có bù sai số, nên bản Rust phải chép đúng thuật toán ấy. Ai port code số học sang ngôn ngữ khác và cần khớp từng bit nên để ý chỗ này.
**Bối cảnh:** Thuật toán related dùng tổng số thực rất nhiều lần. Port bằng sum thông thường thì lệch ở bit cuối cùng.
**Chuyện gì xảy ra:** Python 3.14 dùng thuật toán cộng có bù sai số, nên bản Rust phải copy đúng thuật toán của CPython. Kết quả 15 lời gọi golden và 400 lời gọi sinh ngẫu nhiên khớp hoàn toàn, chênh lệch điểm bằng 0.
**Bài học:** Khi cần khớp bit với một bản khác, sai khác nhỏ nhất thường nằm ở thư viện số học của bản đó chứ không nằm ở thuật toán.
**Artefact:** Bảng 15 lời gọi golden khớp, chênh điểm 0. Không đưa dữ liệu.
