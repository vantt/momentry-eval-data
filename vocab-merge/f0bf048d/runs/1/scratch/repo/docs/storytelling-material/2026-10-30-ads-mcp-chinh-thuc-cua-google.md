---
id: 2026-10-30-ads-mcp-chinh-thuc-cua-google
date: 2026-10-30
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, artefact]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1311", "claude:f0bf048d#L1345"]
hook: "Meta cho tạo chiến dịch quảng cáo, nhưng luôn ở trạng thái paused"
tension: khac
sides: ["MCP Meta đọc và sửa được", "chiến dịch tạo ra luôn paused, Google Ads chỉ đọc"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ads: MCP chính thức của Google chỉ đọc, Meta tạo chiến dịch ở trạng thái paused

**Bối cảnh:** Khảo sát công cụ Ads cho một bộ có thể đọc và sửa tài khoản quảng cáo của khách.
**Chuyện gì xảy ra:** Google Ads có MCP chính thức chỉ đọc (0.0.5, Apache-2.0), dùng developer token của agency. Meta có MCP do nền tảng host, đọc và sửa được, nhưng chiến dịch tạo ra luôn ở trạng thái paused. TikTok đăng nhập OAuth phải làm lại mỗi 30 ngày. LinkedIn chưa có bản chính thức. MCP host qua HTTP buộc gói có kiểu cấu hình url và headers.
**Bài học:** Chọn công cụ chỉ đọc trước, và mặc định thao tác tốn tiền ở trạng thái không chạy (paused).
**Artefact:** Bảng so sánh công cụ Ads theo đọc/sửa và điều khách phải cấp.
