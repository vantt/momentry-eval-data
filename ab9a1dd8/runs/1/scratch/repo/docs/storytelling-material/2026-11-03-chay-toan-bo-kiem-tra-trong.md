---
id: 2026-11-03-chay-toan-bo-kiem-tra-trong
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L101", "claude:ab9a1dd8#L110", "claude:ab9a1dd8#L1225", "claude:ab9a1dd8#L1236", "claude:ab9a1dd8#L1377", "claude:ab9a1dd8#L1385", "claude:ab9a1dd8#L3902"]
hook: "Thử cài, update, xoá installer mà máy thật không bị đụng"
tension: it_ma_nhieu
sides: ["Chỉ một HOME tạm với env -i", "Thử cả vòng đời installer, máy thật nguyên vẹn"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Chạy toàn bộ kiểm tra trong HOME tạm (mktemp) với `env -i`, cache và cấu hình riêng, nên thử cài, init, update, uninstall mà không đụng máy thật của user

**Chuyện gì xảy ra:** Chạy toàn bộ kiểm tra trong HOME tạm (mktemp) với `env -i`, cache và cấu hình riêng, nên thử cài, init, update, uninstall mà không đụng máy thật của user
**Góc người ngoài:** cách làm phổ biến là Dev thường chạy thử installer hoặc CLI thẳng trên máy mình, hoặc dựng Docker/VM; cùng lắm backup dotfiles trước rồi sửa tay nếu hỏng; ở đây khác ở Chỉ cần đổi biến HOME và xoá sạch môi trường là có một máy 'mới tinh' trong vài giây, không cần container. Người đọc muốn thử công cụ cài vào ~/.claude hay ~/.codex mà không sợ làm hỏng cấu hình thật sẽ muốn mẹo này.
