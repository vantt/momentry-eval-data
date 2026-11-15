---
id: 2026-10-09-ranh-gioi-mcp-17-tool-bi
date: 2026-10-09
repo: repo
status: raw
signals: [khác]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [harvest]
lines: ["omp:cd4449ab#L3473", "omp:cd4449ab#L3485", "omp:cd4449ab#L3494", "omp:cd4449ab#L3497", "omp:cd4449ab#L3505", "omp:cd4449ab#L3593", "omp:cd4449ab#L3596", "omp:cd4449ab#L3602", "omp:cd4449ab#L3611", "omp:cd4449ab#L3954", "omp:cd4449ab#L3957"]
hook: "Xoá 17 tool MCP, diff -1650 dòng, và boundary test là bản spec"
tension: it_ma_nhieu
sides: ["một boundary test ngắn làm spec", "quyết định xoá 17 tool và hơn 1600 dòng"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Ranh giới MCP: 17 tool bị xoá, boundary test làm spec

**Bối cảnh:** Đưa MCP và web về contract table của mô hình distill tối giản.
**Chuyện gì xảy ra:** Boundary test yêu cầu danh sách compatible tool khớp server. Agent xoá curation_tools.go (113 dòng) và các tool insight_*, giữ routing_evaluate và skill_update_preview. Commit c75baca có diff 19 file, +350 và -1650. SKILL.md của curator có hai bản đồng bộ bằng cp, và thêm dòng O8 về prior.kind rejected và skill_feedback.
**Bài học:** Boundary test là spec chạy được. Để nó liệt kê tool được phép thay vì tin vào tài liệu nhớ.
**Artefact:** Danh sách tool trước và sau dưới dạng bảng hai cột, không kèm mô tả nội bộ.
