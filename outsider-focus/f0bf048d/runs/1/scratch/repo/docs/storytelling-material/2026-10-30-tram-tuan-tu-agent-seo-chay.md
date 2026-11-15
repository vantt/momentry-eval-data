---
id: 2026-10-30-tram-tuan-tu-agent-seo-chay
date: 2026-10-30
repo: repo
status: raw
signals: ["số trước, số sau", nguyên nhân bất ngờ]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L749", "claude:f0bf048d#L773", "claude:f0bf048d#L783", "claude:f0bf048d#L789", "claude:f0bf048d#L915", "claude:f0bf048d#L923", "claude:f0bf048d#L963"]
hook: "Key service account đăng nhập đúng, nhưng GA4 trả về rỗng"
tension: tuong_ma_hoa_ra
sides: ["Xác thực chạy được", "Key chưa có quyền vào property nên số liệu rỗng, khó biết xác thực có chạy không"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trạm tuần tự: agent SEO chạy được trên MCP GA4 và Search Console thật, nhưng key bị thiếu quyền đọc

**Bối cảnh:** Một bộ agent SEO và Analytics được dựng cho khách marketing trên Multica, gọi GA4 và Search Console qua MCP server cài sẵn trên máy agent.
**Chuyện gì xảy ra:** Lần thử đầu, key service account trả về rỗng vì chưa được cấp quyền vào property, nên khó biết xác thực có chạy không. Sau khi cấp quyền, run_report qua MCP trả về số liệu thật, ví dụ kênh Direct 58 session trong 7 ngày. Search Console ban đầu không có số liệu vì property đang trỏ bản www cũ, trong khi website đã redirect 301 sang bản không www. Lần chạy agent đầu tiên (STU-6) bị blocked vì file key không được chép đúng vào home của user daemon, dù bước cài MCP đã thành công.
**Bài học:** Kiểm xác thực với key trước khi cấp quyền cho người dùng, và kiểm file secret được đặt đúng quyền đọc cho user chạy daemon, không chỉ kiểm binary cài đặt.
**Artefact:** Bảng kết quả tool list GA4 (9 tool) và Search Console (8 tool); che property ID, email service account, domain khách.
