---
id: 2026-11-02-dau-ra-python-doi-theo-thu-3c6e
code: M-P9XX
aliases: [M-P9XX]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L423", "claude:2dfb5915#L474"]
hook: "593 trên 726 id đổi chỉ vì thứ tự liệt kê file"
tension: nho_ma_to
sides: ["Cùng mã, cùng dữ liệu đầu vào", "Thứ tự hệ điều hành trả file làm kết quả lệch"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Đầu ra Python đổi theo thứ tự hệ điều hành liệt kê file

**Bối cảnh:** Bộ so khớp so chặt từng cạnh (edges.id) và điểm related với sai số 1e-6.
**Chuyện gì xảy ra:** Python không có ORDER BY, nên thứ tự cạnh phụ thuộc thứ tự hệ điều hành trả về. Thử đảo thứ tự cho thấy 593 trên 726 edges.id đổi và điểm related lệch khoảng 1e-5, vượt ngưỡng. Chốt sắp xếp theo đường dẫn, ghi vào quyết định.
**Bài học:** Đầu ra không có ORDER BY là nguồn lệch ẩn; ghim thứ tự ngay từ đầu.
