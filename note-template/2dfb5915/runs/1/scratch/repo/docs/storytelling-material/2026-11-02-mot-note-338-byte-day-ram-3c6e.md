---
id: 2026-11-02-mot-note-338-byte-day-ram-3c6e
code: M-PBJ2
aliases: [M-PBJ2]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L819", "claude:2dfb5915#L844"]
hook: "Một note 338 byte ngốn 1,45 GB RAM"
tension: nho_ma_to
sides: ["Note chỉ nặng 338 byte", "Bảy tầng alias phình thành 11,1 triệu mục và 1,45 GB"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh cho vault Obsidian đang viết lại lõi bằng Rust để cho kết quả khớp bản Python. Người làm tưởng khớp Python là đủ; khi rà soát, họ thấy một note 338 byte với alias lồng nhau có thể sinh 11,1 triệu mục và ngốn 1,45 GB RAM, và Python cũng phình y hệt. Khớp spec không có nghĩa là an toàn: ai viết parser đọc file không tin cậy nên đặt ngân sách tài nguyên cho từng đơn vị dữ liệu."
audience: dev viết parser hoặc công cụ đọc file không tin cậy
spine_context: "Một công cụ dòng lệnh cho vault Obsidian, đang viết lại lõi bằng Rust để cho kết quả khớp với bản Python."
spine_context_lines: [profile]
spine_want: Muốn hoàn tất plan viết lại lõi và tới một bản cài được.
spine_want_lines: ["claude:2dfb5915#L11", "claude:2dfb5915#L571"]
spine_obstacle: "Plan còn dở, các phase phụ thuộc gate đang chờ người dùng."
spine_obstacle_lines: ["claude:2dfb5915#L477"]
spine_turn: "Tưởng khớp Python là đủ an toàn; hoá ra Python cũng phình RAM y hệt, nên khớp spec vẫn là lỗ DoS."
spine_turn_lines: ["claude:2dfb5915#L811"]
spine_action: Thêm ngân sách 1.000.000 props và 64 MiB text cho mỗi note; vượt thì báo MemoryError và ghi là lệch có chủ ý.
spine_action_lines: ["claude:2dfb5915#L833"]
spine_outcome: kg-solo khớp 17 bảng với 0 diff không tên; fuzz 25.000 note YAML vẫn 0 khác biệt.
spine_outcome_lines: ["claude:2dfb5915#L833"]
spine_takeaway: "Đặt giới hạn tài nguyên cho từng note, không chỉ kiểm đúng sai so với bản tham chiếu."
spine_takeaway_lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L833"]
completeness: 7
---

# Một note 338 byte đẩy RAM lên 1,45 GB

**Góc kể:** Một công cụ dòng lệnh cho vault Obsidian đang viết lại lõi bằng Rust để cho kết quả khớp bản Python. Người làm tưởng khớp Python là đủ; khi rà soát, họ thấy một note 338 byte với alias lồng nhau có thể sinh 11,1 triệu mục và ngốn 1,45 GB RAM, và Python cũng phình y hệt. Khớp spec không có nghĩa là an toàn: ai viết parser đọc file không tin cậy nên đặt ngân sách tài nguyên cho từng đơn vị dữ liệu.
**Bối cảnh:** Frontmatter YAML có alias trỏ lồng nhau, một kiểu 'alias bomb'.
**Chuyện gì xảy ra:** Bảy tầng alias trong note 338 byte sinh 11,1 triệu props và 1,45 GB RSS; thêm một tầng là khoảng 14 GB. Python cũng phình (877 MB) nên khớp spec nhưng vẫn là lỗ DoS. Sửa bằng ngân sách 1.000.000 props và 64 MiB cho mỗi note, vượt thì báo MemoryError và ghi là lệch có chủ ý.
**Bài học:** Đặt giới hạn tài nguyên cho từng đơn vị dữ liệu, không chỉ kiểm đúng sai.
