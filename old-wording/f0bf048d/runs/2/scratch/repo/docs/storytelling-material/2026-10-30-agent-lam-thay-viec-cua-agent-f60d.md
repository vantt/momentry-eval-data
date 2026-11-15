---
id: 2026-10-30-agent-lam-thay-viec-cua-agent-f60d
code: M-Y15Q
aliases: [M-Y15Q]
date: 2026-10-30
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L923", "claude:f0bf048d#L968", "claude:f0bf048d#L975"]
hook: "Agent làm thay SEO Specialist, người dùng kéo về việc đóng gói"
tension: nguoi_dung_may_sai
sides: ["agent làm thay việc của SEO Specialist", "người vận hành: việc của bạn là đóng gói"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một đội marketing đang dựng bộ agent AI để tự làm SEO và phân tích GA4 thay cho người, nên việc của agent hạ tầng là đóng gói đủ công cụ cho chúng. Agent hạ tầng lại tin mình phải làm luôn việc chuyên môn: tự tìm property, tự chẩn đoán Search Console. Người dùng kéo lại: việc của nó là đóng gói để deploy lại có đủ agent và công cụ, còn SEO thì giao cho agent SEO qua issue. Ai dựng hạ tầng cho agent AI dễ rơi vào đúng bẫy này."
audience: dev dựng hạ tầng cho agent AI
spine_context: "Một đội marketing đang dựng bộ agent AI để làm SEO và phân tích GA4, vì trong team chưa có ai làm các việc này."
spine_context_lines: ["claude:f0bf048d#L7"]
spine_want: "Muốn agent tự làm được SEO và phân tích số liệu bằng công cụ đã gắn, không cần người làm thay."
spine_want_lines: ["claude:f0bf048d#L920"]
spine_obstacle: "Gói deploy thiếu bước đặt file bí mật, nên agent chạy lên mà không có key và bị chặn."
spine_obstacle_lines: ["claude:f0bf048d#L975"]
spine_turn: "Tưởng việc của mình là tự làm chuyên môn: tự tìm property, tự chẩn đoán Search Console. Hoá ra việc của agent hạ tầng chỉ là đóng gói công cụ để agent chuyên môn tự làm."
spine_turn_lines: ["claude:f0bf048d#L923", "claude:f0bf048d#L968"]
spine_action: "Giao vụ Search Console cho SEO Specialist qua issue, rồi sửa gói: khai báo user daemon và file bí mật trong .fgopc.yaml, còn opc.mjs tools cài MCP, đặt file bí mật và kiểm dưới đúng user daemon."
spine_action_lines: ["claude:f0bf048d#L923", "claude:f0bf048d#L975"]
spine_outcome: "Agent khởi động được MCP và gọi được list_sites, get_account_summaries, nhưng issue bị blocked vì thiếu file key. Trước đó GA4 đã trả số liệu thật, ví dụ kênh Direct có 58 session trong 7 ngày."
spine_outcome_lines: ["claude:f0bf048d#L915", "claude:f0bf048d#L955", "claude:f0bf048d#L963"]
spine_takeaway: "Agent hạ tầng nên đóng gói công cụ, quy trình và file bí mật để deploy lại là đủ. Việc chuyên môn giao cho agent chuyên môn qua issue."
spine_takeaway_lines: ["claude:f0bf048d#L968", "claude:f0bf048d#L975"]
completeness: 7
---

# Agent làm thay việc của agent: người dùng kéo lại về đóng gói

**Góc kể:** Một đội marketing đang dựng bộ agent AI để tự làm SEO và phân tích GA4 thay cho người, nên việc của agent hạ tầng là đóng gói đủ công cụ cho chúng. Agent hạ tầng lại tin mình phải làm luôn việc chuyên môn: tự tìm property, tự chẩn đoán Search Console. Người dùng kéo lại: việc của nó là đóng gói để deploy lại có đủ agent và công cụ, còn SEO thì giao cho agent SEO qua issue. Ai dựng hạ tầng cho agent AI dễ rơi vào đúng bẫy này.
**Bối cảnh:** Người vận hành muốn hạ tầng đóng gói đủ công cụ để agent tự làm, nhưng agent của mình vẫn tự tìm property, tự chẩn đoán và tự làm việc chuyên môn.
**Chuyện gì xảy ra:** Agent nhận ra mình đang làm thay SEO Specialist và Analytics Reporter. Nó chuyển sang giao việc qua issue. Người vận hành nhắc lại: việc của agent này là đóng gói để deploy lại có đủ agent và công cụ, không phải làm thay. Agent điều chỉnh gói theo hướng khai báo file bí mật và kiểm dưới user daemon.
**Bài học:** Agent hạ tầng nên đóng gói công cụ và quy trình, còn việc chuyên môn để agent chuyên môn làm qua issue.
**Artefact:** Mô tả issue giao việc (chỉ nêu mục tiêu, không gợi lời giải).
