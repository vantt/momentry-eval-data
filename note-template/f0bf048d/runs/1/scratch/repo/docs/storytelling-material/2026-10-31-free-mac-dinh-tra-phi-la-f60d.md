---
id: 2026-10-31-free-mac-dinh-tra-phi-la-f60d
code: M-Q9DF
aliases: [M-Q9DF]
date: 2026-10-31
repo: repo
status: raw
signals: [artefact_nhin_duoc, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1439", "claude:f0bf048d#L1546", "claude:f0bf048d#L1571", "claude:f0bf048d#L1595", "claude:f0bf048d#L1654"]
hook: "Free mặc định, trả phí chỉ bật theo khách; web khách đầu được 0,31 điểm"
tension: none
sides: []
strength: 0
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Free mặc định, trả phí là add-on theo khách; PageSpeed key báo lỗi rồi có điểm 0,31

**Bối cảnh:** Chủ muốn bộ SEO chạy được ở cả mức miễn phí và mức trả phí.
**Chuyện gì xảy ra:** Công cụ miễn phí mặc định gồm Search Console, GA4, PageSpeed và WebFetch. DataForSEO là add-on, bật cho từng khách trong manifest. Key PageSpeed đầu tiên báo API key not found, sau khi sửa đã gọi được. Điểm performance mobile của website khách đầu tiên là 0,31. Tài liệu được cập nhật để chủ biết khi nào bật, khi nào tắt add-on.
**Bài học:** Thiết kế hai mức cho các công cụ trả phí: mặc định miễn phí, add-on bật theo khách, và plan phải báo lỗi nếu add-on không có bộ nào cung cấp.
**Artefact:** Bảng hai mức công cụ, che key.
