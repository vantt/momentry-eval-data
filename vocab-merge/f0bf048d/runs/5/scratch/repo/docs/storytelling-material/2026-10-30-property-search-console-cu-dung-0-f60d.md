---
id: 2026-10-30-property-search-console-cu-dung-0-f60d
code: M-M8MZ
aliases: [M-M8MZ]
date: 2026-10-30
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L761", "claude:f0bf048d#L915"]
hook: "Property Search Console cấp đúng mà 0 lượt hiển thị từ tháng 7"
tension: tuong_ma_hoa_ra
sides: ["Đã cấp property cho site", "Site chuyển 301 sang bản không www nên là property khác"]
strength: 3
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Property Search Console cũ đứng 0 lượt hiển thị vì site chuyển hướng 301 sang bản không www

**Bối cảnh:** Đã cấp quyền cho service account trên property theo tên website người dùng đưa.
**Chuyện gì xảy ra:** Property đã cấp là bản www, có 0 lượt hiển thị từ tháng 7. Website chuyển 301 sang bản không www nên Search Console có hai property khác nhau. Agent phải tự chọn property khớp với canonical host, không phải người vận hành đoán.
**Bài học:** Trước khi chọn property để đo, kiểm chuyển hướng canonical; số 0 kéo dài là dấu hiệu sai property chứ không phải site không có traffic.
**Artefact:** Dropdown property hoặc kết quả curl cho thấy chuyển hướng 301 (che domain).
