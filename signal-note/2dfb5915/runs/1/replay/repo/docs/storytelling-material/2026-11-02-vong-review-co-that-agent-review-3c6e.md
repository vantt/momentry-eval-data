---
id: 2026-11-02-vong-review-co-that-agent-review-3c6e
code: M-5B5J
aliases: [M-5B5J]
date: 2026-11-02
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:2dfb5915#L811", "claude:2dfb5915#L819", "claude:2dfb5915#L833"]
hook: "Note 338 byte ngốn 1.45 GB RAM nhờ 7 tầng alias"
tension: nho_ma_to
sides: ["Một note chỉ 338 byte", "11.1 triệu props, 1.45 GB, tầng 8 cần 14 GB"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để thay bản Python cũ. Bản Rust đã khớp Python trên 33 ca độc hại, nên tưởng là ổn. Nhưng một note 338 byte với 7 tầng alias ăn 1.45 GB RAM, tầng thứ 8 cần khoảng 14 GB. Kiểm tra khớp với bản tham chiếu không bắt được lỗi tài nguyên này, nên dev viết lại code bằng AI cần thêm bước review tìm lỗi kiểu này."
audience: dev viết lại code bằng AI và cần kiểm tra ngoài việc khớp đầu ra
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang được viết lại bằng Rust để thay bản Python cũ."
spine_context_lines: [profile]
spine_want: Muốn bản Rust chạy được như một file cài sẵn và cho kết quả giống bản Python.
spine_want_lines: ["claude:2dfb5915#L571"]
spine_obstacle: "Vòng review tìm ra một note 338 byte với 7 tầng alias ăn 1.45 GB RAM trong Rust, tầng thứ 8 cần khoảng 14 GB."
spine_obstacle_lines: ["claude:2dfb5915#L811"]
spine_turn: Tưởng bản Rust đã an toàn vì khớp Python trên 33 ca độc hại; hoá ra một note nhỏ vẫn làm hết bộ nhớ.
spine_turn_lines: ["claude:2dfb5915#L811"]
spine_action: "Thêm ngân sách cho mỗi note: tối đa 1 triệu props và 64 MiB văn bản, vượt thì báo MemoryError và ghi như một lệch có chủ ý so với Python."
spine_action_lines: ["claude:2dfb5915#L833"]
spine_outcome: "Build, clippy và test đều qua; kiểm tra parity với kg-solo exit 0, 17 bảng khớp với 0 khác biệt không tên."
spine_outcome_lines: ["claude:2dfb5915#L833"]
spine_takeaway: Kiểm tra khớp với bản tham chiếu không đủ; cần thêm vòng review tìm lỗi tài nguyên như alias bomb.
spine_takeaway_lines: ["claude:2dfb5915#L811"]
completeness: 7
---

# Vòng review có thật: agent review tìm được 'bom alias' làm hết RAM, chỉ 338 byte đã thành 1.45 GB

**Góc kể:** Một công cụ hỏi Claude Desktop về graph của vault Obsidian đang được viết lại bằng Rust để thay bản Python cũ. Bản Rust đã khớp Python trên 33 ca độc hại, nên tưởng là ổn. Nhưng một note 338 byte với 7 tầng alias ăn 1.45 GB RAM, tầng thứ 8 cần khoảng 14 GB. Kiểm tra khớp với bản tham chiếu không bắt được lỗi tài nguyên này, nên dev viết lại code bằng AI cần thêm bước review tìm lỗi kiểu này.
**Bối cảnh:** Phase vault và schema đã khớp golden 17 bảng, nhưng bên review đọc lại phần FFI và so với Python bằng 33 ca độc hại.
**Chuyện gì xảy ra:** Một note 338 byte với 7 tầng alias tạo ra 11.1 triệu props và 1.45 GB RSS trong Rust, tầng thứ 8 cần khoảng 14 GB. Python cũng bị như vậy nhưng đây vẫn là lỗ hổng từ chối dịch vụ. Agent gốc được giao sửa: mỗi note có ngân sách 1 triệu props và 64 MiB văn bản, vượt thì báo MemoryError và ghi như một lệch có chủ ý.
**Bài học:** Review đọc code kèm một bộ thử đối chiếu với bản tham chiếu sẽ tìm ra lỗi mà golden không bắt được.
**Artefact:** Con số trước sau: 1.45 GB và khoảng 14 GB. Không đưa note mẫu.
**Góc người ngoài:** cách làm phổ biến là Một người làm trên một nhánh, tự review rồi merge, không có vòng review chuyên biệt và không có agent giữ ngữ cảnh để sửa tiếp; ở đây khác ở Người dùng không phải tự tìm lỗi; vòng review liên tục bắt được treo máy, rò bộ nhớ, và hạ cấp gói, nên mỗi lần merge đều có kết quả kiểm tra kèm theo.
