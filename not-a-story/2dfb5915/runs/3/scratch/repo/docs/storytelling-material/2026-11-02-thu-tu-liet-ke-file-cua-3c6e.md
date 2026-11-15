---
id: 2026-11-02-thu-tu-liet-ke-file-cua-3c6e
code: M-8MXR
aliases: [M-8MXR]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L423", "claude:2dfb5915#L474"]
hook: "Đảo thứ tự liệt kê file, 593 trên 726 id đổi"
tension: nho_ma_to
sides: ["Chỉ là thứ tự hệ điều hành liệt kê file", "593 trên 726 id đổi, điểm lệch 1e-5 vượt ngưỡng 1e-6"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thứ tự liệt kê file của hệ điều hành làm đầu ra Python đổi

**Bối cảnh:** Python liệt kê note theo thứ tự hệ điều hành trả về, thứ tự này khác nhau giữa NTFS và APFS.
**Chuyện gì xảy ra:** Khi đảo thứ tự liệt kê, 593 trên 726 edges.id đổi, và điểm related lệch khoảng 1e-5, vượt ngưỡng 1e-6 của PRD. Agent ghim thứ tự theo đường dẫn đã sắp và ghi vào nhật ký quyết định. Các phase sau phải giữ thứ tự này.
**Bài học:** Kết quả phụ thuộc thứ tự hệ điều hành là lỗi ẩn: kiểm tra xem đầu ra có đổi khi chỉ đổi thứ tự đầu vào không.
**Artefact:** Bảng số edges đổi theo thứ tự (không có dữ liệu riêng tư).
