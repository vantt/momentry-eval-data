---
id: 2026-10-21-dan-khoa-thua-mot-ky-tu
date: 2026-10-21
repo: repo
status: raw
signals: ["gốc nhỏ, lỗi to", đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L3874", "claude:9514b261#L3920", "claude:9514b261#L3930", "claude:9514b261#L3949"]
hook: "Dán thừa đúng 1 ký tự, khoá cũ đang chạy bị ghi đè mất luôn"
tension: nho_ma_to
sides: ["Khoá mới chỉ thừa 1 ký tự (25 thay vì 24)", "API trả 401 và khoá cũ đang chạy đã bị ghi đè, không có bản sao lưu"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Dán khoá thừa một ký tự, API từ chối 401, ghi đè khoá cũ không sao lưu

**Bối cảnh:** Người dùng nhập khoá API mới cho một nhà cung cấp dùng chung pi và omp, lệnh nhập ghi đè file auth cũ.
**Chuyện gì xảy ra:** Khoá mới dài 25 ký tự, API trả 401 khi gọi cả trực tiếp. Khoá cũ đã chạy được nhưng không có bản sao lưu vì lệnh ghi đè không sao lưu trước. Sau khi nhập lại có bước tr để bỏ khoảng trắng và curl kiểm trước, khoá dài 24 ký tự và trả 200, pi và omp đều trả OK.
**Bài học:** Luôn sao lưu trước khi ghi đè bí mật, và luôn trim khi dán khoá. Kiểm bằng gọi API trực tiếp, đừng chỉ kiểm CLI.
**Artefact:** Sơ đồ quy trình nhập khoá có bước sao lưu, trim và kiểm curl (không có giá trị khoá).
