---
id: 2026-10-30-tach-thiet-lap-workspace-khach-khoi
date: 2026-10-30
repo: repo
status: raw
signals: ["5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1174", "claude:f0bf048d#L1178"]
hook: "Gói tên opc-studio gây nhầm vì đó là workspace của chính mình"
tension: none
sides: []
strength: 0
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tách thiết lập workspace khách khỏi gắn bộ nghiệp vụ

**Bối cảnh:** Mỗi khách có một workspace riêng và mua các bộ nghiệp vụ khác nhau (content, SEO, coding).
**Chuyện gì xảy ra:** Tên gói opc-studio gây nhầm vì nó là workspace của chính mình. Đổi gói thành opc-content, bỏ deploy mặc định vào opc-studio, và dựng hai lớp: workspace của khách (một lần) và các bộ nghiệp vụ (gắn thêm hoặc gỡ theo gói khách mua).
**Bài học:** Tách thiết lập nền (workspace, thành viên, hạ tầng) khỏi việc gắn bộ nghiệp vụ, để khách mua thêm hoặc bỏ bộ nào cũng không phải dựng lại.
**Artefact:** Sơ đồ hai lớp: workspace khách và các bộ nghiệp vụ.
**Góc người ngoài:** cách làm phổ biến là Cấu hình agent thường nằm rải rác trong UI, deploy bằng tay, không có bước xem trước; khi đổi thì thường ghi đè mà không biết; ở đây khác ở Có plan trước khi deploy và manifest theo khách. Người đọc sẽ muốn biết cách làm để tránh sự cố ghi đè kiểu deploy gói thứ hai.
