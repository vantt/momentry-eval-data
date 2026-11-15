---
id: 2026-11-02-gui-skill-len-hub-bi-chan-c4b4
code: M-YABS
aliases: [M-YABS]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyen_nhan_bat_ngo, khac]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L996", "claude:6a207191#L1007", "claude:6a207191#L1065", "claude:6a207191#L1074", "claude:6a207191#L1084", "claude:6a207191#L1102", "claude:6a207191#L1109", "claude:6a207191#L1170"]
hook: "Lỗi gợi ý cờ --user, nhưng bản cài trên máy chưa có cờ đó"
tension: tuong_ma_hoa_ra
sides: ["Thông báo lỗi bảo thêm cờ --user", "Máy cài bản cũ nên cờ đó không tồn tại"]
strength: 2
stakes: 1
hits: 1
runs: 1
unverified_facts: ["0.13"]
privacy: unchecked
links: []
threads: []
---

# Gửi skill lên hub bị chặn: gợi ý cờ --user không tồn tại vì máy cài bản cũ

**Bối cảnh:** Hub chạy skillstation 0.12, máy agent đang chạy 0.8. Lệnh gửi skill có --yes bị chặn vì hub chưa được tin cậy ở cấp user.
**Chuyện gì xảy ra:** Lệnh có tiền tố ! trong Claude Code không tương tác nên không hỏi xác nhận được, chỉ in bản xem trước. Thông báo lỗi gợi ý cờ --user nhưng bản cũ không có cờ đó. Nâng lên 0.13, kết nối ở cấp user, doctor báo Healthy, rồi gửi được và nhận mã SUB.
**Bài học:** Thông báo lỗi phải gợi ý cờ có thật ở đúng phiên bản đang chạy. Khi có cổng an toàn, lệnh cần xác nhận phải chạy trong terminal thật.
**Artefact:** Dòng WHY và FIX của thông báo lỗi, đã che địa chỉ hub. Cần che IP và tên máy.
