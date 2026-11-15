---
id: 2026-11-02-hai-note-cung-diem-doi-cho
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L3210", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247", "claude:c4caee3c#L3288", "claude:c4caee3c#L3349"]
hook: "Test đỏ ngẫu nhiên trên CI vì hai note cùng điểm"
tension: nho_ma_to
sides: ["Hai note bằng điểm đổi chỗ cho nhau", "Test snapshot đỏ ngẫu nhiên trên CI"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai note cùng điểm đổi chỗ: test snapshot đỏ trên CI

**Bối cảnh:** Test so kết quả với ảnh chụp của upstream, và hai note có điểm hybrid bằng hệt nhau.
**Chuyện gì xảy ra:** Thứ tự giữa hai note phụ thuộc thứ tự index trên từng máy, nên test đỏ ngẫu nhiên trên CI. Sửa test: chấp nhận đổi chỗ trong nhóm cùng điểm, phần còn lại vẫn so tuyệt đối. Agent cũng phát hiện một test khác chỉ qua nhờ biến môi trường do file test khác để lại. Chạy 10 lần với thứ tự file xáo trộn đều xanh.
**Bài học:** Khi so thứ tự kết quả, phải định nghĩa rõ thế nào là hòa điểm trước khi viết assertion.
**Artefact:** Đoạn diff của hàm so sánh, không kèm dữ liệu.
