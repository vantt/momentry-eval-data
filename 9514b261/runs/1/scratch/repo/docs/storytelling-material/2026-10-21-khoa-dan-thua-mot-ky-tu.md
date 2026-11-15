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
hook: "Dán thừa một ký tự, khoá chạy được bị ghi đè mất"
tension: nho_ma_to
sides: ["một ký tự thừa trong khoá", "401 khắp nơi và khoá cũ đang chạy bị ghi đè"]
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
**Góc người ngoài:** cách làm phổ biến là Phần lớn dev sửa tay bằng editor hoặc sed, hoặc chỉ dựa vào git; file nằm ngoài repo như ~/.zshrc thường không có bản sao lưu; ở đây khác ở Người đọc sẽ hỏi cách sửa file cấu hình sống mà vẫn quay lại được và không phá định dạng. Phiên này còn kèm bài học ngược: một lệnh do chính agent đưa ra đã ghi đè khoá mà không sao lưu, nên thói quen này cần áp cả cho lệnh đưa cho người dùng chạy.
