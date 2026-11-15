---
id: 2026-11-02-phat-hien-python-phu-thuoc-thu
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định có lý do]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1132"]
hook: "593 trên 726 id đổi chỉ vì hệ điều hành liệt kê file khác thứ tự"
tension: nho_ma_to
sides: ["Thứ tự liệt kê file của hệ điều hành, chuyện không ai để ý", "593/726 id đổi, điểm lệch 1e-5, vượt ngưỡng đặc tả"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Phát hiện Python phụ thuộc thứ tự liệt kê file của hệ điều hành

**Bối cảnh:** Bộ so khớp báo lệch ở edges.id và điểm related, dù code Rust đúng logic.
**Chuyện gì xảy ra:** Python liệt kê note theo thứ tự NTFS hoặc APFS trả về. Đảo thứ tự làm 593 trên 726 edges.id đổi, điểm related lệch khoảng 1e-5, vượt ngưỡng 1e-6 của đặc tả. Quyết định ghim thứ tự theo đường dẫn đã sắp và ghi vào DECISIONS.
**Bài học:** Kết quả phụ thuộc thứ tự file hệ thống là lỗi ẩn; so sánh hai bản phải đóng đúng thứ tự đó.
**Artefact:** Bảng số edges.id đổi và điểm related lệch.
