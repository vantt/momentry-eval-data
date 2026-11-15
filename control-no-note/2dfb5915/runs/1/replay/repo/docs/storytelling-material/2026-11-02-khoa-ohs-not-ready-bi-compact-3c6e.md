---
id: 2026-11-02-khoa-ohs-not-ready-bi-compact-3c6e
code: M-47VW
aliases: [M-47VW]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3060", "claude:2dfb5915#L3110"]
hook: "Test 5 khoá xanh, nhưng agent chỉ nhận được 3 khoá"
tension: tuong_ma_hoa_ra
sides: ["Test kiểm đủ 5 khoá và qua", "Compact xoá 2 khoá null, agent chỉ nhận 3"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay lõi Python bằng Rust, và người làm đang chốt interface MCP cho nó. Hợp đồng lỗi ohs_not_ready phải trả đủ 5 khoá, và test cũ đã kiểm 5 khoá trước bước nén. Nhưng bước nén bỏ khoá null nên agent chỉ nhận 3 khoá khi OHS đang khởi động hoặc lỗi. Ai viết test cho API có bước lọc dữ liệu cuối cùng nên kiểm kết quả ở tầng người dùng thấy."
audience: dev viết test cho API có bước lọc dữ liệu
spine_context: "Công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian, đang thay lõi Python bằng Rust."
spine_context_lines: [profile, "claude:2dfb5915#L3027"]
spine_want: "Muốn chốt interface MCP cho tool hỏi graph, ít lượt gọi và ít token."
spine_want_lines: ["claude:2dfb5915#L3027", "claude:2dfb5915#L3039"]
spine_obstacle: "Khi OHS đang starting, model_missing hay broken, kết quả tool thiếu khoá."
spine_obstacle_lines: ["claude:2dfb5915#L3110"]
spine_turn: "Tưởng test 5 khoá đảm bảo agent nhận đủ 5 khoá; hoá ra compact() xoá khoá null sau test, agent chỉ nhận 3."
spine_turn_lines: ["claude:2dfb5915#L3100", "claude:2dfb5915#L3110"]
spine_action: "Hai agent đọc code, xác nhận compact() gây lỗi; đề xuất miễn ngoại lệ cho ohs_not_ready và thêm test ở tầng MCP."
spine_action_lines: ["claude:2dfb5915#L3060", "claude:2dfb5915#L3110"]
spine_takeaway: "Test ở tầng người dùng nhận được, không chỉ ở tầng trước khi dữ liệu bị biến đổi."
spine_takeaway_lines: ["claude:2dfb5915#L3110"]
completeness: 6
---

# Khoá ohs_not_ready bị compact() xoá, test không bắt được

**Góc kể:** Một công cụ dòng lệnh hỏi Claude Desktop về graph vault Obsidian đang thay lõi Python bằng Rust, và người làm đang chốt interface MCP cho nó. Hợp đồng lỗi ohs_not_ready phải trả đủ 5 khoá, và test cũ đã kiểm 5 khoá trước bước nén. Nhưng bước nén bỏ khoá null nên agent chỉ nhận 3 khoá khi OHS đang khởi động hoặc lỗi. Ai viết test cho API có bước lọc dữ liệu cuối cùng nên kiểm kết quả ở tầng người dùng thấy.
**Bối cảnh:** Mọi kết quả tool đi qua hàm compact() để bỏ khoá rỗng.
**Chuyện gì xảy ra:** Ở trạng thái starting, model_missing hay broken, progress và eta_s là null, nên compact xoá chúng và agent chỉ nhận 3 khoá thay vì 5. Test 5 khoá kiểm trước khi compact nên không bắt được. Fix là miễn compact cho lỗi ohs_not_ready và thêm test ở tầng MCP.
**Bài học:** Test ở đúng tầng mà người dùng nhìn thấy, không chỉ ở tầng nội bộ trước khi biến đổi.
