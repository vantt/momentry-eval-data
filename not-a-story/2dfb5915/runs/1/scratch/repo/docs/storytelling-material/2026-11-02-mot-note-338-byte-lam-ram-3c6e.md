---
id: 2026-11-02-mot-note-338-byte-lam-ram-3c6e
code: M-JR7N
aliases: [M-JR7N]
date: 2026-11-02
repo: repo
status: raw
signals: [khac, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L833"]
hook: "Note 338 byte ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["Một note chỉ 338 byte", "Bung ra 11,1 triệu props, 1,45 GB RAM; thêm một tầng là 14 GB"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang thay lõi Python bằng Rust để chạy như một file cài sẵn. Người làm tưởng khớp kết quả với bản Python là đủ an toàn. Review cho thấy một note 338 byte với alias YAML lồng nhau có thể bung ra 11,1 triệu props và chiếm 1,45 GB RAM, và Python cũng nổ y như vậy. Ai xử lý file không tin cậy nên đặt giới hạn bộ nhớ ngay từ đầu."
audience: dev xử lý file YAML không tin cậy hoặc viết parser
spine_context: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi Python bằng lõi Rust để chạy như một file cài sẵn."
spine_context_lines: [profile]
spine_want: Muốn bản Rust cài được thành một bản dùng thực tế.
spine_want_lines: ["claude:2dfb5915#L571"]
spine_obstacle: "Review phát hiện YAML có alias lồng nhau: một note 338 byte bung ra 11,1 triệu props và chiếm 1,45 GB RAM."
spine_obstacle_lines: ["claude:2dfb5915#L811"]
spine_turn: "Tưởng khớp kết quả với bản Python là đủ an toàn; hoá ra Python cũng nổ bộ nhớ y như vậy, nên khớp Python không có nghĩa là an toàn."
spine_turn_lines: ["claude:2dfb5915#L811"]
spine_action: "Thêm ngân sách mỗi note: tối đa 1 triệu props và 64 MiB. Vượt ngân sách thì báo MemoryError và ghi đây là lệch có chủ ý so với Python."
spine_action_lines: ["claude:2dfb5915#L833"]
spine_outcome: "Đã sửa 6 lỗi từ review. kg-solo khớp 17 bảng với 0 khác biệt không tên, và fuzz 25.000 note YAML vẫn 0 khác biệt."
spine_outcome_lines: ["claude:2dfb5915#L833"]
spine_takeaway: "Với đầu vào không tin cậy, một đoạn văn bản nhỏ có thể nhân thành dữ liệu rất lớn. Đặt giới hạn ngân sách từ đầu, đừng chỉ dựa vào việc khớp bản cũ."
spine_takeaway_lines: ["claude:2dfb5915#L811"]
completeness: 7
---

# Một note 338 byte làm RAM lên 1,45 GB: bom alias YAML

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang thay lõi Python bằng Rust để chạy như một file cài sẵn. Người làm tưởng khớp kết quả với bản Python là đủ an toàn. Review cho thấy một note 338 byte với alias YAML lồng nhau có thể bung ra 11,1 triệu props và chiếm 1,45 GB RAM, và Python cũng nổ y như vậy. Ai xử lý file không tin cậy nên đặt giới hạn bộ nhớ ngay từ đầu.
**Bối cảnh:** Review code phát hiện YAML có alias lồng nhau gây bùng nổ bộ nhớ, cả Rust lẫn Python đều dính.
**Chuyện gì xảy ra:** Note 338 byte với 7 tầng alias tạo 11,1 triệu props và chiếm 1,45 GB RAM trong Rust. Thêm một tầng nữa (vẫn dưới 400 byte) cần khoảng 14 GB. Agent đặt ngân sách mỗi note là 1 triệu props và 64 MiB, vượt thì báo lỗi MemoryError và ghi như một lệch có chủ ý.
**Bài học:** Với đầu vào không tin cậy, một đoạn văn bản nhỏ có thể nhân lên thành dữ liệu rất lớn. Cần giới hạn ngân sách ngay từ đầu.
**Artefact:** Số liệu theo từng tầng alias (không có nội dung note).
