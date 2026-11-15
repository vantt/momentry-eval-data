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
hook: "Agent đang làm thay việc của hai agent khác, bị kéo về đóng gói"
tension: giup_ma_hai
sides: ["Agent làm thay SEO Specialist và Analytics Reporter cho nhanh", "Việc của nó là đóng gói để deploy lại đủ agent và công cụ"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Agent làm thay việc của agent: người dùng kéo lại về đóng gói

**Bối cảnh:** Người vận hành muốn hạ tầng đóng gói đủ công cụ để agent tự làm, nhưng agent của mình vẫn tự tìm property, tự chẩn đoán và tự làm việc chuyên môn.
**Chuyện gì xảy ra:** Agent nhận ra mình đang làm thay SEO Specialist và Analytics Reporter. Nó chuyển sang giao việc qua issue. Người vận hành nhắc lại: việc của agent này là đóng gói để deploy lại có đủ agent và công cụ, không phải làm thay. Agent điều chỉnh gói theo hướng khai báo file bí mật và kiểm dưới user daemon.
**Bài học:** Agent hạ tầng nên đóng gói công cụ và quy trình, còn việc chuyên môn để agent chuyên môn làm qua issue.
**Artefact:** Mô tả issue giao việc (chỉ nêu mục tiêu, không gợi lời giải).
