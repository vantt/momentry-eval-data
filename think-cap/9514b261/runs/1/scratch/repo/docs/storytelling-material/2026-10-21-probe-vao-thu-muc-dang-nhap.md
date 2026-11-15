---
id: 2026-10-21-probe-vao-thu-muc-dang-nhap
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2526", "claude:9514b261#L2862", "claude:9514b261#L2877", "claude:9514b261#L2908", "claude:9514b261#L2966", "claude:9514b261#L3062"]
hook: "Kho đăng nhập trống không báo lỗi, mà treo 200–300 giây"
tension: tuong_ma_hoa_ra
sides: ["Tưởng thiếu dữ liệu sẽ lỗi nhanh", "Thật ra treo im lặng, stderr chỉ báo bỏ qua"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe vào thư mục đăng nhập chưa có dữ liệu treo 200–300 giây thay vì lỗi nhanh

**Bối cảnh:** Agent thêm một đường dùng mới cho một nhà cung cấp và probe nó để xác nhận chạy được, trong khi thư mục đăng nhập của đường đó còn trống.
**Chuyện gì xảy ra:** Probe vào kho trống treo khoảng 200 đến 300 giây, còn stderr chỉ báo credential refresh bị bỏ qua vì thiếu file. Agent tự gây lỗi này và phải gỡ quarantine, tắt tài khoản và chạy lại. Sau khi đăng nhập xong, probe pass trong 23 giây.
**Bài học:** Đừng probe vào thư mục đăng nhập chưa có dữ liệu; kiểm sự tồn tại của file đăng nhập trước, vì nó treo thay vì báo lỗi.
**Artefact:** Dòng thời gian probe: treo 200 giây, treo 300 giây, sau đăng nhập pass 23 giây.
