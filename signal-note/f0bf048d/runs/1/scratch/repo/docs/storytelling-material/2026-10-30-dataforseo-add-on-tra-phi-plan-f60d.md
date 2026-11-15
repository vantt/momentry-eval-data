---
id: 2026-10-30-dataforseo-add-on-tra-phi-plan-f60d
code: M-G75F
aliases: [M-G75F]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L1414", "claude:f0bf048d#L1439", "claude:f0bf048d#L1601", "claude:f0bf048d#L1603", "claude:f0bf048d#L1620", "claude:f0bf048d#L1654"]
hook: "Chưa khách nào mua DataForSEO mà plan vẫn tạo server cho nó"
tension: cam_ma_van_lot
sides: ["add-on trả phí, khách chưa mua", "plan vẫn tạo server dataforseo"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# DataForSEO: add-on trả phí, plan tạo nhầm server khi khách chưa mua

**Bối cảnh:** Bộ SEO có hai mức: miễn phí mặc định và trả phí khi khách mua DataForSEO.
**Chuyện gì xảy ra:** DataForSEO nạp tối thiểu 50 USD, không hết hạn. Agent ước tính 2 đến 5 USD mỗi khách mỗi tháng, ghi rõ đó là ước tính của mình. Lúc khách chưa mua, plan vẫn tạo server dataforseo; sửa bằng cách lọc add-on khỏi danh sách và kiểm lại bằng plan. Mức miễn phí dùng key PageSpeed, gọi thử được điểm mobile 0,31.
**Bài học:** Điều kiện trả phí phải áp cho cả plan, không chỉ cho deploy. Ghi rõ đâu là giá nhà cung cấp và đâu là ước tính của bạn.
**Artefact:** Bảng giá và dịch vụ DataForSEO (lấy từ trang giá, ghi ngày).
