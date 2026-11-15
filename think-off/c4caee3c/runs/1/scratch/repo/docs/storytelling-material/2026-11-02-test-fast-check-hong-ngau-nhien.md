---
id: 2026-11-02-test-fast-check-hong-ngau-nhien
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1659", "claude:c4caee3c#L1694", "claude:c4caee3c#L1820"]
hook: "Test tự đếm sai token, báo lỗi trong khi gói hoàn toàn đúng"
tension: tuong_ma_hoa_ra
sides: ["Tưởng gói có lỗi vì test đỏ ngẫu nhiên", "Hàm đếm token của chính test mới sai"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test fast-check hỏng ngẫu nhiên vì hàm đếm token của chính test

**Bối cảnh:** Gói tiếng Việt có một property test kiểm bất biến số token qua mọi view và mọi tuỳ chọn. Test này thỉnh thoảng hỏng từ thời V13 và cả trên master.
**Chuyện gì xảy ra:** Test thay dấu + và # bằng khoảng trắng trước khi đếm token. Chuỗi như mũi tên cộng dấu kết hợp U+0338 cộng # bị tokenizer đọc thành một token, nhưng sau khi thay thì test đếm khác, nên báo lỗi dù gói đúng. Agent viết helper đếm đúng như tokenizer của view, giữ nguyên phép kiểm, thêm test hồi quy và xác nhận qua 20.000 lần chạy.
**Bài học:** Khi test ngẫu nhiên hỏng, kiểm trước xem bộ đếm trong test có khớp với hành vi thật không, đừng vội sửa mã sản phẩm.
**Artefact:** Ví dụ một chuỗi nhỏ có dấu kết hợp, kèm kết quả đếm token trước và sau.
