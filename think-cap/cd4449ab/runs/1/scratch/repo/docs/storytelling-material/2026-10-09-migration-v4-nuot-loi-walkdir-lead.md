---
id: 2026-10-09-migration-v4-nuot-loi-walkdir-lead
date: 2026-10-09
repo: repo
status: raw
signals: []
source: "chat, omp:cd4449ab"
sessions: ["omp:cd4449ab"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["omp:cd4449ab#L3656", "omp:cd4449ab#L3960", "omp:cd4449ab#L3962", "omp:cd4449ab#L3978", "omp:cd4449ab#L3980", "omp:cd4449ab#L3987", "omp:cd4449ab#L3989", "omp:cd4449ab#L3996", "omp:cd4449ab#L3998", "omp:cd4449ab#L3999"]
hook: "Một dấu '_ =' nuốt lỗi migration, người duyệt mới bắt được"
tension: cam_ma_van_lot
sides: ["Migration có kiểm tra và test", "Một lỗi bị vứt bằng '_ =' lọt qua"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Migration v4 nuốt lỗi WalkDir, lead bắt được

**Bối cảnh:** Migration v4 đọc các file insight cũ bằng cách đi cây thư mục.
**Chuyện gì xảy ra:** Lead chỉ ra một chỗ gọi filepath.WalkDir với lỗi bị bỏ bằng '_ ='. grep tìm đúng một dòng như vậy. Sau sửa, mọi lỗi đọc, parse và walk đều trả về lỗi có tên file. Test thêm: một file insight hỏng làm preview thất bại và in tên file, workspace không đổi.
**Bài học:** Trước khi tin migration là fail-closed, grep '_ =' trong code migration; lỗi bị nuốt thường nằm ở chỗ không ai nghi.
**Artefact:** Đầu ra test preview lỗi có tên file, che đường dẫn tuyệt đối.
