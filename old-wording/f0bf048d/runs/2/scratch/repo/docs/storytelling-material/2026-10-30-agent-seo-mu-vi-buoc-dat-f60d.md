---
id: 2026-10-30-agent-seo-mu-vi-buoc-dat-f60d
code: M-QMGQ
aliases: [M-QMGQ]
date: 2026-10-30
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L954", "claude:f0bf048d#L963", "claude:f0bf048d#L975"]
hook: "Agent SEO mù vì sót một lệnh sudo đặt key"
tension: nho_ma_to
sides: ["một bước tay đặt file key bị sót", "cả agent SEO không làm được việc"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một team marketing đang dựng agent AI làm SEO, GA4 và Search Console để agent tự làm việc, không chỉ có người làm. Khi chạy thử, agent SEO báo blocked: phần cài MCP đã xong, nên việc tưởng là agent đã chạy được, nhưng file key Google chưa được đặt, agent không đọc được gì. Lỗi nằm ở gói chứ không ở agent, vì bước chép key bằng tay dễ bị sót. Ai dựng agent cho team không rành kỹ thuật nên nghe, vì một bước tay bị sót có thể làm agent mù mà không báo rõ ngay."
audience: dev và người dựng agent AI cho team nghiệp vụ
spine_context: "Một team marketing đang dựng agent AI làm SEO, GA4 và Search Console, để agent tự làm việc thay vì chỉ có người làm."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L946"]
spine_want: "Muốn agent có đủ công cụ để tự làm việc, và khi deploy lại team thì đủ cả agent lẫn công cụ."
spine_want_lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L968"]
spine_obstacle: Agent SEO chạy thử báo blocked vì không đọc được file key Google.
spine_obstacle_lines: ["claude:f0bf048d#L963"]
spine_turn: Tưởng cài MCP xong là agent chạy được; hoá ra thiếu file key nên agent không đọc được gì.
spine_turn_lines: ["claude:f0bf048d#L963", "claude:f0bf048d#L975"]
spine_action: "Khai báo file bí mật trong manifest của gói, cài nó vào home của user daemon, và kiểm lại dưới đúng user đó."
spine_action_lines: ["claude:f0bf048d#L975"]
spine_outcome: "Chưa có kết quả: STU-6 chưa chạy lại, đang chờ chủ đặt key rồi mới chuyển về todo."
spine_outcome_lines: ["claude:f0bf048d#L963"]
spine_takeaway: Một bước tay dễ sót sẽ khiến agent mù; đưa bước đó vào khai báo gói và kiểm dưới đúng user chạy agent.
spine_takeaway_lines: ["claude:f0bf048d#L975"]
completeness: 7
---

# Agent SEO mù vì bước đặt key bị sót

**Góc kể:** Một team marketing đang dựng agent AI làm SEO, GA4 và Search Console để agent tự làm việc, không chỉ có người làm. Khi chạy thử, agent SEO báo blocked: phần cài MCP đã xong, nên việc tưởng là agent đã chạy được, nhưng file key Google chưa được đặt, agent không đọc được gì. Lỗi nằm ở gói chứ không ở agent, vì bước chép key bằng tay dễ bị sót. Ai dựng agent cho team không rành kỹ thuật nên nghe, vì một bước tay bị sót có thể làm agent mù mà không báo rõ ngay.
**Bối cảnh:** Agent SEO chạy thử một issue đầu tiên và báo blocked vì không đọc được file credentials.
**Chuyện gì xảy ra:** Phần cài MCP đã chạy xong, nhưng lệnh sudo install đặt key cho user daemon bị sót. Agent không có quyền đọc file đó, nên chuyển issue sang blocked và ghi rõ chủ cần làm gì. Lỗi nằm ở gói chứ không ở agent: việc đặt file bí mật là một bước tay riêng, dễ sót. Sau khi sửa, khai báo file bí mật trong manifest và lệnh cài kiểm lại dưới đúng user daemon.
**Bài học:** Một bước tay dễ sót sẽ khiến agent mù. Đưa bước đó vào khai báo của gói và kiểm nó dưới đúng user chạy agent.
**Artefact:** Thông báo blocked trong issue, đã che nội dung nhạy cảm.
