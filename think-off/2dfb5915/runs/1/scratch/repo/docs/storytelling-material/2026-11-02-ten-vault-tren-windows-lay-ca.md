---
id: 2026-11-02-ten-vault-tren-windows-lay-ca
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1364"]
hook: "Trên Windows, tên vault thành cả đường dẫn ổ C"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tên vault trên Windows lấy cả đường dẫn đầy đủ

**Bối cảnh:** Hai test MCP đỏ trên Windows trong khi Linux xanh.
**Chuyện gì xảy ra:** Hàm basename chỉ tách theo dấu gạch chéo xuôi, nên trên Windows tên vault thành cả đường dẫn ổ C. Tên đó đi vào instructions và link mở vault. Python dùng ntpath.basename, tách cả hai loại dấu và bỏ ký tự ổ đĩa. Bản Rust được sửa theo Python.
**Bài học:** Với đường dẫn Windows, kiểm cả hai loại dấu phân cách và đối chiếu với hàm tương ứng bên đặc tả.
**Artefact:** Không có.
