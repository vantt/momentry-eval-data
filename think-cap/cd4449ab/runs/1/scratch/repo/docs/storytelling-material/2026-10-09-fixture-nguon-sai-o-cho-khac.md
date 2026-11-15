---
id: 2026-10-09-fixture-nguon-sai-o-cho-khac
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2204", "omp:cd4449ab#L2234", "omp:cd4449ab#L2249", "omp:cd4449ab#L2255", "omp:cd4449ab#L2294", "omp:cd4449ab#L2306", "omp:cd4449ab#L3749", "omp:cd4449ab#L3764", "omp:cd4449ab#L3776", "omp:cd4449ab#L3800", "omp:cd4449ab#L3812", "omp:cd4449ab#L3818", "omp:cd4449ab#L3839", "omp:cd4449ab#L3875", "omp:cd4449ab#L3890", "omp:cd4449ab#L3896", "omp:cd4449ab#L3911", "omp:cd4449ab#L3918", "omp:cd4449ab#L3920"]
hook: "Mỗi lượt test chỉ sửa được một trường, nên lặp 5 lần"
tension: none
sides: []
strength: 0
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture nguồn: sai ở chỗ khác nhau mỗi lượt

**Bối cảnh:** Fixture của source import và MCP source cần record nguồn hợp lệ: revision, monitoring, file URL.
**Chuyện gì xảy ra:** TestSourceImportInV3CreatesMetaSkillYAMLAndMatchesSkillAddTrust đỏ ba lần vì file URL, revision và record, rồi xanh. Bên MCP, TestSourceImportMCPPreviewAndConfirm đỏ năm lượt với 'invalid source revision' và 'unsupported source revision kind' trước khi xanh. Mỗi lượt chỉ sửa được một trường, nên vòng lặp dài.
**Bài học:** Record nguồn trong fixture cần đủ mọi trường bắt buộc ngay từ đầu; dùng một builder chung cho test.
**Artefact:** Dòng lỗi 'unsupported source revision kind', không cần che.
