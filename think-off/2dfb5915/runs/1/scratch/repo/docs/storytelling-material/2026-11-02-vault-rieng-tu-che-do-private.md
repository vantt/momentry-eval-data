---
id: 2026-11-02-vault-rieng-tu-che-do-private
date: 2026-11-02
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L83", "claude:2dfb5915#L397"]
hook: "Kiểm vault riêng tư mà đầu ra không chứa một tên note"
tension: none
sides: []
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Vault riêng tư: chế độ private chỉ in số lệch

**Bối cảnh:** Vault B là dữ liệu riêng tư của người dùng. Agent không được đọc nội dung.
**Chuyện gì xảy ra:** Chế độ --private chỉ in số lệch và không ghi gì vào vault. Đầu ra và report.json không chứa tên note, đường dẫn hay tên vault. Trên bản sao kg-solo với cờ giống vault B, 55 mục khớp. Chạy trên vault B thật vẫn chờ người dùng mở cổng.
**Bài học:** Thiết kế công cụ so khớp để đầu ra chỉ có số khi dữ liệu thật không được phép đọc.
**Artefact:** Ảnh đầu ra dạng số, đã che tên.
