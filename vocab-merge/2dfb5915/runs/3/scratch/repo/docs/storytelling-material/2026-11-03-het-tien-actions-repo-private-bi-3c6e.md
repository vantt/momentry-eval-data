---
id: 2026-11-03-het-tien-actions-repo-private-bi-3c6e
code: M-5AZZ
aliases: [M-5AZZ]
date: 2026-11-03
repo: repo
status: raw
signals: [ràng buộc định hình thiết kế, nguyên nhân bất ngờ]
source: "chat Claude, claude:2dfb5915"
sessions: ["claude:2dfb5915"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:2dfb5915#L3785", "claude:2dfb5915#L3794", "claude:2dfb5915#L3804"]
hook: "Repo private hết phút Actions, tới build cũng không chạy, công khai là xong"
tension: gap_ma_phai_chon
sides: ["Giữ repo private để kín nhưng mọi job bị từ chối chạy", "Công khai để Actions miễn phí, sau khi quét lịch sử không thấy token nào"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Hết tiền Actions: repo private bị GitHub từ chối chạy mọi job

**Bối cảnh:** Khi cần tag rc.3, mọi job CI đều bị từ chối với thông báo về thanh toán thất bại hoặc hạn mức chi tiêu.
**Chuyện gì xảy ra:** Repo private dùng phút Actions tính phí; không job nào khởi động, kể cả build. Người dùng chuyển repo sang public, Actions miễn phí, và rc.3 phát hành được ngay sau đó. Trước khi công khai, agent quét lịch sử git tìm mẫu token và khoá, không thấy khớp.
**Bài học:** Repo private trên GitHub có thể dừng cả pipeline phát hành vì hạn mức Actions; biết điều này trước khi cần tag.
**Artefact:** Thông báo lỗi của GitHub (che tên tài khoản).
