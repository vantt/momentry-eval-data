---
id: 2026-10-09-go-17-tool-mcp-cu-test-4257
code: M-0PAE
aliases: [M-0PAE]
date: 2026-10-09
repo: repo
status: raw
signals: [khac, rang_buoc_thiet_ke]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3376", "omp:cd4449ab#L3473", "omp:cd4449ab#L3485", "omp:cd4449ab#L3493", "omp:cd4449ab#L3502", "omp:cd4449ab#L3956", "omp:cd4449ab#L3957"]
hook: "Gỡ 17 tool cũ: xoá 1650 dòng, thêm 350 dòng"
tension: it_ma_nhieu
sides: ["Chỉ thêm 350 dòng code mới", "Thay được 17 tool cũ, xoá 1650 dòng"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
angle: "Một người làm dự án MCP skill hub đang đưa bề mặt MCP về bản tối giản theo bảng contract. Họ tưởng xoá file curation_tools.go là gỡ xong các tool cũ, nhưng test ranh giới curator vẫn đỏ, nên phải đưa lại các tool tương thích. Dev viết công cụ cho AI nên quan tâm vì test ranh giới chạy sau khi xoá cho biết chính xác tool nào còn được gọi, không cần đoán. Kết quả là một commit gom 19 file, +350 -1650 dòng."
audience: dev viết test cho công cụ MCP
spine_context: "Worktree của người làm dự án MCP skill hub, đang chạy Phase 3: đưa bề mặt MCP về bản tối giản theo contract."
spine_context_lines: ["omp:cd4449ab#L6", "omp:cd4449ab#L2374"]
spine_want: Gỡ 17 tool MCP cũ để bề mặt khớp bảng contract.
spine_want_lines: ["omp:cd4449ab#L3957"]
spine_obstacle: Test ranh giới curator đỏ sau khi xoá curation_tools.go.
spine_obstacle_lines: ["omp:cd4449ab#L3490", "omp:cd4449ab#L3502"]
spine_turn: "Tưởng xoá curation_tools.go là gỡ xong; test vẫn đỏ, và các tool tương thích còn nằm trong insight_tools nên phải đưa lại."
spine_turn_lines: ["omp:cd4449ab#L3485", "omp:cd4449ab#L3490", "omp:cd4449ab#L3493"]
spine_action: "Xoá curation_tools.go, viết lại source_tools và insight_tools, sửa server.go, rồi commit 19 file."
spine_action_lines: ["omp:cd4449ab#L3485", "omp:cd4449ab#L3499", "omp:cd4449ab#L3957"]
spine_outcome: "Một commit c75baca: 19 file, +350 -1650 dòng."
spine_outcome_lines: ["omp:cd4449ab#L3956", "omp:cd4449ab#L3959"]
spine_takeaway: "Chạy test ranh giới sau khi xoá code: test đỏ chỉ ra tool nào còn được gọi, không phải đoán."
spine_takeaway_lines: ["omp:cd4449ab#L3490", "omp:cd4449ab#L3502"]
completeness: 7
---

# Gỡ 17 tool MCP cũ, test ranh giới curator buộc tool phải đăng ký đủ

**Góc kể:** Một người làm dự án MCP skill hub đang đưa bề mặt MCP về bản tối giản theo bảng contract. Họ tưởng xoá file curation_tools.go là gỡ xong các tool cũ, nhưng test ranh giới curator vẫn đỏ, nên phải đưa lại các tool tương thích. Dev viết công cụ cho AI nên quan tâm vì test ranh giới chạy sau khi xoá cho biết chính xác tool nào còn được gọi, không cần đoán. Kết quả là một commit gom 19 file, +350 -1650 dòng.
**Bối cảnh:** Phase 3 đưa MCP về bề mặt mới theo bảng contract. Test ranh giới curator yêu cầu mọi tool trong danh sách tương thích phải được đăng ký trên server, và hai bản SKILL.md của curator phải giống nhau.
**Chuyện gì xảy ra:** Agent viết test ranh giới trước, lúc đó đỏ. Sau đó xoá curation_tools.go, viết lại source_tools và insight_tools, thêm source_list. Diff gom lại là 19 file, thêm 350 dòng và xoá 1650 dòng. Nhiều test MCP đỏ trong lúc làm và phải cập nhật thêm server_test.
**Bài học:** Viết test ranh giới trước khi xoá. Nó cho thấy chính xác tool nào còn được gọi, không phải đoán.
**Artefact:** Bảng tool cũ sang tool mới từ contract table, kèm git diff --stat.
