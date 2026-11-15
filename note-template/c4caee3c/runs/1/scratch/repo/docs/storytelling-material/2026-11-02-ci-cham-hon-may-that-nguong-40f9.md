---
id: 2026-11-02-ci-cham-hon-may-that-nguong-40f9
code: M-Z7TC
aliases: [M-Z7TC]
date: 2026-11-02
repo: repo
status: raw
signals: [so_truoc_so_sau, rang_buoc_thiet_ke]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L1801", "claude:c4caee3c#L1820", "claude:c4caee3c#L1833", "claude:c4caee3c#L1857"]
hook: "CI đo 318 ms thay vì 200 ms, agent không nới ngưỡng"
tension: chon_mot_mat_mot
sides: ["Nới ngưỡng cho CI qua", "Giữ 200 ms trên máy thật, CI nhân hệ số 3"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# CI chậm hơn máy thật: ngưỡng 200 ms thành 318 ms

**Bối cảnh:** Test hiệu năng yêu cầu 1 MB xử lý dưới 200 ms, là mục tiêu trên máy người dùng.
**Chuyện gì xảy ra:** Trên runner GitHub, cùng test đo được 318 ms. Thay vì nới ngưỡng, agent thêm biến OHS_PERF_FACTOR, mặc định là 1 để máy thật vẫn kiểm đúng 200 ms, còn CI đặt hệ số 3. Test lấy lần nhanh nhất trong 3 lần chạy.
**Bài học:** Giữ ngưỡng gốc cho máy người dùng, và đưa khác biệt môi trường CI vào một hệ số có tên rõ ràng.
