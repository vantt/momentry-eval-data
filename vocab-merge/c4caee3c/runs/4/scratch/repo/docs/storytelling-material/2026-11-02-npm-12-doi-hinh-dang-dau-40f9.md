---
id: 2026-11-02-npm-12-doi-hinh-dang-dau-40f9
code: M-V75Y
aliases: [M-V75Y]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3474", "claude:c4caee3c#L3486", "claude:c4caee3c#L3491", "claude:c4caee3c#L3745"]
hook: "npm 12 đổi dạng đầu ra, khiến .files thành undefined trên CI"
tension: nho_ma_to
sides: ["nâng một phiên bản npm", "đầu ra đổi từ mảng sang object, test đóng gói đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# npm 12 đổi hình dạng đầu ra npm pack --json, test đóng gói đỏ trên CI

**Bối cảnh:** Catchup chạy npm 12 trước trong PATH, còn test đọc kết quả npm pack như một mảng.
**Chuyện gì xảy ra:** npm 11 trả về mảng, npm 12 trả về object có khoá là tên gói, nên truy cập .files thành undefined. Sửa: đọc được cả hai dạng, kiểm bằng npm 12 thật thấy đủ bốn file dữ liệu.
**Bài học:** Test đọc đầu ra của CLI phải chịu được nhiều dạng khi CI dùng phiên bản khác máy dev.
