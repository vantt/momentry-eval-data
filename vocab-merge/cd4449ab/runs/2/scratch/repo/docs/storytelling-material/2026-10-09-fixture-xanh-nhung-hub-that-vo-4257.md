---
id: 2026-10-09-fixture-xanh-nhung-hub-that-vo-4257
code: M-Q87X
aliases: [M-Q87X]
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L1713", "omp:cd4449ab#L1722", "omp:cd4449ab#L1779", "omp:cd4449ab#L1833", "omp:cd4449ab#L1888", "omp:cd4449ab#L1890"]
hook: "Fixture xanh hết, nhưng hub thật biến mô tả skill thành '>-'"
tension: tuong_ma_hoa_ra
sides: ["test fixture xanh toàn bộ", "hub thật có description bị thành chuỗi '>-' làm hỏng routing"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Fixture xanh nhưng hub thật vỡ: description thành '>-' và name sai thứ tự

**Bối cảnh:** Test migrate v1→v2→v3 trên ba skill thật đã pass nên tưởng đã xong. Lead chạy diff skill show --json trước và sau, và thấy regression.
**Chuyện gì xảy ra:** Frontmatter SKILL.md dùng block scalar (description: >-) nên sau migrate description thành đúng chuỗi '>-'. Resolver dùng description để route, nên đây là regression routing. Thứ tự name cũng sai: một skill thành 'Test Audit' thay vì giữ id, vì H1 được ưu tiên trước frontmatter. Sau khi sửa, cả ba skill có name, description, status và routing trùng trước và sau.
**Bài học:** Test migration phải so sánh output mà hệ thống đọc ra trước và sau, không chỉ kiểm tra trạng thái ghi file.
**Artefact:** Diff hai JSON skill show trước và sau, chỉ các trường name và description. Che nội dung skill.
