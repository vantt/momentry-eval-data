---
id: 2026-10-31-truoc-khi-chot-tai-lieu-thiet
date: 2026-10-31
repo: repo
status: raw
signals: []
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [outsider]
lines: ["claude:f0bf048d#L1843", "claude:f0bf048d#L1855", "claude:f0bf048d#L1861", "claude:f0bf048d#L1874", "claude:f0bf048d#L1875", "claude:f0bf048d#L1878", "claude:f0bf048d#L1891"]
hook: "Tự đọc lại thiết kế của mình, không thấy lỗ hổng chính mình tạo ra"
tension: tuong_ma_hoa_ra
sides: ["tác giả tự rà lại bản thiết kế là đủ", "agent độc lập tìm ra 3 lỗ hổng: mã dev, PAT dùng chung, không backup"]
strength: 2
stakes: 3
hits: 0
runs: 1
privacy: unchecked
links: []
threads: []
---

# Trước khi chốt tài liệu thiết kế quyền, agent viết bản nháp rồi giao cho một agent độc lập phản biện. Phản biện đưa ra lỗ hổng cụ thể (mã đăng nhập dev, PAT của chủ dùng chung với agent, không có backup). Agent tự kiểm lại từng điểm trên máy trước khi sửa thành bản v2.

**Chuyện gì xảy ra:** Trước khi chốt tài liệu thiết kế quyền, agent viết bản nháp rồi giao cho một agent độc lập phản biện. Phản biện đưa ra lỗ hổng cụ thể (mã đăng nhập dev, PAT của chủ dùng chung với agent, không có backup). Agent tự kiểm lại từng điểm trên máy trước khi sửa thành bản v2.
**Góc người ngoài:** cách làm phổ biến là Người làm tự đọc lại bản thiết kế của mình, rất khó thấy lỗ hổng do chính mình tạo ra; ở đây khác ở Có một vòng phản biện riêng với tiêu chí rõ (tìm cách leo quyền, cách lừa agent), và mọi phát hiện đều được xác minh trên hệ thống thật. Người đọc muốn biết cách tự tạo vòng này.
