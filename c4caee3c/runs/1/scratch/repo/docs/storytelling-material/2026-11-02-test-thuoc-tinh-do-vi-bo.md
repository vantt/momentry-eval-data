---
id: 2026-11-02-test-thuoc-tinh-do-vi-bo
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1659", "claude:c4caee3c#L1694"]
hook: "Gói đúng, test đỏ: lỗi nằm ở chính hàm đếm token của test"
tension: tuong_ma_hoa_ra
sides: ["Ai cũng ngờ gói tách từ sai", "Hàm đếm trong test mới là chỗ sai"]
strength: 3
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test thuộc tính đỏ vì bộ đếm token của chính test

**Bối cảnh:** Test property kiểm bất biến số token giữa các view. Hàm đếm token trong test khác với bộ tách token thật.
**Chuyện gì xảy ra:** Ký tự tổ hợp dính vào '+' hoặc '#' được bộ tách coi là một token, còn hàm đếm trong test lại tách khác. Gói đúng nhưng test đỏ ngẫu nhiên. Sửa hàm đếm cho khớp bộ tách, giữ nguyên phép kiểm. Chạy 20.000 lần vẫn qua.
**Bài học:** Hàm đếm trong test phải dùng đúng quy tắc của code thật, không tự viết lại một quy tắc khác.
**Artefact:** Ví dụ chuỗi đầu vào đã rút gọn.
