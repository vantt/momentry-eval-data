---
id: 2026-11-02-npm-12-doi-hinh-dang-dau
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L3474", "claude:c4caee3c#L3486", "claude:c4caee3c#L3491", "claude:c4caee3c#L3745"]
hook: "npm 12 đổi đầu ra npm pack: mảng thành object, test đóng gói đỏ"
tension: nho_ma_to
sides: ["Chỉ đổi dạng đầu ra của một lệnh", "Test đóng gói trên CI đỏ vì .files thành undefined"]
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
