---
id: 2026-10-30-tao-service-account-bang-gcloud-google-f60d
code: M-FWZW
aliases: [M-FWZW]
date: 2026-10-30
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, số trước/sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L521", "claude:f0bf048d#L717", "claude:f0bf048d#L723", "claude:f0bf048d#L728", "claude:f0bf048d#L741", "claude:f0bf048d#L749"]
hook: "Tạo xong project, key, service account, nhưng Google chặn đúng bước cấp quyền GA4"
tension: cam_ma_van_lot
sides: ["Mọi bước khác chạy được bằng lệnh", "Bước cấp quyền GA4 bị Google chặn"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tạo service account bằng gcloud: Google chặn scope GA4, phần còn lại làm được bằng lệnh

**Bối cảnh:** Cần service account đọc được GA4 và Search Console cho một site, project không gắn billing.
**Chuyện gì xảy ra:** gcloud chưa có trên máy nên cài bản 589.0.0 đã ghim và kiểm md5 khớp metadata trên GCS. Tạo project, bật 3 API, tạo service account và key đều chạy được. Lệnh cấp quyền GA4 qua scope analytics.manage.users bị Google chặn với client mặc định của gcloud (This app is blocked). Kiểm key bằng cách gọi API, cả hai trả về rỗng, đúng vì chưa có quyền nào.
**Bài học:** Đừng giả định mọi scope đều xin được với client mặc định; chuẩn bị đường thủ công (một lần thêm email trong UI) và kiểm xác thực trước khi có quyền.
**Artefact:** Chuỗi lệnh gcloud ngắn và thông báo This app is blocked (che email và project id).
