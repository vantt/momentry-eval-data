---
id: 2026-11-02-snapshot-test-hong-khi-hai-ket-40f9
code: M-DW5Z
aliases: [M-DW5Z]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2663", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247"]
hook: "Hai note cùng điểm đổi chỗ, CI đỏ ngẫu nhiên"
tension: nho_ma_to
sides: ["Hai note bằng điểm hệt nhau", "Thứ tự đổi theo máy, test hỏng ngẫu nhiên"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Snapshot test hỏng khi hai kết quả cùng điểm đổi chỗ

**Bối cảnh:** Test so kết quả tìm với ảnh chụp của upstream, khi không có gói.
**Chuyện gì xảy ra:** Hai note có điểm hybrid bằng hệt nhau, nên thứ tự của chúng phụ thuộc thứ tự index trên từng máy. Test so khớp tuyệt đối nên hỏng ngẫu nhiên trên CI. Sửa bằng một phép so sánh chấp nhận hoán vị trong nhóm bằng điểm, các trường còn lại vẫn khớp tuyệt đối. Trong quá trình sửa, agent còn phát hiện một test khác phụ thuộc biến môi trường do file test khác để lại, hỏng 3 trên 10 lần khi xáo thứ tự file.
**Bài học:** Với kết quả xếp hạng có điểm bằng nhau, so sánh phải xét nhóm bằng điểm. Test không được dựa vào trạng thái của test khác.
