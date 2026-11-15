---
id: 2026-11-02-khi-ci-do-do-mot-kiem
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:c4caee3c#L3290", "claude:c4caee3c#L3311", "claude:c4caee3c#L3344", "claude:c4caee3c#L3349", "claude:c4caee3c#L3388", "claude:c4caee3c#L3415"]
hook: "CI đỏ vì test chập chờn: agent sửa phép so, không hạ ngưỡng"
tension: khac
sides: ["Cách quen thuộc là hạ ngưỡng cho xanh", "Agent sửa cổng so sánh trên cùng một lần chạy"]
strength: 1
stakes: 1
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khi CI đỏ do một kiểm tra không ổn định, agent tìm nguyên nhân qua báo cáo tải về và sửa cổng so sánh trên cùng một lần chạy thay vì dựa vào số đo lưu sẵn

**Chuyện gì xảy ra:** Khi CI đỏ do một kiểm tra không ổn định, agent tìm nguyên nhân qua báo cáo tải về và sửa cổng so sánh trên cùng một lần chạy thay vì dựa vào số đo lưu sẵn
**Góc người ngoài:** cách làm phổ biến là Thường người ta hạ ngưỡng hoặc cập nhật số đo cũ cho xanh lại; ở đây khác ở Phiên này phát hiện số đo khác nhau theo loại CPU của máy CI, nên sửa cổng so sánh cùng máy, không sửa số. Người đọc muốn biết cách phân biệt lỗi thật với lỗi do môi trường.
