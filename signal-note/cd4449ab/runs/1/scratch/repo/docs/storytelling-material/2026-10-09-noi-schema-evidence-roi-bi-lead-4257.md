---
id: 2026-10-09-noi-schema-evidence-roi-bi-lead-4257
code: M-2JSE
aliases: [M-2JSE]
date: 2026-10-09
repo: repo
status: raw
signals: [dao_quyet_dinh, nguoi_duyet_may_soan]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L2507", "omp:cd4449ab#L2509", "omp:cd4449ab#L2513", "omp:cd4449ab#L2516", "omp:cd4449ab#L2518", "omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3966", "omp:cd4449ab#L3968"]
hook: "Nới schema cho tiện, 77 mục ngắn khiến lead bắt siết lại"
tension: giup_ma_hai
sides: ["nới schema để kiểm tra nhanh", "lead bắt giữ chặt, chỉ ngoại lệ ở migration"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Dự án mcp-skill-hub đang được làm lại theo hướng đơn giản hoá, và người làm đang chuyển dữ liệu distill cũ sang schema mới. Người làm nới schema để nhận dạng bằng chứng repo@sha cũ, thấy test vẫn xanh nên tưởng là ổn. Lead yêu cầu giữ schema mới chặt và chỉ cho dạng ngắn đi qua bước migration. Với ai thiết kế schema dữ liệu, nới schema để khớp dữ liệu cũ dễ mở đường cho dữ liệu lỗi vào về sau."
audience: dev thiết kế schema và migration dữ liệu cho công cụ AI
spine_context: "Dự án mcp-skill-hub đang được làm lại theo hướng đơn giản hoá, và người làm đang chuyển dữ liệu distill cũ sang schema mới."
spine_context_lines: ["omp:cd4449ab#L6"]
spine_want: "Muốn schema mới giữ chặt cho bài học mới, còn dữ liệu cũ đi qua đường migration riêng."
spine_want_lines: ["omp:cd4449ab#L3656"]
spine_obstacle: "Dữ liệu cũ ghi bằng chứng dạng repo@sha không có đường dẫn, trong khi schema mới yêu cầu repo@<40-hex>:path."
spine_obstacle_lines: ["omp:cd4449ab#L3656"]
spine_turn: "Tưởng nới schema cho khớp dữ liệu cũ là ổn, vì test vẫn xanh; hoá ra lead yêu cầu giữ schema chặt và chỉ chấp nhận dạng ngắn trong bước migration."
spine_turn_lines: ["omp:cd4449ab#L2504", "omp:cd4449ab#L2509", "omp:cd4449ab#L2512", "omp:cd4449ab#L3656"]
spine_action: Nới EvidencePattern và distill.schema.json để chấp nhận repo@sha.
spine_action_lines: ["omp:cd4449ab#L2504", "omp:cd4449ab#L2507"]
spine_outcome: Test distill và schemas qua; lead yêu cầu siết lại; sau đó model và schema được sửa lại.
spine_outcome_lines: ["omp:cd4449ab#L2512", "omp:cd4449ab#L3656", "omp:cd4449ab#L3963", "omp:cd4449ab#L3966"]
spine_takeaway: Đừng nới schema để khớp dữ liệu cũ; giữ schema mới chặt và để đường migration xử lý phần lộn xộn.
spine_takeaway_lines: ["omp:cd4449ab#L3656"]
completeness: 7
---

# Nới schema evidence rồi bị lead yêu cầu siết lại

**Góc kể:** Dự án mcp-skill-hub đang được làm lại theo hướng đơn giản hoá, và người làm đang chuyển dữ liệu distill cũ sang schema mới. Người làm nới schema để nhận dạng bằng chứng repo@sha cũ, thấy test vẫn xanh nên tưởng là ổn. Lead yêu cầu giữ schema mới chặt và chỉ cho dạng ngắn đi qua bước migration. Với ai thiết kế schema dữ liệu, nới schema để khớp dữ liệu cũ dễ mở đường cho dữ liệu lỗi vào về sau.
**Bối cảnh:** Dữ liệu distill cũ có bằng chứng dạng repo@sha không có :path; schema mới yêu cầu repo@40-hex:path.
**Chuyện gì xảy ra:** Để kiểm tra nhanh, agent nới EvidencePattern cho phép repo@sha. Đếm được 77 mục ngắn trong file cũ. Lead phản đối: schema phải giữ chặt cho bài học mới. Quyết định cuối: chỉ chấp nhận dạng ngắn trong migration v4, chuyển thành repo@sha:<đường dẫn skill> hoặc giữ trong trường legacy_where, và ghi sai lệch vào phase-03.
**Bài học:** Đừng nới schema để khớp dữ liệu cũ; giữ chặt schema mới và để đường migration xử lý phần lộn xộn.
**Artefact:** Hai regex cũ và mới đặt cạnh nhau.
