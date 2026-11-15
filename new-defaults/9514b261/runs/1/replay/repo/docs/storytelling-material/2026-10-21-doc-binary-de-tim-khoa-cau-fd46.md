---
id: 2026-10-21-doc-binary-de-tim-khoa-cau-fd46
code: M-QD47
aliases: [M-QD47]
date: 2026-10-21
repo: repo
status: raw
signals: [khac]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3698", "claude:9514b261#L3747", "claude:9514b261#L3757", "claude:9514b261#L3808", "claude:9514b261#L3819"]
hook: "CLI không có tài liệu, agent đào chuỗi trong binary 256 MB để cấu hình"
tension: it_ma_nhieu
sides: ["Không có tài liệu nào để dựa vào", "Lệnh strings trên binary 256 MB cho ra đúng khoá cấu hình sau khoảng năm lượt"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đọc binary để tìm khoá cấu hình provider của omp khi CLI không có tài liệu

**Bối cảnh:** omp không có cờ liệt kê model. Cần khai một provider tuỳ chọn cho TheHive.
**Chuyện gì xảy ra:** Agent không tìm được tài liệu nên dùng strings trên binary 256 MB để tìm chuỗi models.yml và các khoá như baseUrl và apiKey. Sau khoảng năm lượt tìm kiếm mới có kết quả đủ dùng. Agent viết models.yml với khoá lấy bằng lệnh jq lúc chạy. omp liệt kê đúng hai model và lượt gọi thử trả OK.
**Bài học:** Với CLI thiếu tài liệu, strings trên binary cho ra tên khoá cấu hình. Đặt khoá bí mật qua lệnh chạy lúc gọi, không ghi thẳng vào file.
**Artefact:** Ví dụ models.yml với khoá đã che.
