---
id: 2026-11-02-test-anh-chup-ket-qua-hong
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:c4caee3c"
sessions: ["claude:c4caee3c"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:c4caee3c#L3210", "claude:c4caee3c#L3219", "claude:c4caee3c#L3312", "claude:c4caee3c#L3349"]
hook: "Test chập chờn vì hai note bằng điểm đổi chỗ cho nhau"
tension: nho_ma_to
sides: ["Hai note chỉ bằng điểm nhau", "Thứ tự đổi theo máy, test thỉnh thoảng hỏng"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Test ảnh chụp kết quả hỏng vì hai note bằng điểm đổi chỗ

**Bối cảnh:** Test so sánh kết quả tìm với ảnh chụp của upstream, chạy trong CI.
**Chuyện gì xảy ra:** Hai note có cùng điểm hybrid nên thứ tự của chúng phụ thuộc thứ tự index trên từng máy, khiến test thỉnh thoảng hỏng. Sửa bằng so khớp chấp nhận hoán vị trong nhóm bằng điểm, còn lại vẫn so khớp tuyệt đối. Một lỗi khác trong cùng bản vá là test phụ thuộc biến môi trường do file test khác để lại. Mục kiểm không gói trong cổng chất lượng cũng từng hỏng: 0,735 trên máy này và 0,728 trên runner, nên sửa để so với upstream đo trong cùng lần chạy.
**Bài học:** So với baseline ghi sẵn trên máy khác là nguồn lỗi ngẫu nhiên; cổng chất lượng nên đo đối chứng ngay trong cùng lần chạy.
**Artefact:** Hai con số 0,735 và 0,728 cạnh nhau, không kèm đường dẫn. Không cần che.
