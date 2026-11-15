---
id: 2026-11-02-dau-ra-python-phu-thuoc-thu
date: 2026-11-02
repo: repo
status: raw
signals: [số trước sau, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L397", "claude:2dfb5915#L474"]
hook: "Đổi thứ tự liệt kê file, 593 trên 726 id đổi theo"
tension: nho_ma_to
sides: ["chỉ đổi thứ tự liệt kê file", "593 trên 726 id đổi"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đầu ra Python phụ thuộc thứ tự liệt kê file của hệ điều hành

**Bối cảnh:** Khi so index Rust với golden lấy từ Python, một số mục lệch dù logic đúng.
**Chuyện gì xảy ra:** Đảo thứ tự liệt kê file thì 593 trên 726 edges.id đổi, và điểm related lệch khoảng 1e-5, vượt ngưỡng 1e-6 của đặc tả. Python không sắp xếp đường dẫn nên kết quả phụ thuộc NTFS hay APFS. Quyết định ghim thứ tự theo đường dẫn đã sắp, ghi vào nhật ký quyết định, và phần index phải giữ đúng thứ tự này.
**Bài học:** Đầu ra của bản gốc có thể phụ thuộc môi trường. Tìm thứ tự ẩn trước khi viết bộ so khớp chặt.
**Artefact:** Bảng đếm số edges.id đổi theo thứ tự. Không ghi tên note.
