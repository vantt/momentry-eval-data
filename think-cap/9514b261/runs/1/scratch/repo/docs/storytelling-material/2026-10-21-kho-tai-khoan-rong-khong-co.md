---
id: 2026-10-21-kho-tai-khoan-rong-khong-co
date: 2026-10-21
repo: repo
status: raw
signals: [nguyên nhân bất ngờ, số trước/sau]
source: "chat Claude, claude:9514b261"
sessions: ["claude:9514b261"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:9514b261#L1999", "claude:9514b261#L2029", "claude:9514b261#L2191", "claude:9514b261#L2284", "claude:9514b261#L2630"]
hook: "Kho tài khoản rỗng, nhưng deepseek và glm vẫn chạy được mà không bao giờ được chọn"
tension: tuong_ma_hoa_ra
sides: ["Kho rỗng nghe như tài khoản hỏng", "Tài khoản chạy được nhưng walk chỉ liệt kê bốn family nên bị bỏ qua"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# “Kho tài khoản rỗng” không có nghĩa là tài khoản hỏng; chuỗi dự phòng chỉ thu hẹp

**Bối cảnh:** Người dùng yêu cầu kiểm mọi tài khoản LLM còn dùng được không và nếu một model hết quota thì chuyển sang đâu.
**Chuyện gì xảy ra:** Lệnh inspect trả providers rỗng vì cấu hình không khai tài khoản nào, nên fgOS không theo dõi quota. Lượt probe đầu chỉ có một family chạy được. Sau khi người dùng copy lại phiên đăng nhập, hai family khác chạy được, nhưng walk dự phòng chỉ liệt kê bốn family nên deepseek và glm không bao giờ được chọn dù chạy được.
**Bài học:** Chuỗi dự phòng chỉ có thể thu hẹp theo danh sách đã khai; kiểm xem phương án dự phòng có nằm trong danh sách đó không.
**Artefact:** Bảng kết quả probe theo family ở hai thời điểm (trước và sau khi copy phiên), chỉ ghi family, invocation và kết quả.
