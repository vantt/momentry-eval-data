---
id: 2026-11-02-hai-note-co-diem-bang-het
date: 2026-11-02
repo: repo
status: raw
signals: []
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2664", "claude:c4caee3c#L2685", "claude:c4caee3c#L3210", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247"]
hook: "Hai note bằng điểm 0,780383795 làm CI đỏ, máy bạn vẫn xanh"
tension: nho_ma_to
sides: ["Hai note trùng điểm hệt nhau", "Test chỉ đỏ trên CI, còn máy local xanh"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hai note có điểm bằng hệt nhau làm snapshot CI đỏ theo thứ tự ngẫu nhiên

**Bối cảnh:** Test so kết quả tìm kiếm không có gói với ảnh chụp upstream đã ghi, từng so khớp tuyệt đối từng vị trí.
**Chuyện gì xảy ra:** Hai note có điểm hybrid đều là 0,780383795, nên thứ tự giữa chúng phụ thuộc thứ tự index trên từng máy. Test chỉ thất bại trên CI. Agent viết phép so sánh chấp nhận hoán vị trong nhóm bằng điểm, còn mọi thứ khác vẫn khớp tuyệt đối; mã tìm kiếm không đổi. Trong lúc sửa, agent còn tìm ra một test phụ thuộc biến môi trường do file test khác để lại.
**Bài học:** Kết quả xếp hạng có điểm bằng nhau không có thứ tự xác định; so sánh chúng cần định nghĩa rõ nhóm hoán vị được phép.
**Artefact:** Hai dòng điểm bằng nhau đã ẩn tên note (điểm số và thứ hạng vị trí là đủ).
