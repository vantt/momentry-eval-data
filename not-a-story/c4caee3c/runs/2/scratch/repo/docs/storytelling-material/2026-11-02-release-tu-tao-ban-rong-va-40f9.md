---
id: 2026-11-02-release-tu-tao-ban-rong-va-40f9
code: M-8JB7
aliases: [M-8JB7]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2988", "claude:c4caee3c#L3001", "claude:c4caee3c#L3029", "claude:c4caee3c#L3875", "claude:c4caee3c#L3912"]
hook: "Release ra đời không có file, fixture ghim cũ hơn bộ eval"
tension: nho_ma_to
sides: ["Release tự động tưởng chạy đúng, fixture tưởng khớp", "Run dựng sớm hơn bản sửa nên ra bản rỗng; fixture v0.10.0 lệch golden v0.11.0"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Release tự tạo bản rỗng, và workflow ghim fixture cũ hơn bộ eval

**Bối cảnh:** Catchup tạo tag rồi gọi bước dựng gói. Bước dựng gói clone fixture ở một tag cố định.
**Chuyện gì xảy ra:** Release vantt.2 xuất hiện với mô tả đang dựng nhưng chưa có file, vì run dựng gói bắt đầu trước khi sửa điều kiện so sánh. Lead phải chạy lại bước dựng. Sau đó eval hai workflow hỏng vì fixture ghim v0.10.0 trong khi golden set đã sang v0.11.0. Đọc tag từ một nguồn duy nhất đã sửa lỗi.
**Bài học:** Hằng số phiên bản để ở hai nơi sẽ lệch. Đọc từ một nguồn duy nhất trong workflow.
