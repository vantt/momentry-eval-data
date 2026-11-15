---
id: 2026-11-03-khi-mot-cong-cu-ben-thu-d5ef
code: M-TAPC
aliases: [M-TAPC]
date: 2026-11-03
repo: repo
status: raw
signals: []
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:ab9a1dd8#L3117", "claude:ab9a1dd8#L3121", "claude:ab9a1dd8#L3149", "claude:ab9a1dd8#L3157", "claude:ab9a1dd8#L3166", "claude:ab9a1dd8#L3176"]
hook: "Đoán mò cách tính hash của Codex, hay đọc thẳng mã nguồn"
tension: it_ma_nhieu
sides: ["Chỉ đọc mã nguồn mở của Codex qua API GitHub", "Tìm đúng hàm tính hash và cả cờ bỏ qua bước đó, thay vì đoán nhiều lần"]
strength: 2
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi một công cụ bên thứ ba có cơ chế không rõ (cách tính hash tin cậy của Codex), agent đọc mã nguồn mở của nó qua API của GitHub, tìm đúng hàm, và tìm cả cờ bỏ qua bước đó.

**Chuyện gì xảy ra:** Khi một công cụ bên thứ ba có cơ chế không rõ (cách tính hash tin cậy của Codex), agent đọc mã nguồn mở của nó qua API của GitHub, tìm đúng hàm, và tìm cả cờ bỏ qua bước đó.
**Góc người ngoài:** cách làm phổ biến là Đoán thử nhiều lần, hoặc bỏ qua và ghi chú là chưa kiểm được; ở đây khác ở Mã nguồn công khai là nguồn xác thực rẻ nhất, và người đọc sẽ muốn biết agent tìm đúng chỗ bằng cách nào.
