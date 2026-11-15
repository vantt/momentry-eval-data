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
hook: "Xoá 17 tool cũ: thêm 350 dòng, bỏ 1650 dòng"
tension: it_ma_nhieu
sides: ["viết thêm 350 dòng", "gỡ được 1650 dòng và 17 tool cũ"]
strength: 1
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gỡ 17 tool MCP cũ, test ranh giới curator buộc tool phải đăng ký đủ

**Bối cảnh:** Phase 3 đưa MCP về bề mặt mới theo bảng contract. Test ranh giới curator yêu cầu mọi tool trong danh sách tương thích phải được đăng ký trên server, và hai bản SKILL.md của curator phải giống nhau.
**Chuyện gì xảy ra:** Agent viết test ranh giới trước, lúc đó đỏ. Sau đó xoá curation_tools.go, viết lại source_tools và insight_tools, thêm source_list. Diff gom lại là 19 file, thêm 350 dòng và xoá 1650 dòng. Nhiều test MCP đỏ trong lúc làm và phải cập nhật thêm server_test.
**Bài học:** Viết test ranh giới trước khi xoá. Nó cho thấy chính xác tool nào còn được gọi, không phải đoán.
**Artefact:** Bảng tool cũ sang tool mới từ contract table, kèm git diff --stat.
