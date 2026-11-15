---
id: 2026-11-01-thay-pat-cua-chu-tren-may-f60d
code: M-S6V9
aliases: [M-S6V9]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, so_truoc_so_sau]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L2400", "claude:f0bf048d#L2435", "claude:f0bf048d#L2457", "claude:f0bf048d#L2543", "claude:f0bf048d#L2550", "claude:f0bf048d#L2569", "claude:f0bf048d#L2578"]
hook: "Sudo lần hai báo lỗi vì lần đầu đã xoá file PAT"
tension: giup_ma_hai
sides: ["Lệnh đăng nhập lần đầu đã thành công", "Lần hai báo lỗi vì file PAT đã bị xoá"]
strength: 1
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Thay PAT của chủ trên máy agent: lần sudo thứ hai báo lỗi

**Bối cảnh:** Daemon chạy agent vẫn đăng nhập bằng PAT của chủ. Cần thay bằng một danh tính riêng.
**Chuyện gì xảy ra:** Lệnh login lần hai báo lỗi vì lần đầu đã chạy thành công và xoá file PAT. Tìm được PAT của chủ ở đúng 3 chỗ trong home của user daemon. Tạo PAT mới, cập nhật cả 3 chỗ, kiểm PAT mới hoạt động, rồi mới thu hồi PAT cũ (trả về 204). Chuyển 12 agent sang runtime mới: PUT từng phần thành công, POST thì trả 405. Sau đó chạy thử một issue, agent chạy đúng dưới user mới và không đọc được PAT cũ.
**Bài học:** Thay credential theo thứ tự: tạo mới, cập nhật mọi bản sao, kiểm, rồi thu hồi. Grep toàn bộ home để tìm bản sao trước khi thu hồi.
**Artefact:** Bảng 3 vị trí bản sao PAT, che đường dẫn và token.
