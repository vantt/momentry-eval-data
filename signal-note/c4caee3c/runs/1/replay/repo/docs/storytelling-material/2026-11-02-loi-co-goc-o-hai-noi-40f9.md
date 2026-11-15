---
id: 2026-11-02-loi-co-goc-o-hai-noi-40f9
code: M-BCB4
aliases: [M-BCB4]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:c4caee3c#L2663"]
hook: "Hai note cùng điểm 0,780383795, thứ tự đổi theo từng máy"
tension: nho_ma_to
sides: ["Hai note đồng điểm trông vô hại", "Thứ tự kết quả lệch tuỳ máy, làm test đỏ"]
strength: 2
stakes: 1
hits: 1
runs: 1
unverified: [agent_only]
privacy: unchecked
links: []
threads: []
---

# Lỗi có gốc ở hai nơi: nhà cung cấp biến nạp model và nhóm kết quả đồng điểm

**Bối cảnh:** Test so ảnh chụp kết quả khi không có gói thường thất bại ngẫu nhiên.
**Chuyện gì xảy ra:** Hai note có cùng điểm hybrid 0,780383795 nên thứ tự phụ thuộc thứ tự index trên từng máy. Agent sửa phép so sánh cho phép hoán vị trong nhóm đồng điểm, còn các trường khác vẫn so khớp tuyệt đối. Test này và một test phụ thuộc biến môi trường do file khác để lại đều được sửa.
**Bài học:** Kết quả đồng điểm phải được coi là tập hợp không có thứ tự khi so sánh snapshot.
**Artefact:** Ví dụ hai note đồng điểm (chỉ số điểm, không kèm tên).
