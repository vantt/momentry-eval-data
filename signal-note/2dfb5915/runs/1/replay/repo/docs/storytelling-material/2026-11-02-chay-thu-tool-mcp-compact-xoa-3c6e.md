---
id: 2026-11-02-chay-thu-tool-mcp-compact-xoa-3c6e
code: M-QMSC
aliases: [M-QMSC]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3100", "claude:2dfb5915#L3110"]
hook: "Test 5 khoá luôn qua, vì kiểm trước khi compact xoá mất 2 khoá"
tension: tuong_ma_hoa_ra
sides: ["Test kiểm 5 khoá đều xanh", "Agent thật chỉ nhận 3 khoá vì compact bỏ khoá null"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang viết lại lõi bằng Rust, mục tiêu là cho kết quả giống bản Python. Lỗi ohs_not_ready được coi là đủ 5 khoá để agent biết trạng thái, nhưng test kiểm 5 khoá chạy trước bước nén nên luôn xanh, còn hàm nén bỏ khoá rỗng khiến agent chỉ nhận 3. Ai viết test cho API có bước lọc hay biến đổi kết quả nên kiểm đầu ra cuối cùng, không chỉ lớp bên trong."
audience: dev viết test cho API có tầng biến đổi kết quả
spine_context: "Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian, đang viết lại lõi bằng Rust để thay bản Python cũ."
spine_context_lines: [profile]
spine_want: Hoàn tất plan viết lại lõi bằng Rust.
spine_want_lines: ["claude:2dfb5915#L11"]
spine_obstacle: "Test kiểm 5 khoá chạy trước bước nén nên luôn xanh, không bắt được lỗi."
spine_obstacle_lines: ["claude:2dfb5915#L3110"]
spine_turn: Tưởng lỗi ohs_not_ready đã đủ 5 khoá; hoá ra hàm nén bỏ khoá rỗng nên agent chỉ nhận 3 khoá.
spine_turn_lines: ["claude:2dfb5915#L3098", "claude:2dfb5915#L3110"]
spine_action: Hai agent đề xuất miễn nén cho lỗi này và thêm test ở tầng MCP.
spine_action_lines: ["claude:2dfb5915#L3110"]
spine_takeaway: "Test phải kiểm đầu ra cuối cùng sau mọi lớp biến đổi, không chỉ lớp bên trong."
spine_takeaway_lines: ["claude:2dfb5915#L3110"]
completeness: 6
---

# Chạy thử tool MCP: compact() xoá khoá null làm lỗi ohs_not_ready chỉ còn 3 khoá, test cũ không bắt được vì kiểm trước khi compact

**Góc kể:** Một công cụ giúp hỏi Claude Desktop về graph của vault Obsidian đang viết lại lõi bằng Rust, mục tiêu là cho kết quả giống bản Python. Lỗi ohs_not_ready được coi là đủ 5 khoá để agent biết trạng thái, nhưng test kiểm 5 khoá chạy trước bước nén nên luôn xanh, còn hàm nén bỏ khoá rỗng khiến agent chỉ nhận 3. Ai viết test cho API có bước lọc hay biến đổi kết quả nên kiểm đầu ra cuối cùng, không chỉ lớp bên trong.
**Bối cảnh:** Hợp đồng lỗi quy định ohs_not_ready phải có đủ 5 khoá để agent biết đang khởi động hay đang index.
**Chuyện gì xảy ra:** Hàm compact bỏ mọi khoá có giá trị null trên mọi kết quả. Khi OHS đang starting thì progress và eta_s là null, nên agent nhận 3 khoá. Test 5 khoá kiểm trước compact nên luôn qua. Sửa: miễn compact cho lỗi này và thêm test ở tầng MCP.
**Bài học:** Test phải kiểm đầu ra cuối cùng sau mọi lớp biến đổi, không chỉ kiểm lớp bên trong.
**Artefact:** Ví dụ JSON trước và sau khi compact (không có nội dung note).
