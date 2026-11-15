---
id: 2026-11-02-installer-mau-bi-loi-ton-tai-c4b4
code: M-T52X
aliases: [M-T52X]
date: 2026-11-02
repo: repo
status: raw
signals: [nguyên nhân bất ngờ]
source: "chat Claude, claude:6a207191"
sessions: ["claude:6a207191"]
captured_by: harvest
hit_by: [harvest]
lines: ["claude:6a207191#L293", "claude:6a207191#L296", "claude:6a207191#L298", "claude:6a207191#L299", "claude:6a207191#L300", "claude:6a207191#L871", "claude:6a207191#L878", "claude:6a207191#L880"]
hook: "Lệnh gỡ cài đặt bị chặn vì bản thử thiếu số version"
tension: nho_ma_to
sides: ["Gỡ cài đặt vốn không cần version", "Kiểm tra version chặn cả lệnh gỡ, /dev/tty có mà không mở được"]
strength: 2
stakes: 2
hits: 1
runs: 1
privacy: unchecked
links: []
threads: []
---

# Installer mẫu bị lỗi 'tồn tại nhưng không mở được' và chặn cả lệnh gỡ cài đặt

**Bối cảnh:** Khung install.sh kiểu POSIX được thử với một release giả lập qua file://, rồi chạy bằng dash để kiểm tra đúng POSIX.
**Chuyện gì xảy ra:** Lần chạy đầu, lệnh gỡ cài đặt bị chặn bởi kiểm tra 'unstamped installer' vì bản thử không có version, dù gỡ cài đặt không cần version; agent chuyển kiểm tra này xuống sau nhánh gỡ. Khi chạy bằng dash không có terminal, script kiểm tra /dev/tty tồn tại và có quyền đọc ghi, nhưng không mở được nên crash thay vì báo cần --yes. Sửa bằng cách thử mở /dev/tty thật. Sau đó không có terminal thì báo lỗi đúng, có terminal thì hỏi và hủy khi người dùng gõ n.
**Bài học:** Kiểm tra /dev/tty bằng -r và -w là chưa đủ; phải thử mở nó, vì file tồn tại không có nghĩa là dùng được.
**Artefact:** Dòng output 'error: confirmation needed but no terminal is available'. Không cần che.
