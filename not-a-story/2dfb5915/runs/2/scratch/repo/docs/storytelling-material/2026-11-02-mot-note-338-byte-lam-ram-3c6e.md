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
hook: "Một note 338 byte ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["Note chỉ 338 byte với 7 tầng alias", "Sinh 11,1 triệu props, chiếm 1,45 GB RAM, thêm một tầng cần 14 GB"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang thay lõi Python bằng Rust. Việc khớp hành vi với Python được coi là đủ, nhưng một note 338 byte với 7 tầng alias YAML đã chiếm 1,45 GB RAM, và Python cũng bùng nổ tương tự. Với file không tin cậy, một đoạn nhỏ có thể nhân thành dữ liệu rất lớn, nên cần ngân sách mỗi note để chặn từ đầu."
audience: dev xử lý file YAML hoặc file không tin cậy
spine_context: "Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian, đang thay lõi Python bằng lõi Rust."
spine_context_lines: [profile]
spine_want: Thay lõi Python bằng Rust mà vẫn giữ hành vi khớp Python.
spine_want_lines: ["claude:2dfb5915#L819"]
spine_obstacle: "Một note 338 byte với 7 tầng alias YAML chiếm 1,45 GB RAM; thêm một tầng nữa cần khoảng 14 GB."
spine_obstacle_lines: ["claude:2dfb5915#L811"]
spine_turn: "Tưởng khớp Python là đủ; hoá ra note đó vẫn bùng RAM, và Python cũng bùng tương tự."
spine_turn_lines: ["claude:2dfb5915#L811"]
spine_action: Đặt ngân sách mỗi note là 1 triệu props và 64 MiB; vượt thì báo MemoryError và ghi là lệch có chủ ý.
spine_action_lines: ["claude:2dfb5915#L820", "claude:2dfb5915#L833"]
spine_outcome: "Parity 17 bảng khớp, fuzz 25.000 note YAML cho 0 khác biệt."
spine_outcome_lines: ["claude:2dfb5915#L833"]
spine_takeaway: "Với file không tin cậy, khớp hành vi với bản cũ chưa đủ; cần giới hạn tài nguyên ngay từ đầu."
spine_takeaway_lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L833"]
completeness: 7
---

# Một note 338 byte làm RAM lên 1,45 GB: bom alias YAML

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph của vault Obsidian đang thay lõi Python bằng Rust. Việc khớp hành vi với Python được coi là đủ, nhưng một note 338 byte với 7 tầng alias YAML đã chiếm 1,45 GB RAM, và Python cũng bùng nổ tương tự. Với file không tin cậy, một đoạn nhỏ có thể nhân thành dữ liệu rất lớn, nên cần ngân sách mỗi note để chặn từ đầu.
**Bối cảnh:** Review code phát hiện YAML có alias lồng nhau gây bùng nổ bộ nhớ, cả Rust lẫn Python đều dính.
**Chuyện gì xảy ra:** Note 338 byte với 7 tầng alias tạo 11,1 triệu props và chiếm 1,45 GB RAM trong Rust. Thêm một tầng nữa (vẫn dưới 400 byte) cần khoảng 14 GB. Agent đặt ngân sách mỗi note là 1 triệu props và 64 MiB, vượt thì báo lỗi MemoryError và ghi như một lệch có chủ ý.
**Bài học:** Với đầu vào không tin cậy, một đoạn văn bản nhỏ có thể nhân lên thành dữ liệu rất lớn. Cần giới hạn ngân sách ngay từ đầu.
**Artefact:** Số liệu theo từng tầng alias (không có nội dung note).
