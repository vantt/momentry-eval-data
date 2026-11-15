---
id: 2026-10-09-noi-regex-bang-chung-de-test-4257
code: M-0XTG
aliases: [M-0XTG]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3965", "omp:cd4449ab#L3966", "omp:cd4449ab#L3968"]
hook: "Nới regex cho test qua, người duyệt bắt siết lại"
tension: giup_ma_hai
sides: ["Nới quy tắc để test xanh", "Lesson mới thiếu đường dẫn vẫn lọt, phải siết lại"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang đơn giản hoá code và chuyển dữ liệu từ v3 sang v4. Người làm nới regex bằng chứng và schema dùng chung để test qua, vì dữ liệu cũ thiếu đường dẫn; việc này cho thấy họ tin nới chung là đủ. Người duyệt chỉ ra schema chung phải giữ chặt cho lesson mới, ngoại lệ chỉ đặt trong bước migrate. Nới schema chung để qua test là nợ kỹ thuật, lần sau dữ liệu thiếu đường dẫn sẽ lọt vào."
audience: dev làm migration dữ liệu và schema cho công cụ AI
spine_context: Dự án mcp-skill-hub đang đơn giản hoá code và chuyển dữ liệu từ v3 sang v4.
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: "Lesson mới phải có bằng chứng đúng dạng repo@sha:path, và migration phải fail closed."
spine_want_lines: ["omp:cd4449ab#L3656"]
spine_obstacle: Dữ liệu cũ dùng dạng repo@sha không có path nên không khớp quy tắc mới.
spine_obstacle_lines: ["omp:cd4449ab#L3656"]
spine_turn: "Tưởng nới regex và schema chung để dạng repo@sha không path lọt qua là đủ; hoá ra schema phải giữ chặt, ngoại lệ chỉ được đặt trong bước migrate."
spine_turn_lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3966"]
spine_action: "Nới EvidencePattern và distill.schema.json để chấp nhận repo@sha không có :path."
spine_action_lines: ["omp:cd4449ab#L3963", "omp:cd4449ab#L3966"]
spine_takeaway: Nới schema chung để qua test là nợ kỹ thuật; đặt ngoại lệ ở chỗ migrate dữ liệu cũ và giữ quy tắc mới chặt.
spine_takeaway_lines: ["omp:cd4449ab#L3656"]
completeness: 6
---

# Nới regex bằng chứng để test qua, người duyệt yêu cầu siết lại

**Góc kể:** Dự án mcp-skill-hub đang đơn giản hoá code và chuyển dữ liệu từ v3 sang v4. Người làm nới regex bằng chứng và schema dùng chung để test qua, vì dữ liệu cũ thiếu đường dẫn; việc này cho thấy họ tin nới chung là đủ. Người duyệt chỉ ra schema chung phải giữ chặt cho lesson mới, ngoại lệ chỉ đặt trong bước migrate. Nới schema chung để qua test là nợ kỹ thuật, lần sau dữ liệu thiếu đường dẫn sẽ lọt vào.
**Bối cảnh:** Lesson mới phải có bằng chứng dạng repo@sha:path, nhưng dữ liệu cũ dùng dạng repo@sha không có path.
**Chuyện gì xảy ra:** Để test pass, agent nới EvidencePattern và distill.schema.json cho phép repo@sha không có :path (L3963-3968). Lead bắt lỗi: giữ schema chặt cho lesson mới (repo@40 ký tự hex:path), chỉ chấp nhận dạng ngắn trong migration và ghi vào phase-03.
**Bài học:** Nới schema để qua test là nợ kỹ thuật; đặt ngoại lệ ở chỗ migrate, không ở schema chung.
**Artefact:** Diff regex trước và sau; che nội dung lesson.
