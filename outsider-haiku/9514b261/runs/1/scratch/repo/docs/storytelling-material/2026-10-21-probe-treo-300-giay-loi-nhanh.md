---
id: 2026-10-21-probe-treo-300-giay-loi-nhanh
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, đảo quyết định]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:9514b261#L2526", "claude:9514b261#L2862", "claude:9514b261#L2895", "claude:9514b261#L2908", "claude:9514b261#L2966"]
hook: "Lỗi nhanh 1 giây còn hơn treo im lặng 300 giây"
tension: tuong_ma_hoa_ra
sides: ["Một nhà cung cấp bị treo cứ tưởng chỉ chậm", "Nó chiếm ghế hội đồng 200–300 giây mỗi lần"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Probe treo 300 giây: lỗi nhanh tốt hơn lỗi im lặng

**Bối cảnh:** Probe đường omp của một tài khoản chưa có đăng nhập không báo lỗi mà treo, còn hệ thống tự đặt quarantine cho tài khoản đó.
**Chuyện gì xảy ra:** Probe xai treo 200 đến 300 giây với lỗi refresh-ahead vì thư mục đăng nhập omp không tồn tại, trong khi kho pi của cùng tài khoản đã hết hạn OAuth. Hệ thống đặt quarantine, phải chạy lệnh reconcile để gỡ. Tạm thời agent đặt disabled=true để xai bị loại ngay khỏi chuỗi thay vì treo ghế hội đồng.
**Bài học:** Khi một đường thiếu đăng nhập, nó nên thoát nhanh có mã lỗi thay vì treo. Khi phát hiện treo, tắt tài khoản trong config trước rồi mới sửa gốc.
**Artefact:** Một dòng stderr (đã che email) đặt cạnh bảng trạng thái quarantine trước và sau khi gỡ.
