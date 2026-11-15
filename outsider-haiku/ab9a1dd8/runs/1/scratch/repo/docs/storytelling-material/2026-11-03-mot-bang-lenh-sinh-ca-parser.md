---
id: 2026-11-03-mot-bang-lenh-sinh-ca-parser
date: 2026-11-03
repo: repo
status: raw
signals: [artefact]
source: "chat Claude, claude:ab9a1dd8"
sessions: ["claude:ab9a1dd8"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:ab9a1dd8#L959", "claude:ab9a1dd8#L1424", "claude:ab9a1dd8#L1663", "claude:ab9a1dd8#L2230"]
hook: "Một bảng lệnh sinh parser, help và tài liệu; quên sinh lại là test đỏ"
tension: it_ma_nhieu
sides: ["một bảng lệnh duy nhất", "sinh ra parser, --help và tài liệu tham chiếu"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Một bảng lệnh sinh cả parser, --help và tài liệu tham chiếu

**Bối cảnh:** Trước đó --help chỉ in một dòng cú pháp, init --help không có mô tả hay ví dụ.
**Chuyện gì xảy ra:** Một bảng lệnh định nghĩa cờ, mô tả, ví dụ và mã thoát. Parser và help đọc từ bảng đó. Tài liệu docs/cli-reference.md được sinh từ bảng và có test kiểm tra độ lệch, nên quên sinh lại là test đỏ.
**Bài học:** Một nguồn sự thật cho lệnh giúp help, tài liệu và parser không lệch nhau; hãy thêm test kiểm độ lệch.
**Artefact:** Đoạn --help trước và sau khi có bảng lệnh.
**Góc người ngoài:** cách làm phổ biến là Viết parser bằng tay (hoặc thư viện), viết `--help` riêng bằng chuỗi văn bản, rồi tài liệu lệnh viết lại bằng tay; ba nguồn này dần lệch nhau; ở đây khác ở Một nguồn sự thật, tài liệu luôn đúng với code, và có test chặn việc tài liệu bị lệch. Người đọc sẽ hỏi vì sao không cần đồng bộ thủ công.
