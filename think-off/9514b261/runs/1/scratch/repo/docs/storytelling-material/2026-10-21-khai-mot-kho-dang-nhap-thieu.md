---
id: 2026-10-21-khai-mot-kho-dang-nhap-thieu
date: 2026-10-21
repo: repo
status: raw
signals: []
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2526", "claude:9514b261#L2533", "claude:9514b261#L2877", "claude:9514b261#L2908", "claude:9514b261#L2966"]
hook: "Khai thêm một kho đăng nhập trống, lỗi vài giây thành treo 200 giây"
tension: giup_ma_hai
sides: ["khai thêm kho tài khoản để có thêm đường chạy", "lỗi nhanh vài giây thành treo 200 giây"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Khai một kho đăng nhập thiếu file: lỗi nhanh biến thành treo 200 giây

**Bối cảnh:** Để xai chạy được, em khai tài khoản vào kho omp chưa có đăng nhập.
**Chuyện gì xảy ra:** Trước đó probe xai lỗi nhanh trong vài giây. Sau khi khai kho omp trống, lượt probe treo khoảng 200 giây, stderr báo refresh-ahead bị bỏ qua vì file thiếu. Em gỡ khai báo để trả về lỗi nhanh, rồi đặt disabled để ghế xai bị loại ngay thay vì treo.
**Bài học:** Một cấu hình trông đầy đủ có thể tệ hơn lỗi rõ ràng. Đo cả thời gian thất bại, không chỉ kết quả.
**Artefact:** Hai dòng stderr (missing-file) và kết quả probe, che đường dẫn.
