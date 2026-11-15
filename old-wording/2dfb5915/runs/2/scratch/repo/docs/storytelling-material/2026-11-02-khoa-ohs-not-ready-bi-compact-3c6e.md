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
hook: "Test 5 khoá xanh, nhưng agent thực tế chỉ nhận 3 khoá"
tension: tuong_ma_hoa_ra
sides: ["Test kiểm đủ 5 khoá nên tưởng an toàn", "compact xoá 2 khoá null sau bước kiểm"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khoá ohs_not_ready bị compact() xoá, test không bắt được

**Bối cảnh:** Mọi kết quả tool đi qua hàm compact() để bỏ khoá rỗng.
**Chuyện gì xảy ra:** Ở trạng thái starting, model_missing hay broken, progress và eta_s là null, nên compact xoá chúng và agent chỉ nhận 3 khoá thay vì 5. Test 5 khoá kiểm trước khi compact nên không bắt được. Fix là miễn compact cho lỗi ohs_not_ready và thêm test ở tầng MCP.
**Bài học:** Test ở đúng tầng mà người dùng nhìn thấy, không chỉ ở tầng nội bộ trước khi biến đổi.
