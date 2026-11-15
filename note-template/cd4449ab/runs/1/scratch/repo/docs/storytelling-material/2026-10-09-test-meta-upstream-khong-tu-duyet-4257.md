---
id: 2026-10-09-test-meta-upstream-khong-tu-duyet-4257
code: M-GW1Q
aliases: [M-GW1Q]
date: 2026-10-09
repo: repo
status: raw
signals: [khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L534", "omp:cd4449ab#L543", "omp:cd4449ab#L552", "omp:cd4449ab#L561", "omp:cd4449ab#L576", "omp:cd4449ab#L607"]
hook: "Test đỏ 5 lần, vì gốc nằm ở đường đọc, không ở logic duyệt"
tension: tuong_ma_hoa_ra
sides: ["Tưởng lỗi nằm ở logic duyệt", "Gốc thật ở đường đọc meta, sửa 5 lần mới lộ"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test 'meta upstream không tự duyệt' đỏ 5 lần

**Bối cảnh:** Test kiểm tra meta do upstream ghi không được tự duyệt khi import và khi upstream update.
**Chuyện gì xảy ra:** Test đỏ 5 lần liên tiếp. Mỗi lần sửa một chỗ thì lộ ra chỗ tiếp theo, trong đó có điều kiện đọc meta ở loadTrackedSkills (L606-607) khi metaBytes rỗng. Gốc nằm ở đường đọc meta, không nằm ở logic duyệt.
**Bài học:** Với test về quyền duyệt, kiểm tra trạng thái đầu vào trước khi sửa; đừng sửa theo thông báo lỗi cuối.
**Artefact:** Đoạn output test trước và sau khi sửa điều kiện đọc meta; che tên người.
