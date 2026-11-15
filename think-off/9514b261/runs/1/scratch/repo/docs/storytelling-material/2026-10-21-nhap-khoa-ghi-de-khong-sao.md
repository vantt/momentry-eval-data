---
id: 2026-10-21-nhap-khoa-ghi-de-khong-sao
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3864", "claude:9514b261#L3899", "claude:9514b261#L3915", "claude:9514b261#L3949"]
hook: "Một ký tự thừa lúc dán làm cả bốn lượt kiểm trả 401"
tension: nho_ma_to
sides: ["một ký tự thừa khi dán khoá", "cả bốn lượt kiểm trả 401, khoá cũ đã bị ghi đè không sao lưu"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Nhập khoá ghi đè không sao lưu: 401, rồi một ký tự thừa lúc dán

**Bối cảnh:** Chủ máy dán khoá nhà cung cấp mới vào tài khoản pi đang chạy, và omp dùng chung khoá đó.
**Chuyện gì xảy ra:** Lệnh nhập ghi đè khoá cũ mà không sao lưu. Khoá mới dài 25 ký tự, khoá cũ dài 24 và vẫn chạy được. API trả 401 cho cả bốn lượt kiểm. Nguyên nhân gần là một ký tự thừa lúc dán. Sau khi cắt khoảng trắng và sao lưu, API trả 200 và bốn lượt pi/omp đều trả OK.
**Bài học:** Sao lưu trước khi ghi đè khoá, xoá khoảng trắng khi dán, và kiểm bằng một lệnh gọi API trước khi bỏ khoá cũ.
**Artefact:** Bảng 401 trước và OK sau, chỉ có mã trạng thái và độ dài khoá, không có giá trị.
