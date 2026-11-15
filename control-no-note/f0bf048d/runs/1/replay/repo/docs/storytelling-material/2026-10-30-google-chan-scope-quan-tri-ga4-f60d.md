---
id: 2026-10-30-google-chan-scope-quan-tri-ga4-f60d
code: M-MX01
aliases: [M-MX01]
date: 2026-10-30
repo: repo
status: raw
signals: [dao_quyet_dinh, rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L521", "claude:f0bf048d#L697", "claude:f0bf048d#L701", "claude:f0bf048d#L711", "claude:f0bf048d#L717", "claude:f0bf048d#L723"]
hook: "Google chặn scope quản trị, thêm tay chỉ mất 30 giây"
tension: it_ma_nhieu
sides: ["Cả buổi cài gcloud và đăng nhập vẫn bị chặn", "Thêm tay service account chỉ mất 30 giây"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Google chặn scope quản trị GA4 của gcloud, phải thêm tay

**Bối cảnh:** Cần tạo service account và cấp quyền GA4 tự động bằng gcloud, không dùng thao tác tay. Máy chưa có gcloud.
**Chuyện gì xảy ra:** Ban đầu gcloud chưa được cài. Agent cài gcloud 589.0.0 (bản cũ hơn 591.0.0 khoảng hai tuần) và đối chiếu md5 với metadata trên GCS. Khi đăng nhập để cấp quyền GA4 qua API, Google báo app bị chặn vì scope analytics.manage.users nhạy cảm. Phần GA4 chuyển sang thêm service account vào property bằng tay, mất khoảng 30 giây.
**Bài học:** Scope nhạy cảm của client mặc định có thể bị chặn. Cần kế hoạch dự phòng thao tác tay cho chỗ đó trước khi tự động hoá.
**Artefact:** Màn hình thông báo app bị chặn (che email và tên dự án).
