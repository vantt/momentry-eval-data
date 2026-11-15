---
id: 2026-10-30-kiem-mcp-bang-bat-tay-stdio-f60d
code: M-RD0X
aliases: [M-RD0X]
date: 2026-10-30
repo: repo
status: raw
signals: [artefact, số trước/sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L427", "claude:f0bf048d#L456", "claude:f0bf048d#L773", "claude:f0bf048d#L783"]
hook: "Search Console trả rỗng dù GA4 báo 58 session Direct trong 7 ngày"
tension: tuong_ma_hoa_ra
sides: ["Cả hai server đều kết nối và liệt kê tool thành công", "Search Console không trả dữ liệu vì thiếu quyền đúng property"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Kiểm MCP bằng bắt tay stdio thật: GA4 trả 9 tool, Search Console 8 tool, run_report ra số liệu

**Bối cảnh:** Cần chắc MCP chạy được với PATH tối giản dưới user daemon, không chỉ đúng cú pháp.
**Chuyện gì xảy ra:** Khởi động từng server và gọi tools/list: GA4 có 9 tool, Search Console có 8 tool. Gọi run_report GA4 và nhận số liệu thật; kênh Direct có 58 session trong 7 ngày. Search Console trả rỗng vì chưa có quyền đúng property.
**Bài học:** Kiểm công cụ bằng giao thức thật trong môi trường giống như daemon sẽ chạy, không chỉ bằng lint.
**Artefact:** Bảng tool liệt kê và một dòng số liệu đã che.
