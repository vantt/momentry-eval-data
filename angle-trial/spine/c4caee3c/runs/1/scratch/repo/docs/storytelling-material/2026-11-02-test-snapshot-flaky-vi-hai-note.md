---
id: 2026-11-02-test-snapshot-flaky-vi-hai-note
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L2663", "claude:c4caee3c#L3210", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247", "claude:c4caee3c#L3398"]
hook: "Test flaky vì hai note cùng điểm 0,780383795 đổi chỗ theo máy"
tension: tuong_ma_hoa_ra
sides: ["Test chớp đỏ trông như lỗi code", "Hai note bằng điểm tuyệt đối, thứ tự do máy quyết định"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test snapshot flaky vì hai note có điểm bằng nhau đổi thứ tự theo máy

**Bối cảnh:** Test P01 so kết quả tìm khi không có gói với ảnh chụp upstream đã ghi. CI đỏ ngẫu nhiên.
**Chuyện gì xảy ra:** Hai note có điểm hybrid giống hệt (0,780383795), nên thứ tự giữa chúng do thứ tự index trên từng máy quyết định, không phải lỗi code. Agent sửa phép so sánh: cho phép đổi chỗ trong nhóm cùng điểm, các trường khác vẫn khớp tuyệt đối, code tìm kiếm không đổi. Kiểm chứng bằng cách hoán đổi hai note trong ảnh chụp. Agent cũng tìm thêm một test phụ thuộc biến môi trường do file khác để lại.
**Bài học:** Khi điểm bằng nhau, thứ tự không xác định; so sánh theo nhóm bằng điểm, đừng so cứng theo vị trí.
**Artefact:** Diff ảnh chụp kết quả, đã che đường dẫn note.
