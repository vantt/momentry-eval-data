---
id: 2026-10-30-goi-coding-con-gan-cung-ten-f60d
code: M-54CB
aliases: [M-54CB]
date: 2026-10-30
repo: repo
status: raw
signals: [rang_buoc_thiet_ke]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:f0bf048d#L1125", "claude:f0bf048d#L1219", "claude:f0bf048d#L1222", "claude:f0bf048d#L1277"]
hook: "Gói Coding gắn cứng tên một khách, chưa bán được cho ai khác"
tension: tuong_ma_hoa_ra
sides: ["Tưởng đã có sản phẩm đóng gói bán được", "Thực ra gắn cứng workspace và repo của đúng một khách"]
strength: 1
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Gói coding còn gắn cứng tên workspace nên chưa bán cho khách khác được

**Bối cảnh:** Gói Coding là gói của phiên song song, chưa commit tại thời điểm đó.
**Chuyện gì xảy ra:** Gói gắn cứng workspace, tên công ty, và repo GitHub của một khách. Muốn bán bộ Coding cho khách khác thì phải chuyển sang đọc từ manifest của khách. Agent không tự sửa vì phiên kia đang chạy thử trên gói này.
**Bài học:** Đừng gắn tên khách, repo hay workspace vào gói. Mọi giá trị theo khách đưa vào qua manifest.
**Artefact:** Bảng các giá trị cứng cần chuyển sang manifest.
