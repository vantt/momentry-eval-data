---
id: 2026-11-02-thu-tu-liet-ke-file-cua-3c6e
code: M-8MXR
aliases: [M-8MXR]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L423", "claude:2dfb5915#L474"]
hook: "Đổi thứ tự liệt kê file, 593 trên 726 id đổi"
tension: nho_ma_to
sides: ["Chỉ đổi thứ tự hệ điều hành liệt kê file", "593 trên 726 edges.id đổi, điểm related lệch 1e-5, vượt ngưỡng 1e-6"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh giúp hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust, và người làm muốn bản mới cho cùng kết quả với bản Python cũ. Người làm tưởng thứ tự file hệ điều hành trả về không ảnh hưởng đầu ra. Hoá ra đảo thứ tự thì 593 trên 726 id cạnh đổi và điểm liên quan lệch vượt mức 1e-6 mà PRD cho phép. Ai viết lại code rồi so kết quả với bản cũ đều nên kiểm tra lỗi này."
audience: dev viết lại công cụ rồi so kết quả với bản cũ
spine_context: "Một công cụ dòng lệnh để hỏi Claude Desktop về graph của vault Obsidian, đang được viết lại bằng Rust."
spine_context_lines: [profile, "claude:2dfb5915#L11"]
spine_want: "Muốn hoàn tất toàn bộ plan port lõi sang Rust, từ phase 01 đến 17."
spine_want_lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L477"]
spine_obstacle: "Các phase 02, 03 và 05 chờ người dùng làm bước riêng; phase 08 trở đi bị chặn ở cổng G0."
spine_obstacle_lines: ["claude:2dfb5915#L474", "claude:2dfb5915#L484"]
spine_turn: Tưởng thứ tự file hệ điều hành trả về không ảnh hưởng đầu ra; hoá ra đảo thứ tự làm 593 trên 726 edges.id đổi.
spine_turn_lines: ["claude:2dfb5915#L423", "claude:2dfb5915#L474"]
spine_action: Ghim thứ tự liệt kê theo đường dẫn đã sắp và ghi quyết định vào DECISIONS.
spine_action_lines: ["claude:2dfb5915#L423"]
spine_outcome: "Vẫn so chặt như PRD (lệch tối đa 1e-6); CI xanh trên Windows, macOS và Linux; phase 09 và 11 phải giữ thứ tự này."
spine_outcome_lines: ["claude:2dfb5915#L423", "claude:2dfb5915#L474"]
spine_takeaway: "Kết quả phụ thuộc thứ tự hệ điều hành là lỗi ẩn: kiểm tra xem đầu ra có đổi khi chỉ đổi thứ tự đầu vào không."
spine_takeaway_lines: ["claude:2dfb5915#L474"]
completeness: 7
---

# Thứ tự liệt kê file của hệ điều hành làm đầu ra Python đổi

**Góc kể:** Một công cụ dòng lệnh giúp hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust, và người làm muốn bản mới cho cùng kết quả với bản Python cũ. Người làm tưởng thứ tự file hệ điều hành trả về không ảnh hưởng đầu ra. Hoá ra đảo thứ tự thì 593 trên 726 id cạnh đổi và điểm liên quan lệch vượt mức 1e-6 mà PRD cho phép. Ai viết lại code rồi so kết quả với bản cũ đều nên kiểm tra lỗi này.
**Bối cảnh:** Python liệt kê note theo thứ tự hệ điều hành trả về, thứ tự này khác nhau giữa NTFS và APFS.
**Chuyện gì xảy ra:** Khi đảo thứ tự liệt kê, 593 trên 726 edges.id đổi, và điểm related lệch khoảng 1e-5, vượt ngưỡng 1e-6 của PRD. Agent ghim thứ tự theo đường dẫn đã sắp và ghi vào nhật ký quyết định. Các phase sau phải giữ thứ tự này.
**Bài học:** Kết quả phụ thuộc thứ tự hệ điều hành là lỗi ẩn: kiểm tra xem đầu ra có đổi khi chỉ đổi thứ tự đầu vào không.
**Artefact:** Bảng số edges đổi theo thứ tự (không có dữ liệu riêng tư).
