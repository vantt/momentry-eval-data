---
id: 2026-10-30-google-chan-scope-nhay-cam-khi
date: 2026-10-30
repo: repo
status: raw
signals: ["5"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L717", "claude:f0bf048d#L723"]
hook: "gcloud đăng nhập Google bị chặn 'This app is blocked' vì scope nhạy cảm"
tension: cam_ma_van_lot
sides: ["Dùng đúng công cụ chính thức của Google", "Chính app OAuth của gcloud bị Google chặn"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Google chặn scope nhạy cảm khi đăng nhập bằng gcloud

**Bối cảnh:** Cần thêm service account vào GA4 qua API, nên xin scope analytics.manage.users cho gcloud.
**Chuyện gì xảy ra:** Màn hình báo 'This app is blocked' vì app OAuth mặc định của gcloud không được phép dùng scope nhạy cảm. Phần GA4 chuyển sang thêm quyền bằng tay trong giao diện, mất khoảng 30 giây.
**Bài học:** Scope nhạy cảm có thể bị chặn ở mức app mặc định; đừng coi việc cấp quyền qua API là chắc chắn có.
**Artefact:** Ảnh màn hình thông báo bị chặn (đã che email).
