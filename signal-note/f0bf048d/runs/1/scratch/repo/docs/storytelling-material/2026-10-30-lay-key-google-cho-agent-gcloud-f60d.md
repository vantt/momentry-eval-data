---
id: 2026-10-30-lay-key-google-cho-agent-gcloud-f60d
code: M-D50R
aliases: [M-D50R]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L503", "claude:f0bf048d#L511", "claude:f0bf048d#L521", "claude:f0bf048d#L711", "claude:f0bf048d#L717", "claude:f0bf048d#L723", "claude:f0bf048d#L740"]
hook: "Google chặn gcloud của chính mình với thông báo 'This app is blocked'"
tension: cam_ma_van_lot
sides: ["đã cài gcloud và đăng nhập đúng cách", "Google chặn scope GA4, phải thêm tay"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Lấy key Google cho agent: gcloud bị chặn scope, project không gắn billing

**Bối cảnh:** Chủ muốn agent tự có service account để đọc GA4 và Search Console. Chủ cũng hỏi liệu service account có tốn tiền không.
**Chuyện gì xảy ra:** Agent cài gcloud không cần sudo, đối chiếu md5 với metadata trên GCS. Đăng nhập bằng --no-launch-browser để chủ đăng nhập từ laptop. Lệnh ADC xin scope analytics.manage.users bị Google chặn với thông báo 'This app is blocked', nên phần GA4 phải thêm tay. Project được tạo không gắn billing để không phát sinh phí; API chỉ trả lỗi 429 khi vượt hạn mức, không tự tính tiền.
**Bài học:** Khi OAuth client mặc định bị chặn một scope nhạy cảm, hãy có sẵn phương án thủ công thay vì coi bước đó là bắt buộc. Không gắn billing là cách chắc nhất để loại rủi ro chi phí.
**Artefact:** Thông báo 'This app is blocked' (che email và tên project).
