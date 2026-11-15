---
id: 2026-11-02-test-tinh-chat-bao-do-vi-40f9
code: M-XZGY
aliases: [M-XZGY]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1659", "claude:c4caee3c#L1688", "claude:c4caee3c#L1694"]
hook: "Test báo đỏ, nhưng lỗi nằm ở chính hàm đếm của test"
tension: tuong_ma_hoa_ra
sides: ["Test đỏ, tưởng gói sai", "Gói đúng, hàm đếm của test mới sai"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test tính chất báo đỏ vì chính hàm đếm của test

**Bối cảnh:** Một property test kiểm bất biến số token giữa gói và view. Test chạy 400 lần ngẫu nhiên.
**Chuyện gì xảy ra:** Test đếm token sau khi thay dấu cộng và dấu thăng bằng khoảng trắng. Chuỗi có chữ cái cộng dấu tổ hợp U+0338 và dấu thăng được tokenizer đọc thành một token, nhưng sau khi thay thì test đếm ra không có token nào ở nguồn. Gói vẫn đúng. Sửa bằng cách thêm hàm đếm đúng như tokenizer, giữ nguyên tính chất. Chạy 20.000 lần vẫn qua.
**Bài học:** Khi test đỏ ngẫu nhiên, kiểm chính helper của test trước khi nghi code sản phẩm.
