---
id: 2026-10-29-multica-openclaw-truot-ban-openclaw-bi-c455
code: M-65SW
aliases: [M-65SW]
date: 2026-10-29
repo: repo
status: raw
signals: [số, nguyên nhân]
source: "chat Claude, claude:0faf0bb2"
sessions: ["claude:0faf0bb2"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:0faf0bb2#L3041", "claude:0faf0bb2#L3045", "claude:0faf0bb2#L3061", "claude:0faf0bb2#L3083", "claude:0faf0bb2#L3088", "claude:0faf0bb2#L3150"]
hook: "Sửa chuỗi phiên bản để qua mặt kiểm tra, CLI chạy nhưng thoát không output"
tension: giup_ma_hai
sides: ["Đổi chuỗi phiên bản để vượt rào", "CLI chạy được nhưng gateway lỗi, spike trượt"]
strength: 2
stakes: 3
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Multica + OpenClaw trượt: bản OpenClaw bị chặn vì thấp hơn phiên bản tối thiểu

**Bối cảnh:** Spike Multica dùng OpenClaw 2026.3.13 đóng gói trong AICoworker.
**Chuyện gì xảy ra:** Lần chạy đầu bị từ chối với thông báo 'below the minimum supported version 2026.5.5'. Agent thử đổi chuỗi phiên bản trong wrapper thành 2026.5.5. CLI chạy được, nhưng include config bị báo 'Include path escapes config directory', gọi gateway thất bại, rồi thoát không có output. Ngoài ra, với bản này --session-id dồn mọi lượt vào một session. Kết luận: spike trượt, kèm ba hướng đi tiếp.
**Bài học:** Giả mạo số phiên bản để qua kiểm tra chỉ đẩy lỗi xuống tầng sâu hơn. Hãy xem xét gate phiên bản trước khi chọn cách tích hợp.
**Artefact:** Dòng báo lỗi 'below the minimum supported version'. Đường dẫn đã che.
