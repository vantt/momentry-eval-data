---
id: 2026-10-21-truoc-moi-lan-sua-config-hoac
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:9514b261#L2422", "claude:9514b261#L2431", "claude:9514b261#L3038", "claude:9514b261#L3102", "claude:9514b261#L3148", "claude:9514b261#L3852"]
hook: "Sửa dotfile mà có bản sao lưu dấu thời gian, gỡ chỉ cần chép đè"
tension: none
sides: []
strength: 0
stakes: 0
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước mỗi lần sửa config hoặc dotfile, agent sao lưu bản gốc kèm dấu thời gian, kiểm cú pháp (zsh -n), rồi kiểm hành vi thật (alias hiển thị đúng, probe trả OK). Khi cần gỡ, chỉ cần chép đè bản sao lưu.

**Chuyện gì xảy ra:** Trước mỗi lần sửa config hoặc dotfile, agent sao lưu bản gốc kèm dấu thời gian, kiểm cú pháp (zsh -n), rồi kiểm hành vi thật (alias hiển thị đúng, probe trả OK). Khi cần gỡ, chỉ cần chép đè bản sao lưu.
**Góc người ngoài:** cách làm phổ biến là Thường sửa trực tiếp file rồi mở shell mới xem có lỗi không. Ít ai giữ bản sao lưu có dấu thời gian; ở đây khác ở Mọi thay đổi đều có đường lùi rõ ràng và có bằng chứng sau khi sửa, nên sửa cấu hình toàn cục ít rủi ro hơn nhiều.
