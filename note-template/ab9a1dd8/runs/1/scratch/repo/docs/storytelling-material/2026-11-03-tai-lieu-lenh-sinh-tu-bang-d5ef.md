---
id: 2026-11-03-tai-lieu-lenh-sinh-tu-bang-d5ef
code: M-QWBG
aliases: [M-QWBG]
date: 2026-11-03
repo: repo
status: raw
signals: [khac]
signal_note: Cơ chế khoá tài liệu bằng test làm mọi thay đổi bảng lệnh buộc phải sinh lại tài liệu.
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L1663", "claude:ab9a1dd8#L1970", "claude:ab9a1dd8#L3388", "claude:ab9a1dd8#L3397"]
hook: "Đổi bảng lệnh là test đỏ, buộc tài liệu luôn khớp"
tension: it_ma_nhieu
sides: ["Chỉ một test so khớp tài liệu với bảng lệnh", "Bắt được mọi lần quên cập nhật tài liệu"]
strength: 1
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tài liệu lệnh sinh từ bảng lệnh, test khoá: đổi bảng là test đỏ

**Bối cảnh:** Tài liệu tham chiếu lệnh được sinh từ bảng lệnh trong code.
**Chuyện gì xảy ra:** Sau khi đổi bảng lệnh, test kiểm tài liệu có đúng với bảng không đã đỏ, và agent phải chạy lại script sinh tài liệu rồi mới qua test. Cơ chế này bắt được việc quên cập nhật tài liệu.
**Bài học:** Sinh tài liệu từ nguồn và khoá bằng test là cách rẻ để tài liệu không lệch code.
**Góc người ngoài:** cách làm phổ biến là Viết parser bằng tay, `--help` viết tay riêng, README mô tả lệnh viết tay; ba nguồn này lệch nhau theo thời gian mà không ai biết; ở đây khác ở Một nguồn sự thật cho lệnh, tài liệu không thể lệch vì test chặn. Người đọc sẽ hỏi cách làm test 'tài liệu còn đúng không' trong CLI của họ.
