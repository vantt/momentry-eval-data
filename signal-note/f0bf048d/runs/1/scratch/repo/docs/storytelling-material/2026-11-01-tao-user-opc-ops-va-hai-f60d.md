---
id: 2026-11-01-tao-user-opc-ops-va-hai-f60d
code: M-E0W2
aliases: [M-E0W2]
date: 2026-11-01
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo]
source: "chat Claude, claude:f0bf048d"
sessions: ["claude:f0bf048d"]
captured_by: harvest
hit_by: [hotspot, harvest]
lines: ["claude:f0bf048d#L3370", "claude:f0bf048d#L3382", "claude:f0bf048d#L3394", "claude:f0bf048d#L3396", "claude:f0bf048d#L3409", "claude:f0bf048d#L3410", "claude:f0bf048d#L3418", "claude:f0bf048d#L3419"]
hook: "Lệnh kiểm tra trả exit 1 nhưng vẫn in 'syntax ok'"
tension: tuong_ma_hoa_ra
sides: ["màn hình in syntax ok", "exit code là 1"]
strength: 2
stakes: 0
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Tạo user opc-ops và hai danh tính Multica: kiểm tra trả exit 1 nhưng vẫn in OK

**Bối cảnh:** Chuẩn bị tách System Operator: tạo user Linux riêng và hai user Multica, một cho daemon, một cho quản trị.
**Chuyện gì xảy ra:** Lệnh kiểm tra cú pháp script trả exit 1 nhưng vẫn in 'syntax ok'. Lệnh liệt kê thành viên workspace thất bại vì sai tham số, phải dùng cú pháp khác. Sau đó agent kiểm lại từng workspace và thấy user daemon có đúng vai trò member. Hai PAT của danh tính mới được lưu tạm trong home của chủ.
**Bài học:** Đừng tin tuyệt đối vào mã thoát hay dòng 'OK' riêng lẻ; đọc đầu ra thật. Khi kiểm quyền, liệt kê từng nơi thay vì tin một lệnh tổng.
**Artefact:** Danh sách thành viên workspace (che email).
