---
id: 2026-11-03-thu-cai-dat-cap-nhat-va-d5ef
code: M-ERC7
aliases: [M-ERC7]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L1225", "claude:ab9a1dd8#L1236", "claude:ab9a1dd8#L1846"]
hook: "Thử cài, cập nhật, gỡ trong HOME tạm, máy thật không đụng tới"
tension: none
sides: []
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thử cài đặt, cập nhật và gỡ cài đặt trong một HOME tạm (`mktemp`) với `env -i` và PATH trỏ tới các chương trình giả, nên không đụng tới cấu hình thật của máy.

**Chuyện gì xảy ra:** Thử cài đặt, cập nhật và gỡ cài đặt trong một HOME tạm (`mktemp`) với `env -i` và PATH trỏ tới các chương trình giả, nên không đụng tới cấu hình thật của máy.
**Góc người ngoài:** cách làm phổ biến là Hầu hết dev chạy thử trực tiếp trên máy mình, hoặc chỉ mock vài hàm trong unit test rồi tin kết quả; ở đây khác ở Cả vòng cài, cài lại, update và gỡ được chạy như người dùng thật trong môi trường cô lập, bằng script chạy lại được. Người đọc sẽ hỏi làm sao để không làm bẩn máy mình khi thử công cụ có sửa file cấu hình.
