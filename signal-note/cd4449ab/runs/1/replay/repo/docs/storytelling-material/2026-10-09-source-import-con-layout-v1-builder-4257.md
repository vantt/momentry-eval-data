---
id: 2026-10-09-source-import-con-layout-v1-builder-4257
code: M-CC73
aliases: [M-CC73]
date: 2026-10-09
repo: repo
status: raw
signals: [nguoi_duyet_may_soan, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L2123", "omp:cd4449ab#L2124", "omp:cd4449ab#L2126", "omp:cd4449ab#L2133", "omp:cd4449ab#L2136", "omp:cd4449ab#L2160", "omp:cd4449ab#L2202", "omp:cd4449ab#L2232", "omp:cd4449ab#L2247", "omp:cd4449ab#L2250", "omp:cd4449ab#L2253", "omp:cd4449ab#L2259", "omp:cd4449ab#L2262", "omp:cd4449ab#L2264", "omp:cd4449ab#L2292", "omp:cd4449ab#L2294", "omp:cd4449ab#L2306", "omp:cd4449ab#L2319", "omp:cd4449ab#L2321"]
hook: "Lead bảo sửa một chỗ, grep ra thêm hai chỗ sót"
tension: tuong_ma_hoa_ra
sides: ["tưởng đã đồng bộ hết các đường ghi", "source_backfill còn hai chỗ dùng layout cũ"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# source_import còn layout v1: builder dùng chung

**Bối cảnh:** Writer thứ hai (import từ nguồn git) vẫn ghi skill.meta.yaml dạng v1, sót khi chỉ sửa skill_add.
**Chuyện gì xảy ra:** Lead yêu cầu source_import ghi .meta/skill.yaml cùng hình dạng skill_add. Agent tạo buildInitialSkillMetaYAML dùng chung, và nhánh theo schema: từ 3 trở lên ghi .meta, dưới 3 giữ đường cũ. Grep sweep còn sót hai chỗ trong source_backfill, sửa cả hai. Test import đỏ bốn lần vì fixture thiếu commit và ref đúng.
**Bài học:** Khi đổi một định dạng ghi, grep mọi điểm ghi chứ không chỉ điểm được nêu; một builder dùng chung tránh hai bản lệch nhau.
**Artefact:** Kết quả grep 'skill.meta.yaml' trong internal, trước và sau.
