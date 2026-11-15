---
id: 2026-11-02-python-liet-ke-file-theo-thu-3c6e
code: M-P6CM
aliases: [M-P6CM]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L474"]
hook: "Đổi thứ tự liệt kê file, 593 trên 726 id đổi theo"
tension: nho_ma_to
sides: ["Thứ tự liệt kê file của hệ điều hành, chẳng ai để ý", "593/726 edges.id đổi, điểm lệch 1e-5 vượt mức cho phép 1e-6"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust, để cho kết quả giống bản Python trên cùng dữ liệu. Người làm tin đầu ra của bản Python là mốc cố định để so, nhưng khi đảo thứ tự liệt kê file thì 593 trên 726 edges.id đổi theo, vì Python phụ thuộc thứ tự hệ điều hành trả về. Ai so đầu ra với bản cũ nên kiểm xem nó có phụ thuộc thứ tự không trước khi tin vào sai số."
audience: dev so khớp đầu ra khi viết lại công cụ cũ
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang được viết lại bằng Rust để cho kết quả giống bản Python trên cùng dữ liệu."
spine_context_lines: [profile]
spine_want: "Hoàn tất toàn bộ plan lõi Rust, 17 phase."
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Nhiều phase cần người làm chạy bước thử trên máy thật, nên agent phải dừng chờ."
spine_obstacle_lines: ["claude:2dfb5915#L474"]
spine_turn: Tưởng đầu ra Python là mốc cố định để so; hoá ra nó phụ thuộc thứ tự hệ điều hành liệt kê file.
spine_turn_lines: ["claude:2dfb5915#L474"]
spine_action: "Ghim thứ tự file theo đường dẫn đã sắp, ghi vào docs/DECISIONS.md, và giữ so khớp chặt như PRD."
spine_action_lines: ["claude:2dfb5915#L474"]
spine_outcome: "CI xanh trên Windows, macOS và Linux; các phase 08 đến 17 vẫn blocked, chờ người làm trả lời cổng."
spine_outcome_lines: ["claude:2dfb5915#L463", "claude:2dfb5915#L474"]
spine_takeaway: "Khi so đầu ra với bản cũ, kiểm xem nó có phụ thuộc thứ tự không xác định trước khi tin vào sai số."
spine_takeaway_lines: ["claude:2dfb5915#L474"]
completeness: 7
---

# Python liệt kê file theo thứ tự của hệ điều hành: đổi thứ tự là 593 trên 726 edges.id đổi theo

**Góc kể:** Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust, để cho kết quả giống bản Python trên cùng dữ liệu. Người làm tin đầu ra của bản Python là mốc cố định để so, nhưng khi đảo thứ tự liệt kê file thì 593 trên 726 edges.id đổi theo, vì Python phụ thuộc thứ tự hệ điều hành trả về. Ai so đầu ra với bản cũ nên kiểm xem nó có phụ thuộc thứ tự không trước khi tin vào sai số.
**Bối cảnh:** Đầu ra của bản Python được coi là chuẩn, nhưng không ai nghĩ tới việc nó phụ thuộc vào thứ tự file hệ điều hành trả về.
**Chuyện gì xảy ra:** Khi đảo thứ tự liệt kê, 593 trên 726 edges.id đổi theo và điểm related lệch cỡ 1e-5, trong khi PRD cho phép 1e-6. Lựa chọn là ghim thứ tự theo đường dẫn đã sắp và ghi vào quyết định, các phase sau phải giữ đúng thứ tự này.
**Bài học:** Khi so khớp đầu ra với bản cũ, kiểm xem nó có phụ thuộc thứ tự không xác định (thư mục, hash, set) trước khi tin vào sai số.
**Artefact:** Bảng số: 593/726 edges.id đổi, lệch điểm 1e-5 so với ngưỡng 1e-6.
