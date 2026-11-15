---
id: 2026-11-02-installer-mau-test-tren-release-gia
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L293", "claude:6a207191#L296", "claude:6a207191#L298", "claude:6a207191#L870", "claude:6a207191#L878", "claude:6a207191#L880"]
hook: "Lệnh gỡ cài bị chính kiểm tra installer chưa đóng dấu chặn lại"
tension: cam_ma_van_lot
sides: ["Kiểm tra 'unstamped installer' để bảo vệ lúc cài", "Nó chặn cả lệnh gỡ cài vốn không cần version"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer mẫu test trên release giả: bắt được lỗi gỡ cài và lỗi không có terminal

**Bối cảnh:** Installer mẫu viết bằng POSIX sh cho một CLI được test trên một bản release giả qua file://, trong thư mục HOME tạm.
**Chuyện gì xảy ra:** Lần test đầu, lệnh gỡ cài bị chặn bởi kiểm tra 'unstamped installer', vốn áp dụng cả cho lệnh không cần version. Agent chuyển kiểm tra xuống sau nhánh uninstall. Lần test thứ hai chạy bằng dash để đảm bảo POSIX thật: khi không có terminal, /dev/tty tồn tại nhưng không mở được nên script crash thay vì báo cần --yes. Sửa bằng cách thử mở /dev/tty thật sự.
**Bài học:** Kiểm tra quyền tồn tại không đủ, vì /dev/tty có thể tồn tại mà không mở được. Hãy test installer khi không có terminal và bằng dash, không chỉ bash.
**Artefact:** Output của hai lệnh: 'error: unstamped installer' và 'confirmation needed but no terminal is available'. Không chụp đường dẫn scratchpad.
