---
id: 2026-10-09-lead-vong-2-description-sau-migrate-4257
code: M-2FX3
aliases: [M-2FX3]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1714", "omp:cd4449ab#L1722", "omp:cd4449ab#L1747", "omp:cd4449ab#L1749", "omp:cd4449ab#L1779", "omp:cd4449ab#L1863"]
hook: "Sau migrate, description của skill chỉ còn đúng hai ký tự '>-'"
tension: tuong_ma_hoa_ra
sides: ["test xanh nên tưởng migrate an toàn", "description thành '>-', định tuyến hỏng"]
strength: 3
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm migration cho hub skill của AI agent đang đưa hub thật lên schema mới. Validate qua và test xanh nên tưởng đã an toàn, nhưng sau migrate description của skill chỉ còn đúng '>-' vì bộ đọc đọc frontmatter theo từng dòng và không hiểu block scalar YAML. Router dùng description nên định tuyến hỏng. Ai parse YAML bằng tay hoặc chỉ assert trạng thái mà không assert trường router dùng đều có thể dính lỗi tương tự."
audience: dev làm migration hoặc viết parser frontmatter cho công cụ AI agent
spine_context: "Một người làm migration cho hub skill của AI agent, đang đưa hub thật lên schema 3."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: Muốn migration chạy được trên bản sao của hub thật mà không làm hỏng skill.
spine_want_lines: ["omp:cd4449ab#L1462"]
spine_obstacle: "Migration trên hub thật báo lỗi ở bước v1→v2, và bộ đọc frontmatter đọc theo từng dòng."
spine_obstacle_lines: ["omp:cd4449ab#L1462", "omp:cd4449ab#L1713"]
spine_turn: "Tưởng migrate đã an toàn vì validate qua và fixture không báo lỗi; hoá ra description của skill thành đúng hai ký tự '>-', và router dùng description nên định tuyến hỏng."
spine_turn_lines: ["omp:cd4449ab#L1711", "omp:cd4449ab#L1713"]
spine_action: "Thay bộ đọc frontmatter bằng YAML parser thật, sửa thứ tự tên, rồi thêm assert description và các trường router dùng vào fixture test."
spine_action_lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1866"]
spine_outcome: "Đã commit ee06288 (4 file, +224/-142); agent báo make check xanh."
spine_outcome_lines: ["omp:cd4449ab#L1712", "omp:cd4449ab#L1863"]
spine_takeaway: "Đừng parse YAML bằng tay; assert đúng các trường router thật sự dùng, không chỉ trạng thái trust."
spine_takeaway_lines: ["omp:cd4449ab#L1713"]
completeness: 7
---

# Lead vòng 2: description `>-` sau migrate

**Góc kể:** Một người làm migration cho hub skill của AI agent đang đưa hub thật lên schema mới. Validate qua và test xanh nên tưởng đã an toàn, nhưng sau migrate description của skill chỉ còn đúng '>-' vì bộ đọc đọc frontmatter theo từng dòng và không hiểu block scalar YAML. Router dùng description nên định tuyến hỏng. Ai parse YAML bằng tay hoặc chỉ assert trạng thái mà không assert trường router dùng đều có thể dính lỗi tương tự.
**Bối cảnh:** SKILL.md dùng block scalar YAML (description: >-) trong frontmatter, còn bộ đọc frontmatter trong code đọc theo từng dòng.
**Chuyện gì xảy ra:** Trước migrate description hiển thị đúng. Sau migrate, skill show cho description đúng hai ký tự '>-'. Router dùng description nên đây là hồi quy định tuyến. Fixture trước đó không bắt được vì không assert description; khi thêm assert thì lỗi lộ ra. Parser theo dòng được thay bằng YAML parser thật.
**Bài học:** Đừng parse YAML bằng tay; assert đúng trường mà router thật sự dùng, không chỉ trạng thái trust.
**Artefact:** Đoạn frontmatter có >- và kết quả show trước/sau, che nội dung skill nếu nhạy cảm.
