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
hook: "Agent đang làm thay việc của agent khác thì bị kéo lại"
tension: nguoi_dung_may_sai
sides: ["Agent làm thay SEO và Analytics cho nhanh", "Việc của nó là đóng gói để deploy lại đủ agent"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người vận hành đang dựng bộ agent marketing (SEO, GA4) trên Multica và muốn đóng gói sao cho deploy lại là có đủ agent lẫn công cụ. Lần deploy đầu, AI làm việc cho họ tưởng gói chỉ đổi phần Marketing nên bỏ qua các dòng khác khi đọc plan. Hoá ra deploy ghi đè team Coding của một phiên làm song song trong cùng workspace, đưa instructions, model và skill của các agent đó về bản cũ. Ai deploy nhiều team vào chung một workspace nên đọc hết diff trước khi bấm deploy."
audience: dev vận hành nhiều agent chung một workspace
spine_context: "Người vận hành đang dựng bộ agent SEO và GA4 cho website trên Multica, cho team marketing."
spine_context_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L920"]
spine_want: Muốn đóng gói sao cho deploy lại là có đủ agent và công cụ để agent tự làm.
spine_want_lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L968"]
spine_obstacle: "Deploy vào cùng workspace với một phiên làm song song, còn team Coding nằm trong gói riêng."
spine_obstacle_lines: ["claude:f0bf048d#L915"]
spine_turn: Tưởng plan chỉ đổi phần Marketing; hoá ra deploy ghi đè team Coding của phiên kia.
spine_turn_lines: ["claude:f0bf048d#L915"]
spine_action: Deploy gói Marketing và bỏ qua các dòng thay đổi ngoài Marketing khi đọc plan.
spine_action_lines: ["claude:f0bf048d#L915"]
spine_outcome: "Team Coding được khôi phục từ file của phiên kia, plan báo 0 change; issue đang chờ duyệt không bị ảnh hưởng."
spine_outcome_lines: ["claude:f0bf048d#L915"]
spine_takeaway: "Đọc hết diff của plan trước khi deploy, kể cả phần không thuộc việc của mình."
spine_takeaway_lines: ["claude:f0bf048d#L915"]
completeness: 7
---

# Agent làm thay việc của agent: người dùng kéo lại về đóng gói

**Góc kể:** Người vận hành đang dựng bộ agent marketing (SEO, GA4) trên Multica và muốn đóng gói sao cho deploy lại là có đủ agent lẫn công cụ. Lần deploy đầu, AI làm việc cho họ tưởng gói chỉ đổi phần Marketing nên bỏ qua các dòng khác khi đọc plan. Hoá ra deploy ghi đè team Coding của một phiên làm song song trong cùng workspace, đưa instructions, model và skill của các agent đó về bản cũ. Ai deploy nhiều team vào chung một workspace nên đọc hết diff trước khi bấm deploy.
**Bối cảnh:** Người vận hành muốn hạ tầng đóng gói đủ công cụ để agent tự làm, nhưng agent của mình vẫn tự tìm property, tự chẩn đoán và tự làm việc chuyên môn.
**Chuyện gì xảy ra:** Agent nhận ra mình đang làm thay SEO Specialist và Analytics Reporter. Nó chuyển sang giao việc qua issue. Người vận hành nhắc lại: việc của agent này là đóng gói để deploy lại có đủ agent và công cụ, không phải làm thay. Agent điều chỉnh gói theo hướng khai báo file bí mật và kiểm dưới user daemon.
**Bài học:** Agent hạ tầng nên đóng gói công cụ và quy trình, còn việc chuyên môn để agent chuyên môn làm qua issue.
**Artefact:** Mô tả issue giao việc (chỉ nêu mục tiêu, không gợi lời giải).
