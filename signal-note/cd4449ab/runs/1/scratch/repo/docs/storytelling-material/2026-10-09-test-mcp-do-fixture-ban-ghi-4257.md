---
id: 2026-10-09-test-mcp-do-fixture-ban-ghi-4257
code: M-B0EZ
aliases: [M-B0EZ]
date: 2026-10-09
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3683", "omp:cd4449ab#L3695", "omp:cd4449ab#L3701", "omp:cd4449ab#L3711", "omp:cd4449ab#L3713", "omp:cd4449ab#L3714", "omp:cd4449ab#L3725", "omp:cd4449ab#L3749", "omp:cd4449ab#L3762", "omp:cd4449ab#L3764", "omp:cd4449ab#L3774", "omp:cd4449ab#L3776", "omp:cd4449ab#L3800", "omp:cd4449ab#L3812", "omp:cd4449ab#L3816", "omp:cd4449ab#L3818", "omp:cd4449ab#L3839", "omp:cd4449ab#L3873", "omp:cd4449ab#L3875", "omp:cd4449ab#L3888", "omp:cd4449ab#L3890", "omp:cd4449ab#L3894", "omp:cd4449ab#L3896", "omp:cd4449ab#L3909", "omp:cd4449ab#L3911", "omp:cd4449ab#L3918", "omp:cd4449ab#L3920", "omp:cd4449ab#L3927", "omp:cd4449ab#L3929"]
hook: "Test đỏ mười lần, mà code không sai dòng nào"
tension: tuong_ma_hoa_ra
sides: ["test đỏ tưởng code hỏng", "fixture chỉ thiếu trường"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test MCP đỏ: fixture bản ghi nguồn thiếu trường

**Bối cảnh:** Sau khi gỡ tool, các test MCP tự dựng bản ghi nguồn (sourcepkg.Record) bằng tay và thiếu trường.
**Chuyện gì xảy ra:** Test import qua MCP đỏ khoảng mười lần: nguồn thiếu cadence, revision có kind không hợp lệ (validateRevision báo unsupported source revision kind), skill thiếu SKILL.md đúng chỗ. Mỗi lỗi là một trường thiếu trong fixture, không phải lỗi code. Test xanh khi fixture dùng đủ trường.
**Bài học:** Fixture dựng bản ghi bằng tay dễ thiếu trường mà chỉ runtime mới báo; dùng hàm dựng chung của app thay vì struct tự viết.
**Artefact:** Thông báo validateRevision với giá trị đã che.
