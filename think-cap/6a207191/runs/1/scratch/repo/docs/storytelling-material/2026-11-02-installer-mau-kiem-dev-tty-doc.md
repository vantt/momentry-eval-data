---
id: 2026-11-02-installer-mau-kiem-dev-tty-doc
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L293", "claude:6a207191#L296", "claude:6a207191#L298", "claude:6a207191#L871", "claude:6a207191#L878", "claude:6a207191#L880", "claude:6a207191#L890"]
hook: "/dev/tty đọc ghi được, nhưng mở ra thì script vẫn crash"
tension: tuong_ma_hoa_ra
sides: ["Kiểm tra -r và -w báo /dev/tty dùng được", "Không có terminal nên mở thật thì crash"]
strength: 2
stakes: 1
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer mẫu: kiểm /dev/tty 'đọc ghi được' vẫn crash khi không có terminal

**Bối cảnh:** Installer POSIX mẫu được thử với một release giả phục vụ qua file://, chạy bằng dash để chắc là đúng POSIX.
**Chuyện gì xảy ra:** Lần chạy đầu, gỡ cài đặt bị chặn bởi kiểm tra 'installer chưa đóng dấu phiên bản' đặt trước nhánh gỡ cài đặt, nên agent chuyển kiểm tra xuống sau. Khi chạy bằng dash trong môi trường không có terminal, script crash: /dev/tty qua được kiểm tra -r và -w nhưng không mở được. Sửa bằng cách thử mở thật. Bây giờ không có terminal thì báo cần --yes, có terminal thì hỏi và hủy khi trả lời n.
**Bài học:** Kiểm tra 'tồn tại và có quyền' không đủ với thiết bị. Hãy thử mở thật rồi mới quyết định.
**Artefact:** Hai đầu ra terminal: không có terminal (báo cần --yes) và có terminal (hỏi, hủy khi n).
