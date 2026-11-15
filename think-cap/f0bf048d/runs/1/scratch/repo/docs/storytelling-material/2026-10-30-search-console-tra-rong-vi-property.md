---
id: 2026-10-30-search-console-tra-rong-vi-property
date: 2026-10-30
repo: repo
status: raw
signals: ["2"]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest, outsider]
lines: ["claude:f0bf048d#L749", "claude:f0bf048d#L915", "claude:f0bf048d#L963"]
hook: "Search Console trả rỗng không phải do quyền, mà do chọn nhầm bản www"
tension: tuong_ma_hoa_ra
sides: ["Kết quả rỗng trông như lỗi xác thực", "Thật ra property www cũ đã 0 lượt hiển thị từ tháng 7"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Search Console trả rỗng vì property sai, không phải lỗi xác thực

**Bối cảnh:** Service account đã được cấp quyền, nhưng API trả về rỗng.
**Chuyện gì xảy ra:** Ban đầu cả GA4 và Search Console đều trả {} vì chưa cấp quyền. Sau khi cấp, property Search Console được chọn là bản www cũ với 0 lượt hiển thị từ tháng 7, trong khi website 301 chuyển về bản không www. Kết quả rỗng dễ bị đọc nhầm là lỗi xác thực.
**Bài học:** Dữ liệu rỗng có thể do chọn sai property, không nhất thiết do quyền; kiểm tra redirect và danh sách property trước.
**Artefact:** So sánh hai property www và không www trong Search Console (đã che tên miền nếu cần).
**Góc người ngoài:** cách làm phổ biến là Thường phải xuất CSV từ GA4/Search Console rồi dán cho AI, hoặc tự viết connector/API riêng cho từng nguồn dữ liệu; ở đây khác ở Agent tự gọi API, có service account riêng, và tự dò đúng property. Người đọc sẽ muốn biết vì sao không cần copy số liệu tay.
