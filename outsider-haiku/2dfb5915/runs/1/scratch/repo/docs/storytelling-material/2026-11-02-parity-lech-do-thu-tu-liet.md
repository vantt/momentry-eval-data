---
id: 2026-11-02-parity-lech-do-thu-tu-liet
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ, số trước số sau]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L1426", "claude:2dfb5915#L2880"]
hook: "593/726 id đổi chỉ vì Windows liệt kê file khác thứ tự"
tension: nho_ma_to
sides: ["Chỉ khác thứ tự liệt kê file của hệ điều hành", "593 trên 726 id đổi, điểm lệch vượt dung sai"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Parity lệch do thứ tự liệt kê file của hệ điều hành, không phải do thuật toán

**Bối cảnh:** Bộ so khớp Rust với Python phải khớp từng byte đầu ra index và kết quả PageRank (dung sai 1e-6).
**Chuyện gì xảy ra:** Python liệt kê file theo thứ tự NTFS/APFS trả về, nên đổi thứ tự thì 593 trên 726 `edges.id` đổi, và điểm `related` lệch khoảng 1e-5, vượt dung sai PRD. Agent không nới dung sai mà ghim thứ tự liệt kê theo đường dẫn đã sắp, ghi vào DECISIONS, và yêu cầu phase sau giữ đúng thứ tự này.
**Bài học:** Khi so khớp hai bản triển khai, kiểm xem đầu ra có phụ thuộc thứ tự hệ điều hành trả về trước khi nghi thuật toán.
**Artefact:** Bảng đếm số edge đổi theo thứ tự file (593/726) và sai số điểm.
