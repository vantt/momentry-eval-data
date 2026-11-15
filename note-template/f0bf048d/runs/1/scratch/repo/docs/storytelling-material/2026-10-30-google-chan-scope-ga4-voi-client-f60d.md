---
id: 2026-10-30-google-chan-scope-ga4-voi-client-f60d
code: M-ZH9Y
aliases: [M-ZH9Y]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L521", "claude:f0bf048d#L717", "claude:f0bf048d#L751"]
hook: "Google chặn gcloud khi xin scope GA4, 30 giây làm tay là xong"
tension: cam_ma_van_lot
sides: ["Cả quy trình làm được bằng CLI", "Google khoá scope GA4 với client gcloud, phải làm tay"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Google chặn scope GA4 với client mặc định của gcloud

**Bối cảnh:** Muốn tự động hoá toàn bộ việc tạo project, service account và cấp quyền GA4 bằng CLI.
**Chuyện gì xảy ra:** gcloud chưa có trên máy. Sau khi cài và đăng nhập, lệnh xin scope analytics.manage.users bị Google chặn với thông báo app bị khoá, vì client mặc định của gcloud không được phép dùng scope đó. Phần project, bật API, tạo service account và key làm được bằng CLI. Phần cấp quyền GA4 phải làm tay trong khoảng 30 giây.
**Bài học:** Đừng dựa vào scope nhạy cảm qua client mặc định. Tách ngay từ đầu phần CLI làm được và phần người phải làm.
**Artefact:** Ảnh thông báo bị chặn, che email.
