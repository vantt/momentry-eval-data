---
id: 2026-10-30-chu-doi-vai-khong-de-agent-f60d
code: M-BWBM
aliases: [M-BWBM]
date: 2026-10-30
repo: repo
status: raw
signals: [dao_quyet_dinh]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L923", "claude:f0bf048d#L929", "claude:f0bf048d#L930", "claude:f0bf048d#L946"]
hook: "Chủ không muốn agent làm hộ, nên agent giao việc qua issue"
tension: khac
sides: ["agent làm hộ việc chuyên môn", "chủ muốn giao qua issue, agent chỉ cung cấp công cụ"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Người làm đang dựng bộ agent AI cho team marketing của một website, vì team chưa có agent nào làm SEO, theo dõi GA4 hay đọc số liệu. Trợ lý AI của họ tưởng việc mình là tự tìm property, phát hiện lỗi www và chẩn đoán Search Console để có kết quả nhanh. Chủ nhắc rằng agent chỉ cần đủ công cụ, nên việc đúng là trang bị công cụ rồi giao việc qua issue. Ai dựng agent cho việc marketing dễ rơi vào cái bẫy tự làm hộ này."
audience: người dựng agent AI cho marketing hoặc vận hành nội dung
spine_context: "Người làm đang dựng bộ agent AI cho team marketing của một website, vì team chưa có agent nào làm SEO, theo dõi GA4 hay đọc số liệu."
spine_context_lines: ["claude:f0bf048d#L7"]
spine_want: "Muốn các agent SEO và GA4 tự làm được việc, không phải người làm tự tay làm."
spine_want_lines: ["claude:f0bf048d#L7", "claude:f0bf048d#L920"]
spine_obstacle: Search Console đang cấp quyền nhầm property nên chưa có số liệu.
spine_obstacle_lines: ["claude:f0bf048d#L915"]
spine_turn: "Trợ lý AI tưởng việc của mình là tự tìm property, phát hiện lỗi www và chẩn đoán Search Console. Chủ nói việc đúng là trang bị đủ công cụ để agent chuyên môn tự làm."
spine_turn_lines: ["claude:f0bf048d#L920", "claude:f0bf048d#L923"]
spine_action: "Tạo issue STU-6 giao cho SEO Specialist, không nêu trước lỗi www để kiểm xem agent có tự phát hiện được không."
spine_action_lines: ["claude:f0bf048d#L929", "claude:f0bf048d#L937"]
spine_takeaway: "Khi thấy mình đang làm hộ agent, hãy hỏi agent có công cụ để làm việc đó không. Nếu không, phần thiếu nằm ở bộ công cụ chứ không ở người vận hành."
spine_takeaway_lines: ["claude:f0bf048d#L923", "claude:f0bf048d#L946"]
completeness: 6
---

# Chủ đổi vai: không để agent làm hộ việc chuyên môn, phải giao qua issue

**Góc kể:** Người làm đang dựng bộ agent AI cho team marketing của một website, vì team chưa có agent nào làm SEO, theo dõi GA4 hay đọc số liệu. Trợ lý AI của họ tưởng việc mình là tự tìm property, phát hiện lỗi www và chẩn đoán Search Console để có kết quả nhanh. Chủ nhắc rằng agent chỉ cần đủ công cụ, nên việc đúng là trang bị công cụ rồi giao việc qua issue. Ai dựng agent cho việc marketing dễ rơi vào cái bẫy tự làm hộ này.
**Bối cảnh:** Agent đã tự tìm property GA4, phát hiện lỗi www và chẩn đoán Search Console thay vì để agent SEO làm.
**Chuyện gì xảy ra:** Chủ nói 'agent chỉ cần đầy đủ công cụ để làm là tốt nhất'. Agent nhận ra các bước đó phải do agent SEO làm bằng MCP sẵn có. Agent tạo issue STU-6 không nêu trước lỗi www, để kiểm xem agent có tự phát hiện được không. Agent liệt kê các công cụ còn thiếu cho từng mảng.
**Bài học:** Khi thấy mình đang làm hộ agent, hãy tự hỏi agent có công cụ để làm việc này không. Nếu không, phần thiếu nằm ở gói chứ không ở người vận hành.
**Artefact:** Nội dung issue giao việc (không kể lỗi trước đó).
