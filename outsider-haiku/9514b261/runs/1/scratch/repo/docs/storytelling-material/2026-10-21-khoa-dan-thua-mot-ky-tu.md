---
id: 2026-10-21-khoa-dan-thua-mot-ky-tu
date: 2026-10-21
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:9514b261#L3874", "claude:9514b261#L3895", "claude:9514b261#L3915", "claude:9514b261#L3920", "claude:9514b261#L3944", "claude:9514b261#L3949"]
hook: "Thừa đúng 1 ký tự, khoá mới làm cả hai công cụ chết"
tension: nho_ma_to
sides: ["Dán thừa một ký tự, 25 thay vì 24", "401 ở cả pi lẫn omp, khoá cũ bị ghi đè không sao lưu"]
strength: 3
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khoá dán thừa một ký tự, và lệnh ghi đè không sao lưu

**Bối cảnh:** Dán khoá API mới vào file đăng nhập của pi. omp đọc khoá từ đúng file đó.
**Chuyện gì xảy ra:** Khoá mới dài 25 ký tự, khoá cũ đang chạy được dài 24. API trả 401 cho cả pi lẫn omp, và gọi thẳng API cũng 401. Lệnh nhập đã ghi đè khoá cũ mà không sao lưu. Sau khi nhập lại và lọc khoảng trắng, khoá 24 ký tự nhận 200, bốn lượt kiểm pi và omp đều trả OK. Agent tự nhận lỗi vì lẽ ra phải đưa lệnh có sao lưu ngay từ đầu.
**Bài học:** Trước mọi lệnh ghi đè bí mật, sao lưu bằng cp -p sang file .bak. Khi dán khoá, lọc khoảng trắng và kiểm độ dài.
**Artefact:** Bảng kiểm pi và omp x model x kết quả. Không ghi giá trị khoá.
**Góc người ngoài:** cách làm phổ biến là Sửa config bằng script hoặc sửa tay, không sao lưu, và chỉ biết cách quay lại khi có lỗi; ở đây khác ở Mỗi thay đổi đều có một bản sao và một lệnh hoàn tác ghi trong báo cáo, nên người dùng có thể đảo lại ngay mà không cần tìm trong lịch sử.
