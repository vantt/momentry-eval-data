---
id: 2026-11-02-snapshot-test-trong-ci-hong-ngau
date: 2026-11-02
repo: repo
status: raw
signals: [Nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L3210", "claude:c4caee3c#L3219", "claude:c4caee3c#L3247"]
hook: "Test snapshot hỏng ngẫu nhiên chỉ vì hai kết quả bằng điểm đổi chỗ"
tension: nho_ma_to
sides: ["Hai kết quả cùng điểm hoán đổi vị trí", "Snapshot test đỏ ngẫu nhiên trên CI"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Snapshot test trong CI hỏng ngẫu nhiên vì điểm bằng nhau đổi chỗ

**Bối cảnh:** Test so ảnh chụp kết quả không gói với upstream; hai note có điểm hybrid 0,780383795 bằng nhau nên thứ tự phụ thuộc thứ tự index trên máy.
**Chuyện gì xảy ra:** Sửa bằng so sánh chấp nhận hoán vị trong nhóm bằng điểm, các phần khác vẫn khớp tuyệt đối. Cùng commit phát hiện một test khác phụ thuộc biến môi trường do file khác để lại; sửa, chạy 10 lần với thứ tự xáo trộn đều xanh.
**Bài học:** So thứ tự kết quả với điểm bằng nhau cần so tập hợp, không so danh sách.
**Artefact:** Không cần.
