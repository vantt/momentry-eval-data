---
id: 2026-10-09-migration-phai-fail-closed-loi-doc-4257
code: M-18G4
aliases: [M-18G4]
date: 2026-10-09
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, khac]
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest, outsider]
lines: ["omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3978", "omp:cd4449ab#L3987", "omp:cd4449ab#L3989", "omp:cd4449ab#L3996"]
hook: "Migration tưởng an toàn, nhưng WalkDir nuốt lỗi đọc file"
tension: cam_ma_van_lot
sides: ["migration thiết kế để fail closed", "một vòng WalkDir âm thầm nuốt lỗi đọc file"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration phải fail closed: lỗi đọc file bị nuốt trong vòng WalkDir

**Bối cảnh:** Lead yêu cầu mọi lỗi walk, read hoặc parse trong migration v4 phải trả lỗi kèm tên file và workspace không được đổi khi có lỗi.
**Chuyện gì xảy ra:** Grep dấu gán bỏ qua lỗi tìm thấy một chỗ nuốt lỗi WalkDir. Agent viết lại v4.go để trả lỗi có tên file và thêm test cho một file insight bị hỏng. Test đầu tiên vẫn đỏ, và phiên dừng khi test đang được chạy lại.
**Bài học:** Quét lỗi bị nuốt trước khi tuyên bố migration an toàn, vì một lỗi nuốt lặng có thể để workspace ở trạng thái nửa cũ nửa mới.
**Artefact:** Không có.
**Góc người ngoài:** cách làm phổ biến là Thường dev bỏ qua lỗi đọc file trong vòng lặp để code gọn, rồi không ai nhận ra cho đến khi dữ liệu hỏng; ở đây khác ở Agent coi việc nuốt lỗi là rủi ro dữ liệu và yêu cầu workspace không đổi khi lỗi xảy ra. Đây là thói quen an toàn dữ liệu người đọc ít khi làm.
