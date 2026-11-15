---
id: 2026-10-29-multica-claude-code-dat-5-5
date: 2026-10-29
repo: repo
status: raw
signals: [artefact nhìn được, người duyệt máy soạn, số trước/sau]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:0faf0bb2#L3622", "claude:0faf0bb2#L3628", "claude:0faf0bb2#L3629", "claude:0faf0bb2#L3672", "claude:0faf0bb2#L3691", "claude:0faf0bb2#L3712", "claude:0faf0bb2#L3747"]
hook: "Agent sales trả issue về hai lần, vì agent kia chưa chịu bịa giá"
tension: tuong_ma_hoa_ra
sides: ["tưởng agent sẽ tự điền giá và hạn chót cho xong việc", "agent dừng lại hỏi chủ, nên cả workflow đạt 5/5"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica + Claude Code đạt 5/5: workflow cột tự giao việc, agent hỏi chủ thay vì bịa số

**Bối cảnh:** Sau khi OpenClaw trượt, spike chuyển sang Claude Code qua CLI của Multica. Workflow gồm bốn cột: nháp, sales review, in review, done.
**Chuyện gì xảy ra:** Issue đi qua agent marketing, agent sales trả lại hai lần vì thiếu giá, và agent marketing dừng lại hỏi chủ thay vì tự bịa giá và hạn chót. Chủ trả lời, agent sales duyệt và issue sang in review giao cho chủ. Comment ghi lại trong 16 giây, và resume session cho kết quả true. Hai phiên chat riêng cho hai khách hàng vẫn giữ đúng ngữ cảnh riêng. Không agent nào tự chuyển done, nhưng điều này chỉ nhờ chỉ dẫn, server không ép.
**Bài học:** Một cột workflow có người xử lý biến bảng kanban thành quy trình chạy được. Luật 'không tự done' trong chỉ dẫn chỉ là chỉ dẫn, muốn chắc chắn phải để server ép.
**Artefact:** Sơ đồ cột Nháp → Sales review → In review → Done, ghi rõ người xử lý từng cột. Che id.
**Góc người ngoài:** cách làm phổ biến là Chạy demo một lần thấy chạy được là kết luận, hoặc so sánh bảng tính năng trên giấy; ở đây khác ở Đặt trước tiêu chí và gieo một mật mã kiểm chứng để thấy rõ chuyện công cụ nào mất bộ nhớ của agent, hoặc agent có tự bịa số liệu hay không. Người đọc muốn cách đánh giá công cụ agent bằng bằng chứng thay vì quảng cáo.
