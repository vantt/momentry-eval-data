---
id: 2026-10-21-khong-co-tai-lieu-agent-do-fd46
code: M-BPMF
aliases: [M-BPMF]
date: 2026-10-21
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L3636", "claude:9514b261#L3637", "claude:9514b261#L3649", "claude:9514b261#L3751", "claude:9514b261#L3761", "claude:9514b261#L3774", "claude:9514b261#L3808", "claude:9514b261#L3823"]
hook: "Không có tài liệu, agent đọc chuỗi trong binary và gọi được omp"
tension: it_ma_nhieu
sides: ["Không có tài liệu, hook chặn đường tìm thông thường", "Chỉ dùng strings trên binary là viết đúng models.yml và nhận OK"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Không có tài liệu, agent dò định dạng cấu hình omp từ chuỗi trong binary

**Bối cảnh:** Omp không có tài liệu cấu hình provider tuỳ chọn trên máy. Binary omp nặng khoảng 256 MB.
**Chuyện gì xảy ra:** Hook chặn lệnh tìm trong node_modules nên agent đổi cách tìm. Dùng strings trên binary, agent tìm thấy tên file models.yml xuất hiện 25 lần và một chuỗi lỗi nói khoá apiKey không được gửi qua tài khoản OAuth pool. Từ đó agent viết models.yml với khoá lấy bằng lệnh jq lúc chạy, rồi gọi thử và nhận OK.
**Bài học:** Khi thiếu tài liệu, grep chuỗi trong binary để tìm tên file cấu hình và thông báo lỗi, rẻ và hiệu quả.
**Artefact:** Chuỗi lỗi từ binary (không chứa bí mật) và cấu trúc models.yml không kèm khoá.
